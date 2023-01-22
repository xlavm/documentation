# Cycles

=== "JAVA"

    - While

    ```JAVA
    int contador =1; 
    while (contador <= 5 ){
        System.out.println("numero" + contador);
        contador = contador +1;
    }
    //output:numero1 numero2 numero3 numero4 numero5
    ```

    - Do While

    ```JAVA
    import java.util.Scanner;

    public class HolaMundo {
        public static void main(String[] args) {

            Scanner sc = new Scanner(System.in);
            int numero = 0;
            do {
                System.out.println("Ingresa el 0 para ejecutar el ciclo o el 1 para detenerlo");
                numero = sc.nextInt();
                if (numero == 0){
                    System.out.println("El ciclo se ejecutara nuevamente");
                }else if (numero == 1){
                    System.out.println("El ciclo se detendra");
                }else if (numero != 0 && numero != 1){
                    System.out.println("Ingreso un valor no correcto");
                }
            } while ( numero == 0);

        }
    }
    ```

    - For

    ```JAVA
    for (int contador=1; contador <= 5; contador++){
        System.out.println("numero:" +contador);
    }
    //output: numero:1 numero:2 numero:3 numero:4 numero:5
    ```

=== "JAVASCRIPT"

    - While

    ```JS
    var num = 1
    while(num <= 3){
        num++
    }
    console.log('el valor final de num es: '+ num)
    //output: el valor final de num es: 4
    ```

    - Do While

    ```JS
    var num = 1
    do{
        num++
    }while(num <= 3);
    console.log('el valor final de num es: '+ num)
    //output: el valor final de num es: 4
    ```

    - For

    ```JS
    for(var num = 0; num <= 3; num++){
        num++
    }
    console.log('el valor final de num es: '+ num)
    //output: el valor final de num es: 4
    ```

=== "PYTHON"

    - While

    ```PY
    dia = 0    
    semana = ['Lunes', 'Martes']
    while dia < 2:
        print("Hoy es " + semana[dia])
        dia += 1
    #output: Hoy es Lunes Hoy es Martes
    ```

    - For

    ```PY
    nums = [4, 78]
    for n in nums:
        print(n)
    #output: 4 78
    ```
