# Javadoc

1. Javadocs Tags

    - @author: Nombre del desarrollador.
    - @deprecated: Indica que el método o clase es obsoleto (propio de versiones anteriores) y que no se recomienda su uso.
    - @param: Definición de un parámetro de un método, es requerido para todos los parámetros del método.
    - @return: Informa de lo que devuelve el método, no se aplica en constructores o métodos "void".
    - @see: Asocia con otro método o clase.
    - @version: Versión del método o clase.
    - @since: Versión de la aplicativo

2. Ejemplo de clase para Javadoc

    ```JAVA
    /**
     * Clase NodoDoble,
     * moldea la estructura de un nodo con doble liga (izquierda y derecha)
     * @author Luis Angel Vanegas Martinez
     * @version 28/09/2017
     * @since 1.0
     */
    public class javadoc {
        /**
         * Atributos,
         * - dato: hace referencia al info del nodo doble y es de tipo cadena.
         * - ligaDer: hace referencia a la liga derecha del nodo doble y es de tipo NodoDoble.
         * - ligaIzq: hace referencia a la liga izquierda del nodo doble y es de tipo NodoDoble.
         */
        private String dato ;
        private javadoc ligaDer;
        /**
         * metodo Constructor de la clase,
         * este metodo almacena el dato obtenido y crea una liga izq y liga der y las 
         * asigna nulas.
         * @param pdato -dato obtenido una vez se cree un nuevo NodoDoble.
         */
        public javadoc (String pdato){
            dato=pdato;
            ligaDer= null;
        }
        /**
         * metodo AsignaLigaDer,
         * modifica la liga derecha del nodo doble, asignandole el valor que recibe.
         * @param pLigaDer -valor de la liga Derecha, recibido por parametro.
         */
        public void AsignaLigaDer(javadoc pLigaDer){
            ligaDer = pLigaDer;
        }
        /**
         * metodo RetornaLigaDer,
         * @return -retorna la lida derecha del nodo doble.
         */
        public javadoc RetornaLigaDer(){
            return ligaDer;
        }
        /**
         * metodo RetornaDato,
         * @return -retorna el dato que contiene el nodo doble en su info.
         */
        public String RetornaDato(){
            return dato;
        }
    }
    ```
