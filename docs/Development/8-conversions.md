# Conversions (FALTA)

## Convertir de Cualquier ... a String

=== "JAVA"

    ```JAVA
    //integer a String
    Integer.toString(entero);
    // o
    String cadena = String.valueOf(entero);

    //char a String
    String cadena = Character.toString(char);

    //double a String
    String cadena = String.valueOf(doble);

    //float a String
    String cadena = Float.toString(flotante);

    //boolean a String
    String cadena = String.valueOf(boolean);
    // o
    String cadena = Boolean.toString(boolean);
    ```

=== "JAVASCRIPT"

    No Aun

=== "PYTHON"

    No Aun

## Convertir de String a ... Cualquier

=== "JAVA"

    ```JAVA
    //String a integer
    int entero = Integer.valueOf(cadena);
    // o
    int entero = Integer.parseInt(cadena);

    //String a char
    char caracter = cadena.charAt(0); //Solo primer carácter

    //String a double
    double doble = Double.parseDouble(cadena);

    //String a float
    float flotante = Float.parseFloat(cadena);

    //String a boolean
    Boolean booleano = Boolean.valueOf(cadena);
    // o
    boolean booleano = Boolean.parseBoolean(cadena);
    ```

=== "JAVASCRIPT"

    No Aun

=== "PYTHON"

    No Aun
