# Conectar vía SSH con Java y ejecutar comandos

Descargar las dependencias o librerías

    ```BASH
    <dependency>
        <groupId>com.jcraftgroupId>
        <artifactId>jschartifactId>
        <version>0.1.53version>
        <type>jartype>
    dependency>
    ```

Crear la clase conector con el servidor

    ```JAVA
    package co.com.miEmpresa.Modelo;
    /** @author LuisAngel*/
    import com.jcraft.jsch.ChannelExec;
    import com.jcraft.jsch.JSch;
    import com.jcraft.jsch.JSchException;
    import com.jcraft.jsch.Session;
    import java.io.BufferedReader;
    import java.io.IOException;
    import java.io.InputStream;
    import java.io.InputStreamReader;
     
    public class SSHConnector {
        private static final String ENTER_KEY = "n";//tecla ENTER
        private Session session;//sesion ssh
     
        //metodo que establece conexion ssh
        public void connect(String username, String password, String host, int port)
            throws JSchException, IllegalAccessException {
            if (this.session == null || !this.session.isConnected()) {
                JSch jsch = new JSch();
                this.session = jsch.getSession(username, host, port);
                this.session.setPassword(password);
                // Parametro para no validar key de conexion.
                this.session.setConfig("StrictHostKeyChecking", "no");
                this.session.connect();
            } else {
                throw new IllegalAccessException("Sesion SSH ya iniciada.");
            }
        }
        
        //metodo que permite ejecutar un comando ssh 
        public final String executeCommand(String command)
            throws IllegalAccessException, JSchException, IOException {
            if (this.session != null && this.session.isConnected()) {
                // Abrimos un canal SSH. Es como abrir una consola.
                ChannelExec channelExec = (ChannelExec) this.session.
                    openChannel("exec");
                InputStream in = channelExec.getInputStream();
                // Ejecutamos el comando.
                channelExec.setCommand(command);
                channelExec.connect();
                // Obtenemos el texto impreso en la consola.
                BufferedReader reader = new BufferedReader(new InputStreamReader(in));
                StringBuilder builder = new StringBuilder();
                String linea;
                while ((linea = reader.readLine()) != null) {
                    builder.append(linea);
                    builder.append(ENTER_KEY);
                }
                // Cerramos el canal SSH.
                channelExec.disconnect();
                // Retornamos el texto impreso en la consola.
                return builder.toString();
            } else {
                throw new IllegalAccessException("No existe sesion SSH iniciada.");
            }
        }
     
        //metodo que cierra la sesion ssh
        public final void disconnect() {
            this.session.disconnect();
        }
    }
    ```

Crear la clase de conexión con el servidor y dónde se digitan los comandos

    ```JAVA
    package co.com.miEmpresa.Modelo;
    /** @author LuisAngel*/
    import com.jcraft.jsch.JSchException;
    import java.io.IOException;


    public class SSHConnection {
        
        private static final String USERNAME = "faosorio";
        private static final String HOST = "10.72.165.96";
        private static final int PORT = 22;
        private static final String PASSWORD = "71685106";
     
        public static void main(String[] args) {
            try {
                SSHConnector sshConnector = new SSHConnector();
                //establezco la conexión con el servidor
                sshConnector.connect(USERNAME, PASSWORD, HOST, PORT);
                //ejecuto los comandos que quiera aquí:
                sshConnector.executeCommand("sudo su - svcimxdebco");
                sshConnector.executeCommand("cd /imxdevbco/intra/imx/interfaces/lim/comandos");
                sshConnector.executeCommand("sh UTILIZACIONES.ch");
                String result = sshConnector.executeCommand("ls -ltr");
                sshConnector.disconnect();
                //retorno el string del resultado del comando
                System.out.println("resultado es: "+result);
            } catch (JSchException ex) {
                ex.printStackTrace();
                System.out.println(ex.getMessage());
            } catch (IllegalAccessException ex) {
                ex.printStackTrace();
                System.out.println(ex.getMessage());
            } catch (IOException ex) {
                ex.printStackTrace();
                System.out.println(ex.getMessage());
            }
        }
    }
    ```
