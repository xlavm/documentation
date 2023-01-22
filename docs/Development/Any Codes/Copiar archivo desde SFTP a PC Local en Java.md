# Copiar archivo desde SFTP a PC Local en Java

Descargar las dependencias en GRADLE:

compile group: 'com.jcraft', name: 'jsch', version: '0.1.44-1'

    ```JAVA
    try {
        JSch ssh = new JSch();
        //usuario, host, puerto
        Session session = ssh.getSession("luanvane", "10.72.181.137", 22);
        java.util.Properties config = new java.util.Properties();
        config.put("StrictHostKeyChecking", "no");
        session.setConfig(config);
        session.setPassword("MxJ33$!!*g");
        session.connect();
        Channel channel = session.openChannel("sftp");
        channel.connect();
        ChannelSftp sftp = (ChannelSftp) channel;
        //directorio donde esta el archivo a copiar desde FTP
        sftp.cd("/imxuat/intra/imx/interfaces/cxref/imx_cxref_cli/ready");
        //de primero le enviamos el nombre del archivo que está en el FTP y de segundo se manda la ruta en el pc donde se guardará
        sftp.get("CDCXUPEN", "ArchivosInterfaces/");
        Boolean success = true;
        if (success) {
            // El archivo ha sido subido satisfactoriamente
        }
        channel.disconnect();
        session.disconnect();
    } catch (JSchException e) {
        System.out.println(e.getMessage().toString());
        e.printStackTrace();
    } catch (SftpException e) {
        System.out.println(e.getMessage().toString());
        e.printStackTrace();
    }
    ```
