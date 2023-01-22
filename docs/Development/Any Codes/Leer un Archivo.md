# Leer un Archivo

Lee el archivo, lo recorre, lo agrega en una lista y lo muestra por pantalla en un textbox

    ```JAVA
    //#LEER UN ARCHIVO
    BufferedReader archivo = new BufferedReader(new FileReader(/ruta/local/archivo.txt));
    ArrayList<String> lista = new ArrayList<String>();//lista donde se agregará linea a linea del archivo
    String Linea;
    String mostrarArchivo = "";
    while ((Linea = archivo.readLine()) != null) {
        lista.add(Linea);//se agrega la linea leida del archivo
        mostrarArchivo = mostrarArchivo + Linea + "\n";
    }
    txtTextArea.setText(mostrarArchivo);
    archivo.close();
    ```
