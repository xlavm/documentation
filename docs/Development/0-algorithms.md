# Algorithms

Un algoritmo ​ es un conjunto de instrucciones o reglas definidas y no-ambiguas, ordenadas y finitas que permite, típicamente, solucionar un problema, realizar un cómputo, procesar datos y llevar a cabo otras tareas o actividades.​

![algoritmo](https://upload.wikimedia.org/wikipedia/commons/b/bd/LampFlowchart-es.svg)

## Diagrama de Flujo

Es una de las formas de representar un algoritmo y du simbologia puede variar.

![smbologia](https://static.platzi.com/media/user_upload/simbolos-diagrama-de-flujo-a942a526-219e-44cf-b5d3-d4d1069b3c30.jpg)

## Pseudocodigo

Es otra forma de representar un algoritmo pero esta por medio de un lenguaje natural. Un ejemplo de este es:

```JAVA
Algoritmo resta
    Leer numero1, numero2
    resultado<-numero1 - numero2
    Escribir resultado
FinAlgoritmo
```

## PSeint

Este es un programa que permite representar algoritmos en forma de Diagramas de flujos y Pseudocodigo. Este lo puedes descargar en: <https://pseint.sourceforge.net/?page=descargas.php>

## Ejercicios

Estos ejercicios son creados con PSeint y para importarlos en PSeint basta con crear un archivo de extension `.psc` y pegar dentro cada codigo, luego vas a PSeint y lo importas

=== "EJERCICIO 1"

    Crea un programa que sume 2 numeros e imprima su resultado por pantalla.

    Te tienes que preguntar:

    - Que me dan?
    - Que me piden?
    - Que debo de dar?

    Como respuestas, me dan 2 numeros y me piden que los sume y luego que de el resultado.

    ```JAVA
    Algoritmo suma
        Leer numero1, numero2
        resultado<-numero1 + numero2
        Escribir resultado
    FinAlgoritmo
    ```

=== "EJERCICIO 2"

    En un almacén se quiere realizar un descuento del 10% a los clientes cuya compra sea mayor a 50.000, cree un programa que genere el valor total a pagar de acuerdo a la política establecida para el descuento.

    ```JAVA
    Algoritmo descuento
        Leer valorCompra
        Si valorCompra>50000 Entonces
            valorDescuento <- valorCompra*0.10
            valorTotal <- valorCompra-valorDescuento
        SiNo
            valorTotal <- valorCompra
        FinSi
        Escribir valorTotal
    FinAlgoritmo
    ```

=== "EJERCICIO 3"

    Una empresa quiere verificar que sus colaboradores usen el uniforme adecuado según el día que toque. Por ejemplo, si es Lunes tienen que ir con el uniforme azul y si es miercoles, tienen que ir con el uniforme amarillo, de lo contrario no se les puede dar el acceso a la empresa. Para esto te han buscado con el fin de que crees un programa que valide el uniforme del colaborador según el día y que muestre por pantalla si el acceso es aceptado o denegado.
    Debes tener en cuenta que la empresa solo trabaja de lunes a viernes y de acuerdo a los siguientes días se usa un color de uniforme específico:

    - lunes: marron
    - martes: blanco
    - miercoles: marron
    - jueves: verde
    - viernes: marron

    ```JAVA
    Algoritmo Color_de_uniforme
        Leer dia,uniforme
        Segun dia  Hacer
            'lunes':
                Si uniforme='marron' Entonces
                    Escribir 'acceso aceptado'
                SiNo
                    Escribir 'acceso denegado'
                FinSi
            'martes':
                Si uniforme='blanco' Entonces
                    Escribir 'acceso aceptado'
                SiNo
                    Escribir 'acceso denegado'
                FinSi
            'miercoles':
                Si uniforme='marron' Entonces
                    Escribir 'acceso aceptado'
                SiNo
                    Escribir 'acceso denegado'
                FinSi
            'jueves':
                Si uniforme='verde' Entonces
                    Escribir 'acceso aceptado'
                SiNo
                    Escribir 'acceso denegado'
                FinSi
            'viernes':
                Si uniforme='marron' Entonces
                    Escribir 'acceso aceptado'
                SiNo
                    Escribir 'acceso denegado'
                FinSi
            De Otro Modo:
                Escribir 'ingreso un dia no valido'
        FinSegun
    FinAlgoritmo
    ```

    El algoritmo anterior se puede optimizar asi:

    ```JAVA
    Algoritmo Color_de_uniforme_OPTIMIZADO
        Leer dia,uniforme
        Segun dia  Hacer
            'lunes':
                uniformeEsperado <- 'marron'
            'martes':
                uniformeEsperado <- 'blanco'
            'miercoles':
                uniformeEsperado <- 'marron'
            'jueves':
                uniformeEsperado <- 'verde'
            'viernes':
                uniformeEsperado <- 'marron'
            De Otro Modo:
                Escribir 'ingreso un dia no valido'
        FinSegun
        Si uniforme<>uniformeEsperado Entonces
            Escribir 'acceso denegado'
        SiNo
            Escribir 'acceso aceptado'
        FinSi
    FinAlgoritmo
    ```
