# Arrays (FALTA)

## Declarar, inicializar y listar valores

=== "JAVA"

    - Array

    ```JAVA
    //declarar
    int[] numero = new int[4];
    //declarar e inicializar
    int[] numero = {2, -4, 15, -25};

    //listar
    for (int i=0; i < numero.length; i++){
        System.out.println(numero[i]);
    }
    //output: 2 -4 15 -25
    ```

    - ArrayList

    Se debe importar las siguientes librerias:

    ```JAVA
    import java.util.ArrayList;
    import java.util.Iterator;
    ```

    ```JAVA
    //declarar
    ArrayList<String> nombreArrayList = new ArrayList<String>();

    //agregamos elemento
    nombreArrayList.add("Elemento Nuevo");

    //listar
    // declaramos el Iterador e imprimimos los Elementos del ArrayList
    Iterator<String> nombreIterator = nombreArrayList.iterator();
    while(nombreIterator.hasNext()){
        String elemento = nombreIterator.next();
        System.out.print(elemento);
    }  
    //output: Elemento Nuevo
    ```

=== "JAVASCRIPT"

    ```JS
    //declarar e inicializar
    const array1 = [1,2,3,4,5]
    const array2 = new Array(5,4,3,2,1)

    //listar
    console.log(`Array 1: ${array1}`)
    //output: array1: 1,2,3,4,5
    console.log(array1.toString())
    //output: array1: 1,2,3,4,5
    for(let i=0; i < array1.length; i++){
        console.log(array1[i])
    }
    //output: 1 2 3 4 5
    ```

=== "PYTHON"

    ```PY
    #declarar e inicializar
    miArray = ['valor1', 2, True]

    #listar
    print(miArray)
    #output: ['valor1', 2 , True]
    print('valor de posición 2 de miArray es: ', miArray[2])
    #output: valor de posición 2 de miArray es:  True
    for valor in miArray:
    print(valor)
    #output: valor1 2 True 
    ```

## Modificar valor

=== "JAVA"

    - Array

    ```JAVA
    int[] numero = {2, -4, 15, -25};
    numero[3] = 500;
    System.out.println(numero[3]);
    //output: 500
    ```

    - ArrayList

    ```JAVA
    ArrayList<String> nombreArrayList = new ArrayList<String>();
    nombreArrayList.add("Elemento Nuevo");
    nombreArrayList.set(0, "Elemento Modificado")
    //output: Elemento Modificado
    ```

=== "JAVASCRIPT"

    ```JS
    const array1 = [1,2,3,4,5]
    array1[4] = 500
    console.log(`el nuevo valor de la posición 4 de array1 es: ${array1[4]}`)
    //output: el nuevo valor de la posición 4 de array1 es: 500
    ```

=== "PYTHON"

    ```PY
    miArray = ['valor1', 2, True]
    miArray[0] = 'nuevo valor'
    print(miArray)
    #output: ['nuevo valor', 2, True]
    ```

## Insertar valor

=== "JAVA"

    - ArrayList

    ```JAVA
    // Añade el elemento al ArrayList
    nombreArrayList.add("Elemento");
    // Añade el elemento al ArrayList en la posición 'n'
    nombreArrayList.add(0, "Elemento 2");
    ```

=== "JAVASCRIPT"

    ```JS
    const array = ['a','b','c',]
    array.push('d')
    console.log(array)
    //output: ["a","b","c","d"]
    ```

=== "PYTHON"

    ```PY
    miArray = ['valor1', 2, True]
    miArray.append('nuevo valor')
    print(miArray)
    #output: ['valor1', 2, True, 'nuevo valor']
    miArray.insert(2,'valor en 2')
    print(miArray)
    #output: ['valor1', 2, 'valor en 2', True, 'nuevo valor']
    ```

## Eliminar valor

=== "JAVA"

    - ArrayList

    ```JAVA
    // Borra el elemento de la posición '5' del ArrayList   
    nombreArrayList.remove(5); 
    // Borra la primera ocurrencia del 'Elemento' que se le pasa como parametro.  
    nombreArrayList.remove("Elemento");
    //Borra todos los elementos de ArrayList   
    nombreArrayList.clear();
    ```

=== "JAVASCRIPT"

    ```JS
    const array = ['a','b','c',]
    array.pop()
    console.log(array)
    //output: ["a","b"]
    ```

=== "PYTHON"

    ```PY
    miArray = ['valor1', 2, True]
    miArray.remove('valor1')
    print(miArray)
    #output: [2, True]
    del miArray[0]
    print(miArray)
    #output: [True]
    ```

## Multidimensional Arrays (FALTA)

=== "JAVA"

    ```JAVA
    //declarar e inicializar
    double[][] arrayBi={{1,2,3},{4,5,6}};

    //listar
    for (int i=0; i < arrayBi.length; i++) {//filas
        for (int j=0; j < arrayBi[i].length; j++) {//columnas
            System.out.print(arrayBi[i][j]+"\t");
        }
        System.out.println("");
    }

    //agregar
    for (int i=0; i < arrayBi.length; i++) {//filas
        for (int j=0; j < arrayBi[i].length; j++) {//columnas
            if (i==1 && j==1){
                arrayBi[i][j] = 500; //agregamos en la fila i columna j
            }
        }
    }
    ```

=== "JAVASCRIPT"

    ```JS
    //declarar e inicializar
    const arrayBi = [[1,2,3],[4,5,6]]
    console.log(arrayBi[0][2])
    //output: 3
    console.log(arrayBi[1][2])
    //output: 6
    ```

=== "PYTHON"

    ```PY
    #declarar e inicializar
    miArrayBi = [[1,2,3],[4,5,6]]
    print(miArrayBi[0][2])
    #output: 3
    print(miArrayBi[1][2])
    #output: 6
    ```

## Otras funciones de ArrayList en Java

- Devolver valores

```JAVA
 // Devuelve el elemento que esta en la posición '2' del ArrayList
 nombreArrayList.get(2);
 // Devuelve la posición de la primera ocurrencia ('Elemento') en el ArrayList  
 nombreArrayList.indexOf("Elemento");
 // Devuelve la posición de la última ocurrencia ('Elemento') en el ArrayList
 nombreArrayList.lastIndexOf("Elemento");
 // Devuelve el numero de elementos del ArrayList
 nombreArrayList.size();
 // Devuelve True si el ArrayList esta vacio. Sino Devuelve False   
 nombreArrayList.isEmpty(); 
```

- Otras funciones

```JAVA
 // Comprueba se existe del elemento ('Elemento') que se le pasa como parametro
 nombreArrayList.contains("Elemento");
 // Copiar un ArrayList 
 ArrayList arrayListCopia = (ArrayList) nombreArrayList.clone();  
 // Pasa el ArrayList a un Array 
 Object[] array = nombreArrayList.toArray();
```
