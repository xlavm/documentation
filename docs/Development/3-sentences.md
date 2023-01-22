# Sentences

=== "JAVA"

    - If y Else

    ```JAVA
    int numero1 = 1, numero2 = 2;
    if (numero1 > numero2){
        System.out.println("el numero mayor es: "+ numero1);
    }else {
        System.out.println("el numero mayor es: "+ numero2);
    }
    //output: el numero mayor es: 2
    ```

    - If Ternario

    ```JAVA
    int numero1 = 1, numero2 = 2;
    String resultado = (numero1 > numero2)? ("el numero mayor es: "+ numero1) : ("el numero mayor es: "+ numero2);
    System.out.println(resultado);
    //output: el numero mayor es: 2
    ```

    - Switch

    ```JAVA
    char op = '-';
    switch (op) {
        case '+':
            System.out.println("ingreso a sumar");
        break ;
        case '-':
            System.out.println("ingreso a restar");
        break;
    }
    // output: ingreso a restar
    ```

=== "JAVASCRIPT"

    - If y Else

    ```JS
    const nota = 4.5
    if(nota > 3){
      console.log('aprobó con: '+ nota)
    }else{
      console.log('reprobó con: '+ nota)
    }
    // output: aprobó con: 4.5
    ```

    - If Ternario

    ```JS
    const nota = 4.5
    console.log((nota > 3)?('aprobó con: '+ nota) : ('reprobó con: '+ nota))
    // output: aprobó con: 4.5
    ```

    - Switch

    ```JS
    const nota = 4.5
    switch(nota){
    case 1.0:
        console.log('mal hecho')
        break
    case 3.0:
        console.log('lo hiciste regular')
        break
    case 4.5:
        console.log('Bien hecho!!!')
        break
    default:
        console.log('no se que decir')
        break
    }
    // output: Bien hecho!!!
    ```

=== "PYTHON"

    - If y Else

    ```PY
    nota = 4.5
    if nota > 3:
        print('aprobó con: ', nota)
    else:
        print('reprobó con: ', nota)
    # output: aprobó con: 4.5
    ```

    - Match

    ```PY
    nota = 4.5
    match nota:
        case 1.0:
            print('mal hecho')
        case 3.0:
            print('lo hiciste regular')
        case 4.5:
            print('Bien hecho!!!')
        case _:
            print('no se que decir')
    # output: Bien hecho!!!
    ```
