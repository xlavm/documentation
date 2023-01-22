# Executions

## Compilado

El codigo es convertido a un binario que lee el sistema operativo

=== "JAVA"

    Se crea el archivo `HolaMundo.java`

    - HolaMundo.java:

    ```JAVA
    public class HolaMundo {
        public static void main(String[] args) {
            System.out.println("Hola Mundo por Luis Vanegas");
        }
    }
    ```

    Primero se compila el archivo con el comando: `javac HolaMundo.java`

    Luego se ejecuta el archivo con el comando: `java HolaMundo` y obtienes como salida: **Hola Mundo por Luis Vanegas**

=== "JAVASCRIPT"

    Se crean 2 archivos que trabajaran juntos, `index.html` y `script.js`

    - index.html:

    ```HTML
    <!DOCTYPE html>
    <html>
       <head>
           <meta charset="utf-8">
           <title>Javascript</title>
       </head>
       <body>
           Hola Mundo!
           <script> src="script.js"</script>
       </body>
    </html>
    ```

    - script.js:

    ```JS
    alert('Hola Mundo')
    ```
    
    Tambien puede ser Embebido asi:

    Acá el script de js va a estar inmerso en el html

    ```HTML
    <!DOCTYPE html>
    <html>
       <head>
           <meta charset="utf-8">
           <title>Javascript</title>
       </head>
       <body>
           Hola Mundo!
           <script>
               //alert('Hola Mundo')
           </script>
       </body>
    </html>
    ```

=== "PYHTON"

    Se crea el archivo `main.py`

    - main.py:

    ```PY
    print('hola mundo')
    ```

    Si ejecutas el comando `py main.py` obtienes como salida: **hola mundo**

## Interpretado

Requiere de un programa que lea la instruccion de codigo en tiempo real y la ejecute

=== "JAVA"

    Java es un lenguaje 100% compilado, NO interpretado

=== "JAVASCRIPT"

    Puedes ir a las herramientas de desarrollador de tu Browser y luego al menu de consola y escribir codigo Javascript, luego este sera interpretado por el navegador y en vivo ejecutara la accion

=== "PYTHON"

    Puedes ir al command line o consola de python y escribir codigo Python, luego este sera interpretado por la consola y en vivo ejecutara la accion
