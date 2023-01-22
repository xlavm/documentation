# Objects

1. atributos en objetos

    ```JS
    const obj = new Object()

    obj.nombre = 'Luis Vanegas'
    obj['edad'] = 16

    console.log(obj.nombre)
    // output: Luis Vanegas

    console.log(obj['nombre'])
    // output: Luis Vanegas

    console.log(obj.edad)
    // output: 16

    console.log(obj['edad'])
    // output: 16
    ```

2. metodos en objetos

    ```JS
    const obj = new Object()

    obj.sumar = (x, y) => {
        return x + y
    }

    const resultSuma = obj.sumar(1, 10)

    console.log(resultSuma)
    // output: 11
    ```
