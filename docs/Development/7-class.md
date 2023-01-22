# Class (FALTA)

## Clases, Atributos y Funciones (FALTA)

=== "JAVA"

    - Clase

    ```JAVA
    public class MyClass{
  
    }
    ```

    - Clase con atributos

    ```JAVA
    public class MyClass{
      public String nombre = "Luis";
      private String apellido = "Vanegas";
      protected int edad = 25;
    }
    ```

    - Clase con funciones

    ```JAVA
    public class MyClass{
      //funcion que retorna un valor entero
      public int sumar(int num1, int num2){
        return (num1 + num2);
      }
      //funcion que retorna NO retorna valor
      public void mensaje(){
        System.out.println("esta es una funcion sin retorno");
      }
      //funcion principal
      public static void main(String[] args) {
        MyClass miClase = new MyClass();
        System.out.println("el resultado de la suma es: " + miClase.sumar(1, 2));
        miClase.mensaje();
      }
    }
    ```

=== "JAVASCRIPT"

    - Funciones de Flecha

    Es recomendable usar funciones de flecha

    ```JS
    //funcion tradicional
    function sumar(a, b){
      return a + b 
    }
    //funcion de flecha
    const sumar = (a, b) => {
      return a + b
    }
    //funcion de flecha abreviada
    const sumar = (a, b) => a + b
    ```

=== "PYTHON"

    - Clase

    ```PY
    class myClass():
    ```

    - Clase con atributo

    ```PY
    class myClass():
        x=1

    #mostrar valor del atributo
    clase = myClass()
    print(clase.x)
    #output: 1

    #modificar valor del atributo
    myClass.x = 'Luis Vanegas'
    print(myClass.x)
    #output: Luis Vanegas
    ```

    - Clase con funciones

    ```PY
    class Person:
        def __init__(self, name, age):
            self.name = name
            self.age = age

        def myfunc(self):
            print("Hola mi nombre es: " + self.name)

    p1 = Person("Luis", 25)
    p1.myfunc()
    #output: Hola mi nombre es:
    ```
