### Curso de Fundamentos de Java 🚀

#### Módulo 1: Introducción a Java 🌟
1. **Historia y Características de Java**
   - Historia del lenguaje Java
   - Características principales de Java
   ```java
   // Tu primer programa en Java
   public class HolaMundo {
       public static void main(String[] args) {
           // Imprime "¡Hola, Mundo!" en la consola
           System.out.println("¡Hola, Mundo!");
       }
   }
   ```
2. **Configuración del Entorno de Desarrollo**
   - Instalación de JDK y configuración de entorno
   - Introducción a IDEs populares: IntelliJ IDEA, Eclipse, NetBeans
   - Creación de un proyecto Java

#### Módulo 2: Sintaxis Básica y Estructuras de Control 📝
1. **Declaración de Variables y Tipos de Datos**
   - Tipos de datos primitivos: int, float, double, char, boolean
   - Declaración y inicialización de variables
   ```java
   int edad = 25; // Declara una variable entera y la inicializa a 25
   double salario = 55000.75; // Declara una variable double y la inicializa a 55000.75
   char inicial = 'A'; // Declara una variable char y la inicializa a 'A'
   boolean esEstudiante = true; // Declara una variable boolean y la inicializa a true
   ```
2. **Operadores**
   - Operadores aritméticos, relacionales y lógicos
   - Operadores de asignación y bit a bit
   ```java
   int suma = 5 + 3; // Suma de dos números, resultado: 8
   boolean esMayor = 10 > 5; // Comparación, resultado: true
   boolean resultado = (5 > 3) && (2 < 4); // Evaluación lógica, resultado: true
   ```
3. **Estructuras de Control**
   - Sentencias condicionales: if, if-else, switch
   - Bucles: for, while, do-while
   ```java
   // Estructura if-else
   int numero = 10;
   if (numero > 0) {
       System.out.println("El número es positivo");
   } else {
       System.out.println("El número es negativo");
   }

   // Bucle for
   for (int i = 0; i < 5; i++) {
       // Imprime el valor de i en cada iteración
       System.out.println("Iteración: " + i);
   }
   ```

#### Módulo 3: Métodos y Funciones 🔍
1. **Declaración de Métodos**
   - Definición y llamada a métodos
   - Parámetros y valores de retorno
   ```java
   public class Calculadora {
       // Método que suma dos enteros y devuelve el resultado
       public int sumar(int a, int b) {
           return a + b;
       }

       public static void main(String[] args) {
           Calculadora calc = new Calculadora();
           // Llama al método sumar y almacena el resultado en una variable
           int resultado = calc.sumar(5, 3);
           // Imprime el resultado de la suma
           System.out.println("La suma es: " + resultado);
       }
   }
   ```
2. **Sobrecarga de Métodos**
   - Concepto de sobrecarga
   - Ejemplos prácticos
   ```java
   public class Calculadora {
       // Método que suma dos enteros
       public int sumar(int a, int b) {
           return a + b;
       }

       // Método que suma dos doubles
       public double sumar(double a, double b) {
           return a + b;
       }
   }
   ```

#### Módulo 4: Programación Orientada a Objetos (POO) 🏛️
1. **Clases y Objetos**
   - Definición de clases y creación de objetos
   - Constructores y sobrecarga de constructores
   ```java
   public class Persona {
       String nombre;
       int edad;

       // Constructor que inicializa los atributos nombre y edad
       public Persona(String nombre, int edad) {
           this.nombre = nombre;
           this.edad = edad;
       }

       // Método que muestra la información de la persona
       public void mostrarInfo() {
           System.out.println("Nombre: " + nombre + ", Edad: " + edad);
       }

       public static void main(String[] args) {
           // Crea un objeto Persona y llama al método mostrarInfo
           Persona persona = new Persona("Juan", 30);
           persona.mostrarInfo();
       }
   }
   ```
2. **Encapsulamiento**
   - Modificadores de acceso: private, public, protected
   - Getters y setters
   ```java
   public class CuentaBancaria {
       private double saldo;

       // Método getter para obtener el saldo
       public double getSaldo() {
           return saldo;
       }

       // Método para depositar dinero en la cuenta
       public void depositar(double cantidad) {
           if (cantidad > 0) {
               saldo += cantidad;
           }
       }
   }
   ```
3. **Herencia**
   - Concepto de herencia
   - Uso de la palabra clave `extends`
   ```java
   public class Animal {
       public void hacerSonido() {
           // Método base para hacer un sonido
           System.out.println("El animal hace un sonido");
       }
   }

   public class Perro extends Animal {
       // Método sobrescrito para hacer un sonido específico de perro
       public void hacerSonido() {
           System.out.println("El perro ladra");
       }

       public static void main(String[] args) {
           Perro miPerro = new Perro();
           // Llama al método hacerSonido de la clase Perro
           miPerro.hacerSonido();
       }
   }
   ```
4. **Polimorfismo**
   - Sobrescritura de métodos
   - Interfaces y clases abstractas
   ```java
   interface Animal {
       void hacerSonido(); // Método abstracto que debe ser implementado por las clases que implementen la interfaz
   }

   class Perro implements Animal {
       // Implementación del método hacerSonido para la clase Perro
       public void hacerSonido() {
           System.out.println("Guau guau");
       }
   }

   public class Main {
       public static void main(String[] args) {
           Animal miPerro = new Perro();
           // Llama al método hacerSonido de la interfaz Animal, implementado por la clase Perro
           miPerro.hacerSonido();
       }
   }
   ```

#### Módulo 5: Wrappers y Tipos de Datos 📦
1. **Clases Wrapper**
   - Uso de clases wrapper para tipos de datos primitivos (Integer, Double, Boolean, etc.)
   - Autoboxing y Unboxing
   ```java
   Integer numero = 10; // Autoboxing: convierte el int 10 a Integer
   int valor = numero;  // Unboxing: convierte el Integer numero a int
   ```
2. **Conversiones entre tipos de datos**
   - Conversión explícita e implícita
   - Métodos de conversión de clases wrapper
   ```java
   String numeroStr = "123";
   int numeroInt = Integer.parseInt(numeroStr); // Convierte el String a int
   ```

#### Módulo 6: Manejo de Excepciones ⚠️
1. **Introducción a Excepciones**
   - Concepto de excepciones
   - Tipos de excepciones: checked y unchecked
2. **Manejo de Excepciones**
   - Uso de try, catch y finally
   - Creación de excepciones personalizadas
   ```java
   public class EjemploExcepciones {
       public static void main(String[] args) {
           try {
               // Intenta dividir por cero
               int division = 10 / 0;
           } catch (ArithmeticException e) {
               // Captura la excepción y muestra un mensaje
               System.out.println("Error: División por cero");
           } finally {
               // Este bloque siempre se ejecuta
               System.out.println("Bloque finally ejecutado");
           }
       }
   }
   ```

#### Módulo 7: Colecciones y Generics 📚
1. **Colecciones en Java**
   - Listas, Conjuntos y Mapas
   - Iteración sobre colecciones
   ```java
   import java.util.ArrayList;

   public class EjemploColecciones {
       public static void main(String[] args) {
           // Crea una lista de Strings
           ArrayList<String> lista = new ArrayList<>();
           lista.add("Manzana");
           lista.add("Banana");
           lista.add("Cereza");

           // Itera sobre la lista e imprime cada elemento
           for (String fruta : lista) {
               System.out.println(fruta);
           }
       }
   }
   ```
2. **Generics**
   - Uso de generics en colecciones
   - Creación de clases genéricas
   ```java
   public class Caja<T> {
       private T contenido;

       // Método para guardar un objeto en la caja
       public void guardar(T contenido) {
           this.contenido = contenido;
       }

       // Método para obtener el objeto de la caja
       public T obtener() {
           return contenido;
       }



```java
       public static void main(String[] args) {
           Caja<String> cajaDeString = new Caja<>();
           // Guarda un String en la caja
           cajaDeString.guardar("Hola Mundo");
           // Imprime el contenido de la caja
           System.out.println(cajaDeString.obtener());
       }
   }
   ```
   
¡Espero que este curso te sea de gran ayuda para comenzar tu viaje en el desarrollo con Java! 🚀
