# Callbacks

Si hago uso de una funcion como esta:

```JS
app.listen(port){

}
```

Yo podria crear un callback con el fin de que al ejecutarse la funcion, se ejecute tambien otra subfuncion definida asi:

```JS
app.listen(port, () => {
    console.log(`la app esta corriendo en el puerto ${prot}`)
})
```
