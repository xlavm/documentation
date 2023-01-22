# Promises

Para crear una promesa se usa `async`, para capturar un error de la promesa `try catch` y para obtener el resultado de la promesa, se usa `.then` y para el error `.catch`

```JS
const obtenerMultiplicacion = async(base = 5) => {
    try {
        let salida = ''

        for(let i = 1; i <= 10; i++){
            salida += `${ base } x ${ i } = ${ base * i }\n`
        }

        return salida

    } catch (error) {
        throw error
    }
}

const base = 7

obtenerMultiplicacion(base)
    .then(resultSalida => console.log(resultSalida))
    .catch (err => console.log(err))
```

La funcion `obtenerMultiplicacion()` seria una funcion promesa