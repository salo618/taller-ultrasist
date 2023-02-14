# Clase 10/02/2023 #

## Resumen ##

## Modificador abstract

Clase abstracta :

- Se utilizan sólo como super clases.
- No se pueden instanciar objetos.
- Sirve para proporcioner una super clase apropiada apartir de la cual heredan otras clases.

## Sobre escritura ##

La sobreescritura en Java también es conocida con el nombre de polimorfismo de inclusión y no es otra cosa que una característica que permite a las clases secundarias o subclases hacer una implementación de un método que ha sido dado por una clase principal o superclase.

Ejemplo de sobre escritura en Java

public class Coche{
   
   //Atributos
   
   String marca;
   
   int año;

   //Métodos
   
   //Método Constructor
   
   public Coche(String marca){
       this.marca = marca;
   }

   // Método Constructor Sobrecargado
   
   public Coche(String marca, int año){
   this.marca = marca;
   this.año = año;
   }

    
Para que funcione adecuadamente, la sobreescritura de métodos en Java debe cumplir con las siguientes condiciones:

- El método debe tener el mismo nombre tanto en la clase principal como en la clase hija o subclase.
- Tanto la lista de parámetros como el tipo de valor devuelto, deben ser iguales en ambas clases (principal y subclase).
- Es imprescindible que haya una clase principal donde se declare el método y una clase hija que también lo implemente, es decir, es necesaria una relación de herencia.
- Cada uno de los métodos que son declarados como abstractos en la clase principal, deben ser sobreescritos en la clase hija.
- Si los métodos se declaran como estáticos, no se pueden sobreescribir.

## Sobrecarga de Metodos ##

Se le llama sobrecarga de funciones o métodos a la creación de varias funciones dentro de nuestro programa, que tienen el mismo nombre, pero sus argumentos son distintos y realizan distinta acción.

Básicamente sobrecargar significa definir nuevos métodos con parámetros distintos para ampliar las funcionalidades del método original, manteniendo la calidad en el código, reutilizando las funciones, sin extender la cantidad de líneas en nuestro programa.

Ejemplo de sobrecarga de métodos en Java

class Empleado {  //clase general
    public static int base = 400;
    int salario() {
        return base;
    }
}

class Gerente extends Empleado { //aquí estamos sobreescribiendo el método de la clase principal
    @Override
    int salario() {
        return base + 200;
    }
}

class Supervisor extends Empleado {
    @Override
    int salario() {
        return base + 100;
    }
}

class Main { // con esto vamos a imprimir el salario de cualquier trabajador
static void imprimirSalario(Empleado Empleado) {
        System.out.println(Empleado.salario());
	 public static void main(String[] args) {
	  Empleado Gerente = new Gerente();
        System.out.println("El salario del gerente es: ");
        imprimirSalario(Gerente);
	Empleado Supervisor = new Supervisor();
        System.out.println("El salario del supervisor es: ");
        imprimirSalario(Supervisor);
	Empleado Empleado1 = new Empleado();
        System.out.println("El salario del empleado es: ");
        imprimirSalario(Empleado1);
	}
}
   

## Metodo super ##

Esta palabra super se utiliza en el lenguaje Java para invocar al método constructor de una clase superior (clase padre) de la cual queremos utilizar el mismo tipo de parametrización, entonces esta palabrita sube de categoría y pasa a ser el método super().

Habrás notado que en el título se hace referencia al “_método super_” y no a una palabra reservada en sí, esto puede resultar confuso.

La palabra reservada super acompañada del nombre del método al que quiere invocar, tiene un uso especial y es el método super().

El método super nos permite reutilizar bloques de código sin tener que volver a escribir lo mismo, invocando al constructor de una clase superior, desde una clase hija y hacia una clase padre.

Cuando queremos acceder a los atributos y/o métodos de una clase superior, utilizamos la herencia (una clase hija “hereda” de una clase padre sus atributos y métodos), y creamos una nueva clase que es extendida de la clase principal, cuya primera línea del constructor debe ser siempre el método super().

Es muy importante el uso del método super(), ya que así evitamos la ambigüedad que puede generarle a la JVM (Java Virtual Machine) que una clase derivada y una clase base utilicen un método con el mismo nombre pero con distinta funcionalidad.

Con la palabra super hacemos referencia a su clase padre. 

Además podemos usar la palabra super para inicializar atributos de la clase superior de la que se extiende con la palabra extends.

Las clases hijas pueden sobreescribir métodos de las clases padre y luego invocarlos con la cláusula super.

Ejemplo de método super en Java



## this ##

Cuando se efectúa un llamado un método, se pasa en forma automática un argumento implícito que es una referencia al objeto invocado. A esta referencia se la conocen en Java como this. 

En el siguiente ejemplo se puede ver a this en un programa.

package mx.qbits.ejemplo4;

class Forma extends Poligono{
      private double base;
      private double altura;

   public Forma(double base, double altura) {
	   super(3);
	   this.base = base;
	   this.altura = altura;
	   
   }
   public double AreaCalculada() {
	   return (base*altura) / 2;
   }
}

## Duda 1 ##

al realizar el ejercicio de los poligonos me arroja un error de sintaxis en Forma2

![image](https://user-images.githubusercontent.com/123017277/218380624-68810c98-f09e-4f89-8f7b-38567627025e.png)

Pero aun con el  error el programa compila y funciona bien 

![image](https://user-images.githubusercontent.com/123017277/218381757-33522198-5676-4e19-b2a5-9ba85a74ab72.png)

busque en algunas paginas en internet el error pero no me convencieron las respuestas o no las entendi

![image](https://user-images.githubusercontent.com/123017277/218384900-01fa2233-2ada-40f7-97fc-60b960384f2f.png)

## Duda 2 ##

En el ejercicio de Persona arrojaba este error en al solicitar la variable nombre.

![image](https://user-images.githubusercontent.com/123017277/218396948-505e79a6-6895-41ab-8558-9a31d1825fed.png)

investigue en alguna paginas de internet y daban como solucion agregar un metodo get lo aplique al proyecto y si se soluciono aunque este privado.

![image](https://user-images.githubusercontent.com/123017277/218397770-5b6560ad-80e7-4ef2-81af-b1651c795f5c.png)
