# Descargar archivo desde ruta FTP

Creo la clase que se conecta al FTP y copia el archivo desde el FTP al local

    ```JAVA
    package co.com.miEmpresa.Utilidades;


    import com.jcraft.jsch.Channel;
    import com.jcraft.jsch.ChannelSftp;
    import com.jcraft.jsch.JSch;
    import com.jcraft.jsch.JSchException;
    import com.jcraft.jsch.Session;
    import com.jcraft.jsch.SftpException;
    import org.apache.commons.net.ftp.FTPClient;


    /** @author LuisAngel*/


    public class DescargaFTP {


        //metodo que copia el archivo del FTP a una ruta local
        public String copiarArchivoDeFTPALocal(String rutaDirectorioFTP, String RUTA_LOCAL_ARCHIVO, String nombreArchivo) {
            try {
                String resulCopiDeFTPALocal = "";
                JSch ssh = new JSch();
                //usuario, host, puerto
                Session session = ssh.getSession("luanvane", "10.72.181.137", 22);
                java.util.Properties config = new java.util.Properties();
                config.put("StrictHostKeyChecking", "no");
                session.setConfig(config);
                session.setPassword("MxJ33$!!*g");//Contraseña del usuario FTP
                session.connect();
                Channel channel = session.openChannel("sftp");//le desimos que es ftp seguro "sftp"
                channel.connect();
                ChannelSftp sftp = (ChannelSftp) channel;
                //directorio donde esta el archivo a copiar desde FTP
                sftp.cd(rutaDirectorioFTP);
                //de primero le enviamos el nombre del archivo que está en el FTP y de segundo se manda la ruta en el pc donde se guardará
                sftp.get(nombreArchivo, RUTA_LOCAL_ARCHIVO);
                Boolean success = true;
                if (!success) {
                    //dejo un mensaje
                    return resulCopiDeFTPALocal = "No se puedo copiar el archivo desde el FTP.";
                }
                channel.disconnect();
                session.disconnect();
                return resulCopiDeFTPALocal = "Se ha conectado al FTP y descargado el archivo correctamente";
            } catch (JSchException e) {
                System.out.println(e.getMessage());
                return resulCopiDeFTPALocal = "No hay Conexión con el FTP";
            } catch (SftpException e) {
                System.out.println(e.getMessage());
                return resulCopiDeFTPALocal = "No hay archivo generado en la ruta FTP. Es posible que se procese el último archivo generado en la ruta local";
            }
        }


        private static void showServerReply(FTPClient ftpClient) {
            String[] replies = ftpClient.getReplyStrings();
            if (replies != null && replies.length > 0) {
                for (String aReply : replies) {
                    System.out.println("SERVER: " + aReply);
                }
            }
        }
    }
    ```

Código para ejecutar el método de copiar de FTP a Local

    ```JAVA
    //orden de los parametros: ruta_archivo_ftp, ruta_archivo_local, nombre_archivo
    resulCopiDeFTPALocal = descargaFTP.copiarArchivoDeFTPALocal("/ftp/intra/", "/local/carpeta/archivo.txt", "archivo.txt");
    ```
