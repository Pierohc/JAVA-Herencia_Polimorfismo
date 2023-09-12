## Herencia:
- Existirá una clase padre.
- La clase hija herede los atributos y metodos de la clase padre
- Si los atributos estan privados se accede mediante getter and setter, para acceder a ellos:
- Para los metodos no es necesario ya que estan en publico normalmente en la clase Padre.

Clase Hija:

    sout("Fabricante" + getFabricante());
    sout("Fabricante" + this.getFabricante());


# Para heredar:

    public class ClaseHija extends ClasePadre{

# Se pueden pasar pedidos de datos:
clase Padre:

      public void registrarDatos(Scanner scanner){
        sout("Ingrese el fabricante:" );
        fabricante = scanner.nextLine();
         o 
        sout("Ingrese el fabricante:" );
        this.setFabricante(scanner.nextLine());
        
-----------------
# Si en la clase padre e hija hay métodos con el mismo nombre:
Clase Padre:

    public void imprimirEspecificaiones(){
        //pide fabricante, modelo, color // atributos comunes que tendran otras clases

Clase Hija:

    public void imprimirEspecificaciones(){
       //pide pulgadas(pantalla) 

Necesitamos pedir en la clase Hija los otros datos que estan en la clase padre. Solución (`super`):

Clase Hija:

    public void imprimirEspecificaciones(){
            super.imprimirEspecificaciones();
           //pide pulgadas(pantalla)

# Si no se llamada a super y en el main se llama a la funcion que tiene el mismo nombre en la clase Padre:

    monitor.imprimirEspecificaciones()
Este se referirá a la clase que se encuentre en el Hijo(Monitor).

--------------------
# No se pueden borrar metodos de la clase Padre pero si modificar su comportamiento:
Cuando se imprime un objeto, se imprime su posicion de memoria e implicitamente Java llamada a la función `toString`
Pasos:
- Clic derecho en un espacio en blanco.
- Overwrite Methods
- Elegimos toString, en este caso la clasePadre herede de Object

      public String toString(){
        return "hola"  //ya no imprimira la pos de memoria, sino un hola
      }
- Estos significa que solo afectara al `toString` de la clase Padre y de los Hijos que la heredan.
Si aun quiero imprimir la pos de memoria:

       public String toString(){
              String posMemoria = super.toString(); //dispositivo@12443533;
              return "hola"  //
            }

------------------------
# Clase Object:

-Todas las clases heredan de Object




 
