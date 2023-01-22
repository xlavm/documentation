# Basics (FALTA)

## Comments

=== "JAVA"

    ```JAVA
    /*
    este es un comentario  complejo para un bloque de codigo (no visible en javadoc)
    */

    //este es un comentario simple para una linea de código

    /**
    * este es un comentario complejo para definición de clases, metodos y atributos
    * (visible en javadoc)
    */
    ```

=== "JAVASCRIPT"

    ```JS
    // comentario de una linea

    /* comentario
    de
    varias lineas */
    ```

=== "PYTHON"

    ```PY
    # comentario de una linea

    """ comentario
    de
    varias lineas """
    ```

## Variables y tipos de datos

=== "JAVA"

    ```JAVA
     //primitivos
     //enteros
     byte diasMes = 31;
     short diasLustro = (12 *31)* 5;
     int velocidadLuz = 299792458;
     long añoLuz = velocidadLuz * 365;
     //decimales
     float pi = 3.1415926535f;
     double e = 2.718281828459045235360;
     //caracteres
     char letraA = 'a';
     char letraANumerico = 61;
     //booleanos
     boolean verdadero = true;
     boolean falso = false;

     //compuestos
     String cadena = 'esta es una cadena';
     int[] arrayNumerico = new int[4];
     int[] arrayNumerico = {2, -4, 15, -25};
     double[][] arrayBidimensional = new double[4][4];
     ArrayList<String> arrayListCadena = new ArrayList<String>();\
     List<String> listaCadena = new ArrayList();

     //especiales
     int vacio = null

     //constantes
     final String constante = 'Luis'
    ```

=== "JAVASCRIPT"

    ```JS
     //primitivos
     const cadena = 'Luis Vanegas'
     const numero = 1
     const booleano = true

     //compuestos
     const obj = new Object()
     const array = new Array()

     //especiales
     const esp1 = null
     const esp2 = undefined

     //variables
     var variable1 = 'cadena'
     let variable2 = 'cadena2'

     //constantes
     const constante1 = 'cadena'
    ```
    **Nota:** usar Let en vez de Var, pero si puedes, usa Const antes que Let porque es mas eficiante, corre mejor y es mas liviana

=== "PYTHON"

    ```PY
     #primitivos
     entero = 1
     flotante = 1.0304
     booleano = True
     cadena = 'esta es una cadena'
     

     #compuestos
     listas = [0,1,2]
     tuplas = ('hola', 7)
     diccionariosOHash = {'clave': 123, 'color': 'rojo'}

     #especiales
     vacio = None

     #constantes
     CONSTANTE = 'Luis'
    ```
    **Nota:** una constante se diferencia de una variable, porque esta es en Mayuscula

## Operadores

=== "JAVA"

    - Relacionales

      ```BASH
      <
      >
      <=
      >=
      !=
      ==
      ```

    - Aritméticos

      ```BASH
      +
      -
      *
      /
      % modulo ej: x=13%5 x=3
      math.pow() exponenciación
      ```

    - Logicos

      ```JAVA
      && and
      || or
      ! not
      ```

    - Asignacion

      ```BASH
      += equivale a x=x+5
      -= equivale a x=x-5
      *= equivale a x=x*5
      /= equivale a x=x/5
      etc..
      ```

=== "JAVASCRIPT"

    - Relacionales

         ```BASH
         <
         >
         <=
         >=
         !=
         ==
         === estrictamente igual "tipos de datos iguales"
         ```

    - Aritméticos

         ```BASH
         +
         -
         *
         /
         % modulo ej: x=13%5 x=3
         math.pow() exponenciación
         ```

    - Logicos

         ```BASH
         &&
         ||
         !
         ```

    - Asignacion

         ```BASH
         += equivale a x=x+5
         -= equivale a x=x-5
         *= equivale a x=x*5
         /= equivale a x=x/5
         etc..
         ```

=== "PYTHON"

    - Relacionales

         ```BASH
         <
         >
         <=
         >=
         !=
         ==
         ```

    - Aritméticos

         ```BASH
         +
         -
         *
         /
         % modulo ej: x=13%5 x=3
         ** potenciacion ej: 12 ** 3 = 1728
         // division con resultado numero entero ej: 18 // 5 = 3
         ```

    - Logicos

         ```PY
         and
         or
         not
         ```

    - Bit a Bit

         ```BASH
         & and
         | or 
         ~ not
         ^ xor
         ```

    - Asignacion

         ```BASH
         += equivale a x=x+5
         -= equivale a x=x-5
         *= equivale a x=x*5
         /= equivale a x=x/5
         &= equivale a x=x&5
         //= equivale a x=x//5
         etc..
         ```

## Forzar cierres (FALTA)

=== "JAVA"

    ```JAVA
    break;
    ```

=== "JAVASCRIPT"

    No Aun

=== "PYTHON"

    No Aun

## Manejo de cadenas

=== "JAVA"

    ```JAVA
     //concatenacion
     String name = "Luis Vanegas"
     System.out.println("Mi nombre es: " + name);
     //output: Mi nombre es: Luis Vanegas

     //cantidad de caracteres
     String cadena = "Esta es una prueba";
     System.out.println(cadena.length());
     //output: 18

     //obtener un caracter
     String cadena = "Polimorfismo"; 
     System.out.println(cadena.charAt(4));
     //output: m

     //obtener sub cadena
     String cadena = "Desarrollo Orientado a Objetos";
     System.out.println(cadena.substring(11,20));
     //output: Orientado

     //eliminar espacios en blancos
     String cadena = "      Programación 1  ";
     System.out.println(cadena.trim());
     //output: Programación 1

     //remplazar caracteres
     String cadena = "mamá";
     System.out.println(cadena.replace('m','p'));
     //output: papá

     //remplazar cadena
     String cadena = "Luis Angel";
     System.out.println(cadena.replaceAll("Angel","Vanegas"));
     //output: Luis Vanegas

     //convertir de Mayus a Minus
     String cadena = "JAVA";
     System.out.println(cadena.toLowerCase());
     //output: java

     //convertir de Minus a Mayus
     String cadena = "java";
     System.out.println(cadena.toUpperCase());
     //output: JAVA

     //comparar cadena
     String cadena1 = "alajuela", cadena2 = "Alajuela";
     System.out.println(cadena1.equals(cadena2));
     //output: false

     //comparar cadena ignorando mayus o minus
     String cadena1 = "alajuela", cadena2 = "Alajuela";
     System.out.println(cadena1.equalsIgnoreCase(cadena2));
     //output: true

     //OTROS METODOS
     //bolean isLetter(char caracter)) 
     //Retorna un verdadero si el carácter del parámetro es una letra

     //bolean isDigit(char caracter)) 
     //Retorna un verdadero si el carácter del parámetro es un dígito

     //bolean isUpperCase(char caracter) 
     //Retorna un verdadero si el carácter del parámetro es una letra mayúscula

     //boolean isLowerCase(char caracter) 
     //Retorna un verdadero si el carácter del parámetro es una letra minúscula
    ```

=== "JAVASCRIPT"

    ```JS
     //templates literales
     const nombre = 'Luis'
     console.log (`La edad de ${nombre} es: 16`)
     // output: La edad de Luis es: 16
    ```

=== "PYTHON"

    ```PY
     #templates literales
     name="Luis"
     age="25"
     print("Hi {name}, you age is {age}".format(name=name, age=age))
     # output: Hi Luis, you age is 25
    ```

## Capturador de Errores (FALTA)

- Try: va el bloque de codigo a evaluar.
- Catch: va el comportamiento que tomará el programa si hay un error.
- Finally: va el bloque de codigo que se ejecutará si hay o no error (siempre se ejecutará).

=== "JAVA"

    - Capturador simple

    ```JAVA
    try {
        System.out.println("Bloque de Codigo a Evaluar");
    }
    catch (Exception e) {
        System.out.println("Instrucciones a ejecutar cuando se produce un error");
    }
    finally {
        System.out.println("Instrucciones a ejecutar tanto si se producen errores como si no.");
    }
    ```

    - Capturador multiple

    ```JAVA
    try {

    }catch( ArithmeticException e ) {
               
    }catch( Exception e ) {
              
    }
    ```

=== "JAVASCRIPT"

    No aun

=== "PYTHON"

    No aun
