# JSON

## Retornar valores de JSON

=== "JAVA"

    **Nota:** Debe tener instalada la libreria `org.json` e importarla en la clase asi: `import org.json.*;`

    - JSON Object

    ```JAVA
    JSONObject obj = new JSONObject();
    obj.put("name", "foo");
    obj.put("num", 100);
    obj.put("balance", 1000.21);
    obj.put("is_vip", true);
    System.out.print(obj);
    /*output:
    {
    "name": " foo ",
    "num": 100,
    "balance": 1000.21,
    "Italia": true
    } 
    */
    ```

    - JSON Array

    ```JAVA
    JSONArray arr = new JSONArray();
    arr.add("foo");
    arr.add(new Integer(100));
    arr.add(new Double(1000.21));
    arr.add(new Boolean(true));
    arr.add(new JSONObject());
    System.out.print(arr);
    /*output:
    [" foo ", 100, 1000.21, true]
    */
    ```

    - Sub JSON

    ```JAVA
    JSONObject obj = new JSONObject();
    obj.put("name", "foo");
    obj.put("num", new Integer(100));
    obj.put("balance", new Double(1000.21));
    obj.put("is_vip", new Boolean(true));
    obj.put("detail", new JSONObject());
    System.out.print(obj);
    /*output:
    {
    "name": " foo ",
    "num": 100,
    "balance": 1000.21,
    "is_vip": true,
    "Detail": { }
    }
    */
    ```

    - Convertir JSON a String

    ```JAVA
    JSONObject obj = new JSONObject();
    arr.add("foo");
    arr.add(new Integer(100));
    arr.add(new Double(1000.21));
    arr.add(new Boolean(true));
    obj.toJSONString()
    System.out.print(obj);
    /*output:
    {
    "name": " foo ",
    "num": 100,
    "balance": 1000.21,
    "Italia": true
    } 
    */
    ```

=== "JAVASCRIPT"

    ```JS
    const usuario = {
        nombre: 'Luis',
        edad: '16',
        skill: ['js', 'java', '.net'],
        perfil: {
            tipo: 'privado',
            cuenta: 'premium'
        }
    } 

    console.log(usuario.nombre)
    //output: Luis
    
    console.log(usuario.skill[0])
    //output: js
   
    console.log(usuario.perfil.cuenta)
    //output: premium

    console.log(usuario)
    //output: { retorna todo el JSON }
    ```

=== "PYTHON"

    ```PY
    usuario = {
    "nombre": 'Luis',
    "edad": 16,
    "skill": ['js', 'java', '.net'],
    "perfil": {
        "tipo": 'privado',
        "cuenta": 'premium'
    }
    } 
    print(usuario["nombre"])
    #output: Luis
    print(usuario["skill"][0])
    #output: js
    print(usuario["perfil"]["cuenta"])
    #output: premium
    print(usuario)
    #output: { retorna todo el JSON }
    ```
