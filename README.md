# _FUNDAMENTOS KOTLIN_ :electron:

![_143a8476-dfa4-4902-9a64-ae53a5e70c76](https://github.com/user-attachments/assets/4d23f31b-a958-42e3-9a46-62b2b5bb772c)


*_Autora: Aura Nicte-Ha Pech Reyes._*


# _SESION 1 ¿QUE ES KOTLIN?_ 💻

#### 1. Declaración de Variables

Declara variables para representar la información de un producto:

* Nombre del producto (String)

* Precio (Double)

* Disponible en inventario (Boolean)

* Código de producto (String) Imprime todas las variables.

```Kotlin
  fun main(){
  val nombreProducto: String = "Laptop Gaming"
  val precio: Double = 1299.99
  val disponible: Boolean = true
  val codigoProducto: String = "LPT-001"

  println("Producto: $nombreProducto")
  println("Precio: $precio")
  println("Disponible: $disponible")
  println("Código: $codigoProducto")
}
```
#### 2. Operaciones Aritméticas
Crea dos variables numéricas y realiza las siguientes operaciones:

* Suma Resta Multiplicación División Módulo Imprime el resultado de cada operación.

```Kotlin
fun main(){
  val num1 = 20
  val num2 = 6

  println("Suma: ${num1 + num2}")
  println("Resta: ${num1 - num2}")
  println("Multiplicación: ${num1 * num2}")
  println("División: ${num1 / num2}")
  println("Módulo: ${num1 % num2}")
}
```
#### 3. Incremento y Decremento
Declara una variable numérica e:

* Incrementa su valor en 1 y muestra el resultado Decrementa su valor en 1 y muestra el resultado:

```Kotlin
fun main(){
  var contador = 5
  println("Incremento: ${++contador}")
  println("Decremento: ${--contador}")
}
```

#### 4. Operadores de Asignación Compuesta

Declara una variable numérica y utiliza operadores de asignación compuesta para:

* Sumar 5 Multiplicar por 2 Restar 3 Dividir entre 4 Muestra el resultado después de cada operación.

```Kotlin
fun main(){
  var numero = 10
  numero += 5
  println("Después de sumar 5: $numero")
  numero *= 2
  println("Después de multiplicar por 2: $numero")
  numero -= 3
  println("Después de restar 3: $numero")
  numero /= 4
  println("Después de dividir entre 4: $numero")
}
```
#### 5. Comparaciones

Declara dos variables numéricas y utiliza operadores de comparación para:

* Verificar si son iguales Verificar si la primera es mayor que la segunda Verificar si la segunda es menor o igual que la primera Muestra el resultado de cada comparación.

```Kotlin
fun main(){
  val a = 15
  val b = 20
  println("a es igual a b: ${a == b}")
  println("a es mayor que b: ${a > b}")
  println("b es menor o igual que a: ${b <= a}")
}
```

#### 6. Operaciones con Strings

Declara dos variables de tipo String y:

* Concaténalas usando el operador + Compara si son iguales Obtén la longitud de ambas y suma los resultados Muestra los resultados.

```Kotlin
fun main(){
  val str1 = "Hola"
  val str2 = "Mundo"
  println("Concatenación: ${str1 + " " + str2}")
  println("Son iguales: ${str1 == str2}")
  println("Suma de longitudes: ${str1.length + str2.length}")
}
```
#### 7. Cálculo de Descuento

* Crea variables para el precio de un producto y el porcentaje de descuento. Calcula el precio final después del descuento. Muestra el precio original, el descuento y el precio final.

```Kotlin
fun main(){
  val precioOriginal = 100.0
  val porcentajeDescuento = 20
  val descuento = precioOriginal * porcentajeDescuento / 100
  val precioFinal = precioOriginal - descuento
  
  println("Precio original: $precioOriginal")
  println("Descuento: $descuento")
  println("Precio final: $precioFinal")
}
```
#### 8. Conversión de Tipos

* Declara una variable de tipo String que contenga un número. Conviértela a Int y luego a Double. Realiza una operación aritmética con cada tipo y muestra los resultados.

```Kotlin
main(){
  val numeroString = "42"
  val numeroInt = numeroString.toInt()
  val numeroDouble = numeroInt.toDouble()
  
  println("Int + 10: ${numeroInt + 10}")
  println("Double + 10.5: ${numeroDouble + 10.5}")

}
```

#### 9. Operaciones Booleanas

* Crea tres variables booleanas y utiliza operadores lógicos (AND, OR, NOT) para combinarlas. Muestra el resultado de al menos tres combinaciones diferentes.

```Kotlin
fun main(){
  val p = true
  val q = false
  val r = true
  
  println("p AND q: ${p && q}")
  println("p OR q: ${p || q}")
  println("NOT p: ${!p}")
  println("(p OR q) AND r: ${(p || q) && r}")
}
```
#### 10. Cálculo de IMC

* Crea variables para el peso (en kg) y la altura (en metros) de una persona. Calcula el Índice de Masa Corporal (IMC) usando la fórmula: IMC = peso / (altura * altura) Muestra el resultado del IMC.

```Kotlin
fun main(){
  val peso = 70.0 // kg
  val altura = 1.75 // metros
  val imc = peso / (altura * altura)
  
  println("IMC: ${"%.2f".format(imc)}")
}
```
# _SESIÓN 2 FUNDAMENTOS DE PROGRAMACIÓN._ 🖱️

#### 1. Calculadora de volumen de cilindro

* Crea una función que calcule el volumen de un cilindro dado su radio y altura.

```Kotlin

fun main(){
import kotlin.math.PI

fun calcularVolumenCilindro(radio: Double, altura: Double): Double {
    return PI * radio * radio * altura
}

fun main() {
    println("Volumen del cilindro: ${calcularVolumenCilindro(5.0, 10.0)}")
}
```

#### 2. Verificador de número primo

* Implementa una función que determine si un número es primo.

```Kotlin

fun esPrimo(numero: Int): Boolean {
    if (numero <= 1) return false
    for (i in 2..Math.sqrt(numero.toDouble()).toInt()) {
        if (numero % i == 0) return false
    }
    return true
}

fun main() {
    println("¿Es 17 primo? ${esPrimo(17)}")
    println("¿Es 24 primo? ${esPrimo(24)}")
}
```

#### 3. Validador de email con función local

* Desarrolla una función que valide una dirección de email utilizando una función local.

```Kotlin
    fun validarEmail(email: String): Boolean {
    fun tieneArrobaYPunto(str: String): Boolean {
        return str.contains("@") && str.contains(".")
    }

    return email.isNotEmpty() && tieneArrobaYPunto(email)
}

fun main() {
    println("¿Es válido user@example.com? ${validarEmail("user@example.com")}")
    println("¿Es válido invalid-email? ${validarEmail("invalid-email")}")
}
```

#### 4. Clasificador de edades usando when

* Crea una función que clasifique a una persona según su edad utilizando when.

```Kotlin
fun clasificarEdad(edad: Int) {
    when (edad) {
        in 0..12 -> println("Niño")
        in 13..19 -> println("Adolescente")
        in 20..64 -> println("Adulto")
        else -> println("Adulto mayor")
    }
}

fun main() {
    clasificarEdad(8)
    clasificarEdad(15)
    clasificarEdad(35)
    clasificarEdad(70)
}
```

#### 5. Imprimir números pares en un rango

* Utiliza un ciclo for para imprimir los números pares en un rango dado.

```Kotlin
fun imprimirPares(inicio: Int, fin: Int) {
    for (i in inicio..fin step 2) {
        if (i % 2 == 0) {
            println(i)
        }
    }
}

fun main() {
    imprimirPares(1, 10)
}
```

#### 6. Contar vocales en una lista de palabras

* Usa una lista y un ciclo para contar las vocales en una lista de palabras.

```Kotlin

fun contarVocales(palabras: List<String>): Int {
    val vocales = setOf('a', 'e', 'i', 'o', 'u')
    var totalVocales = 0
    
    for (palabra in palabras) {
        totalVocales += palabra.lowercase().count { it in vocales }
    }
    
    return totalVocales
}

fun main() {
    val listaPalabras = listOf("Hola", "Mundo", "Kotlin")
    println("Total de vocales: ${contarVocales(listaPalabras)}")
}

```

#### 7. Diccionario de sinónimos

* Crea un mapa de sinónimos y una función para obtener sinónimos de una palabra.


```Kotlin

val sinonimos = mapOf(
    "feliz" to listOf("contento", "alegre", "dichoso"),
    "triste" to listOf("melancólico", "abatido", "apenado"),
    "enojado" to listOf("furioso", "irritado", "colérico")
)

fun obtenerSinonimos(palabra: String): List<String> {
    return sinonimos[palabra.lowercase()] ?: listOf("No se encontraron sinónimos")
}

fun main() {
    println("Sinónimos de 'feliz': ${obtenerSinonimos("feliz")}")
    println("Sinónimos de 'cansado': ${obtenerSinonimos("cansado")}")
}
```


# _SESIÓN 3: PROGRAMACIÓN ORIENTADA A OBJETOS - PARTE I_ 👨‍💻


#### 1. Clase Libro

* Crea una clase Libro con los atributos titulo, autor y añoPublicacion. Incluye un constructor primario y un método para imprimir la información del libro.

```Kotlin

class Libro(val titulo: String, val autor: String, val añoPublicacion: Int) {
    fun imprimirInfo() {
        println("'$titulo' por $autor ($añoPublicacion)")
    }
}

fun main() {
    val miLibro = Libro("1984", "George Orwell", 1949)
    miLibro.imprimirInfo()
}
```

#### 2. Clase Cuenta Bancaria

* Diseña una clase CuentaBancaria con un atributo privado saldo. Incluye métodos para depositar, retirar y consultar saldo.

```Kotlin
class CuentaBancaria(saldoInicial: Double) {
    private var saldo = saldoInicial

    fun depositar(monto: Double) {
        saldo += monto
        println("Depósito de $monto realizado. Nuevo saldo: $saldo")
    }

    fun retirar(monto: Double) {
        if (monto <= saldo) {
            saldo -= monto
            println("Retiro de $monto realizado. Nuevo saldo: $saldo")
        } else {
            println("Saldo insuficiente")
        }
    }

    fun consultarSaldo() = println("Saldo actual: $saldo")
}

fun main() {
    val cuenta = CuentaBancaria(100.0)
    cuenta.depositar(50.0)
    cuenta.retirar(30.0)
    cuenta.consultarSaldo()
}

```

#### 3. Clase con Constructor Secundario

* Crea una clase Rectangulo con atributos ancho y alto. Incluye un constructor primario y un constructor secundario que inicialice ambos valores con el mismo número.

```Kotlin
    class Rectangulo(val ancho: Double, val alto: Double) {
    constructor(lado: Double) : this(lado, lado)

    fun calcularArea() = ancho * alto
}

fun main() {
    val rectangulo1 = Rectangulo(5.0, 3.0)
    val cuadrado = Rectangulo(4.0)

    println("Área del rectángulo: ${rectangulo1.calcularArea()}")
    println("Área del cuadrado: ${cuadrado.calcularArea()}")
}
```

#### 4. Getters y Setters Personalizados

* Implementa una clase Temperatura con un atributo en Celsius. Incluye getters y setters personalizados para obtener y establecer la temperatura en Fahrenheit.

```Kotlin
    class Temperatura(celsius: Double) {
    var celsius = celsius
        set(value) {
            field = value
            println("Temperatura establecida a $value°C")
        }

    var fahrenheit: Double
        get() = celsius * 9/5 + 32
        set(value) {
            celsius = (value - 32) * 5/9
            println("Temperatura establecida a $value°F")
        }
}

fun main() {
    val temp = Temperatura(25.0)
    println("En Fahrenheit: ${temp.fahrenheit}°F")
    temp.fahrenheit = 68.0
    println("En Celsius: ${temp.celsius}°C")
}
```

#### 5. Clase con Propiedades Lazy

* Crea una clase Calculadora con una propiedad pi que se inicialice de manera perezosa (lazy) y un método para calcular el área de un círculo.

```Kotlin
class Calculadora {
    val pi: Double by lazy {
        println("Calculando pi...")
        3.14159265359
    }

    fun areaCirculo(radio: Double): Double {
        return pi * radio * radio
    }
}

fun main() {
    val calc = Calculadora()
    println("Área de un círculo con radio 5: ${calc.areaCirculo(5.0)}")
    println("Área de un círculo con radio 3: ${calc.areaCirculo(3.0)}")
}

```

#### 6. Clase con Métodos de Extensión


* Define una clase Persona con propiedades nombre y edad. Luego, crea un método de extensión para imprimir un saludo personalizado.

```Kotlin
class Persona(val nombre: String, val edad: Int)

fun Persona.saludar() {
    println("Hola, mi nombre es $nombre y tengo $edad años.")
}

fun main() {
    val persona = Persona("Ana", 28)
    persona.saludar()
}
```

# _SESIÓN 4: PROGRAMACIÓN ORIENTADA A OBJETOS - PARTE II_ 🔄

#### 1. Herencia y Polimorfismo

* Crea una clase base Animal con un método hacerSonido().
  
* Crea dos clases derivadas Perro y Gato que hereden de Animal y sobrescriban el método hacerSonido().
  
* Crea una función que reciba un Animal y llame a su método hacerSonido().

```Kotlin
open class Animal {
    open fun hacerSonido() {
        println("El animal hace un sonido")
    }
}

class Perro : Animal() {
    override fun hacerSonido() {
        println("El perro ladra")
    }
}

class Gato : Animal() {
    override fun hacerSonido() {
        println("El gato maulla")
    }
}

fun hacerSonar(animal: Animal) {
    animal.hacerSonido()
}

fun main() {
    val perro = Perro()
    val gato = Gato()
    
    hacerSonar(perro) // Imprime: El perro ladra
    hacerSonar(gato)  // Imprime: El gato maulla
}

```

#### 2. Clases Abstractas

* Crea una clase abstracta Figura con un método abstracto calcularArea().
  
* Implementa dos clases concretas Circulo y Rectangulo que hereden de Figura.
  
* Implementen el método calcularArea().

```Kotlin
abstract class Figura {
    abstract fun calcularArea(): Double
}

class Circulo(private val radio: Double) : Figura() {
    override fun calcularArea(): Double {
        return Math.PI * radio * radio
    }
}

class Rectangulo(private val base: Double, private val altura: Double) : Figura() {
    override fun calcularArea(): Double {
        return base * altura
    }
}

fun main() {
    val circulo = Circulo(5.0)
    val rectangulo = Rectangulo(4.0, 6.0)
    
    println("Área del círculo: ${circulo.calcularArea()}")
    println("Área del rectángulo: ${rectangulo.calcularArea()}")
}
```

#### 3. Interfaces

* Crea una interfaz Volador con un método volar().
  
* Implementa esta interfaz en las clases Ave y Avion.
  
* Crea una función que reciba un Volador y llame a su método volar().

```Kotlin
interface Volador {
    fun volar()
}

class Ave : Volador {
    override fun volar() {
        println("El ave vuela moviendo sus alas")
    }
}

class Avion : Volador {
    override fun volar() {
        println("El avión vuela usando motores")
    }
}

fun hacerVolar(volador: Volador) {
    volador.volar()
}

fun main() {
    val ave = Ave()
    val avion = Avion()
    
    hacerVolar(ave)   // Imprime: El ave vuela moviendo sus alas
    hacerVolar(avion) // Imprime: El avión vuela usando motores
}

```

#### 4. Data Classes

* Crea una data class Libro con propiedades para título, autor y año de publicación.
* Crea una lista de libros y utiliza las funciones generadas automáticamente para copiar un libro y comparar dos libros.

```Kotlin
data class Libro(val titulo: String, val autor: String, val anioPublicacion: Int)

fun main() {
    val libro1 = Libro("1984", "George Orwell", 1949)
    val libro2 = Libro("Cien años de soledad", "Gabriel García Márquez", 1967)
    val libro3 = libro1.copy(titulo = "Rebelión en la granja")
    
    val libros = listOf(libro1, libro2, libro3)
    
    println(libro1 == libro2) // false
    println(libro1 == libro1.copy()) // true
    
    libros.forEach { println(it) }
}
```

#### 5. Companion Object
* Crea una clase Contador con un companion object que mantenga un contador global de instancias creadas.
* Cada vez que se cree una nueva instancia de Contador, el contador global debe incrementarse.

```Kotlin
class Contador {
    companion object {
        private var contadorGlobal = 0
        
        fun obtenerContadorGlobal(): Int {
            return contadorGlobal
        }
    }
    
    init {
        contadorGlobal++
    }
}

fun main() {
    println(Contador.obtenerContadorGlobal()) // 0
    
    val contador1 = Contador()
    println(Contador.obtenerContadorGlobal()) // 1
    
    val contador2 = Contador()
    val contador3 = Contador()
    println(Contador.obtenerContadorGlobal()) // 3
}

```

#### 6. Herencia Múltiple con Interfaces

* Crea dos interfaces Nadador y Corredor con métodos nadar() y correr() respectivamente.
* Crea una clase Triatleta que implemente ambas interfaces.
* Crea una función que reciba un objeto y verifique si puede nadar, correr o ambos.

```Kotlin
interface Nadador {
    fun nadar()
}

interface Corredor {
    fun correr()
}

class Triatleta : Nadador, Corredor {
    override fun nadar() {
        println("El triatleta está nadando")
    }
    
    override fun correr() {
        println("El triatleta está corriendo")
    }
}

fun verificarHabilidades(obj: Any) {
    if (obj is Nadador) {
        obj.nadar()
    }
    if (obj is Corredor) {
        obj.correr()
    }
}

fun main() {
    val triatleta = Triatleta()
    verificarHabilidades(triatleta)
}
```
# _Sesión 5: Programación funcional_ :accessibility:

#### 1. Expresiones Lambda

*Crea una función literal que calcule el cuadrado de un número y úsala para calcular el cuadrado de 5.

```Kotlin
val cuadrado = { x: Int -> x * x}
	fun main() {
        println(cuadrado(5))
    }
```

#### 2. Funciones de Orden Superior

* Uso simple de función de orden superior: Utiliza la función de orden superior filter para obtener una lista de números pares de una lista dada,  multiplos de 2 de los elementos de la lista
  
```Kotlin
val numeros = listOf(1, 2, 3, 4, 5)
val pares = numeros.filter { it % 2 == 0 }
fun main(){
println(pares) // Imprime: [2, 4]
}
```

* Función de orden superior personalizada:
* Crea una función de orden superior llamada aplicarOperacion que tome dos números y una función, y aplique esa función a los números.

```Kotlin
fun aplicarOperacion(a: Int, b: Int, operacion: (Int, Int) -> Int): Int{
    return operacion(a,b)
} 
val suma = aplicarOperacion(5.0, 3.0){x, y -> x + y}
fun main(){
    println("Suma: $suma")
}
```

* Crea una función de orden superior llamada transformarLista que tome una lista de números enteros y una función de transformación.
* La función debe aplicar la transformación a cada elemento de la lista y devolver una nueva lista con los resultados.

```Kotlin
fun main(){
fun transformarLista(lista: List<Int>, transformacion: (Int) -> Int): List <Int> {
    return lista.map {transformacion(it)}
}
val numeros = listOf(1, 2, 3, 4, 5)
val listaDoble = transformarLista(numeros){ it * 2}
println("Lista duplicada: $listaDoble")
}
```


#### 3. Inline Functions

```Kotlin
inline fun saludar(nombre: String){
   println("Hola, $nombre")
}
fun main (){
   println("Hi my name is Aura")
}
```

#### 4. Filter y Map

* Utiliza filter para obtener solo las palabras que tengan más de 5 letras, y luego usa map para convertir estas palabras a mayúsculas.

 ```Kotlin
fun main() {
    val palabras = listOf("gato", "perro", "elefante", "ratón", "hipopótamo")
    
    val resultado = palabras
        .filter { it.length > 5 }
        .map { it.uppercase() }
    
    println(resultado)
}
```

* Ejemplo de map

* Crea una función que tome una lista de temperaturas en Celsius y las convierta a Fahrenheit.
* Luego, en la función main, crea una lista de temperaturas en Celsius, aplica la conversión, e imprime los resultados.

```Kotlin
fun CelsiusaFahrenheit(temperaturas: List<Double>): List<Double> {
    return temperaturas.map { it * 9/5 + 32}
}
fun main(){
    
 val temperaturasC = listOf(10.0, 120.0, 40.0, 38.0)
 val temperaturasF = CelsiusaFahrenheit(temperaturasC)
 println("Temperaturas en Fahrenheit: $temperaturasF")
}
```

#### 5. Partition y FlatMap

* Vamos a trabajar con una lista de números y usaremos partition para separar los números pares de los impares.

```Kotlin

fun main(){
val numeros = listOf(10,6,4,8,5,2,8,9,4,3,6,7,9,10,10,10,4,6,7)
val (pares, impares) = numeros.partition{it % 2 == 0}
println("Números pares: $pares")
println("Números impares: $impares")
}
```


#### 6. Reduce y ForEach

* Vamos a trabajar con una lista de números y usaremos partition para separar los números pares de los impares.



# Sesión 6: Interoperabilidad Kotlin-Java

#### 1. Uso de Clases Java en Kotlin

* Crea una clase Java llamada Persona con propiedades nombre y edad, y sus respectivos getters y setters. Luego, en Kotlin, crea una instancia de esta clase y modifica sus propiedades.

```Kotlin
    // Persona.java
public class Persona {
    private String nombre;
    private int edad;

    public String getNombre() { return nombre; }
    public void setNombre(String nombre) { this.nombre = nombre; }
    public int getEdad() { return edad; }
    public void setEdad(int edad) { this.edad = edad; }
}
kotlinCopy// main.kt
fun main() {
    val persona = Persona()
    persona.nombre = "Juan"
    persona.edad = 25
    println("Nombre: ${persona.nombre}, Edad: ${persona.edad}")
}
```

#### 2. Uso de Clases Kotlin en Java

* Crea una clase Kotlin llamada Producto con propiedades nombre y precio. Luego, en Java, crea una instancia de esta clase y accede a sus propiedades.

```Kotlin
// Producto.kt
class Producto(var nombre: String, var precio: Double)
javaCopy// Main.java
public class Main {
    public static void main(String[] args) {
        Producto producto = new Producto("Laptop", 999.99);
        System.out.println("Nombre: " + producto.getNombre() + ", Precio: " + producto.getPrecio());
    }
}
```

#### 3. Miembros Estáticos de Java en Kotlin

* Crea una clase Java con un método estático y una constante estática. Luego, accede a estos miembros desde Kotlin.

```Kotlin
// Util.java
public class Util {
    public static final String VERSION = "1.0";
    public static int sumar(int a, int b) {
        return a + b;
    }
}
// main.kt
fun main() {
    println("Versión: ${Util.VERSION}")
    println("Suma: ${Util.sumar(5, 3)}")
}
```

#### 4. Companion Object de Kotlin en Java

* Crea una clase Kotlin con un companion object que contenga un método y una propiedad. Luego, accede a estos miembros desde Java.

```Kotlin
// Calculadora.kt
class Calculadora {
    companion object {
        const val PI = 3.14159
        fun cuadrado(n: Int): Int = n * n
    }
}
// Main.java
public class Main {
    public static void main(String[] args) {
        System.out.println("PI: " + Calculadora.PI);
        System.out.println("Cuadrado de 5: " + Calculadora.Companion.cuadrado(5));
    }
}
```

#### 5. Uso de Keywords de Kotlin como Identificadores en Java

* Crea una clase Java con métodos cuyos nombres sean palabras clave en Kotlin (por ejemplo, when, is, object). Luego, llama a estos métodos desde Kotlin.

```Kotlin
// Keywords.java
public class Keywords {
    public static void when() {
        System.out.println("Método when");
    }
    
    public static void is() {
        System.out.println("Método is");
    }
    
    public static void object() {
        System.out.println("Método object");
    }
}
// main.kt
fun main() {
    Keywords.`when`()
    Keywords.`is`()
    Keywords.`object`()
}
```

#### 6. Propiedades Kotlin con Nombres Especiales en Java

*Crea una clase Kotlin con propiedades cuyos nombres requieran un tratamiento especial en Java (por ejemplo, is para un booleano). Luego, accede a estas propiedades desde Java.

```Kotlin
// EstadoObjeto.kt
class EstadoObjeto {
    var isActivo: Boolean = false
    var hasValor: Int = 0
}
// Main.java
public class Main {
    public static void main(String[] args) {
        EstadoObjeto estado = new EstadoObjeto();
        estado.setActivo(true);
        estado.setHasValor(10);
        System.out.println("Activo: " + estado.isActivo());
        System.out.println("Valor: " + estado.getHasValor());
    }
}
```

# Sesión 7: Manejo de errores 🩹

#### 1. Null Safety

* var nombre: String? = "Juan"
* ¿Cuál es la forma correcta de obtener la longitud del nombre si no es nulo, o devolver 0 si es nulo?

```Kotlin
val longitud = nombre?.length ?: 0
```
Esta solución utiliza el operador de llamada segura ?. y el operador Elvis ?: para manejar el caso nulo de manera concisa.

#### 2. Manejo de Excepciones
* Escribe una función que tome un String y lo convierta a un Int. Si la conversión falla, la función debe devolver null. Usa un bloque try-catch para manejar la excepción.

```Kotlin
fun convertirAEntero(str: String): Int? {
    return try {
        str.toInt()
    } catch (e: NumberFormatException) {
        null
    }
}
Esta función intenta convertir el String a Int y devuelve null si ocurre una NumberFormatException.
```
#### 3. Smart Casting

* sealed class Resultado
* class Exito(val mensaje: String) : Resultado()
* class Error(val codigo: Int) : Resultado()
* Escribe una función que tome un Resultado y devuelva un String describiendo el resultado.

```Kotlin
fun describirResultado(resultado: Resultado): String {
    return when (resultado) {
        is Exito -> "Éxito: ${resultado.mensaje}"
        is Error -> "Error: Código ${resultado.codigo}"
    }
}
Esta función utiliza smart casting para acceder a las propiedades específicas de cada subclase de Resultado.
```

#### 4. Safe Cast

* Escribe una función que tome un Any y lo convierta de manera segura a un List.
* Si la conversión no es posible, debe devolver una lista vacía.

```Kotlin
fun convertirAListaDeStrings(objeto: Any): List<String> {
    return (objeto as? List<*>)?.filterIsInstance<String>() ?: emptyList()
}
Esta función utiliza safe cast as? y filterIsInstance para realizar una conversión segura.
```

#### 5. Manejo de Null con Let

* Dada una variable nullable usuario: Usuario?, escribe un código que imprima el nombre del usuario si existe, o "Usuario desconocido" si es null. Usa la función let.

```Kotlin
usuario?.let { 
    println(it.nombre) 
} ?: println("Usuario desconocido")
Esta solución utiliza let para ejecutar un bloque de código solo si usuario no es null, y el operador Elvis para manejar el caso nulo.
```
#### 6. Lanzamiento de Excepciones Personalizadas

* Crea una función dividir que tome dos enteros y devuelva su división. Si el segundo número es cero, debe lanzar una excepción personalizada llamada DivisionPorCeroException.

```Kotlin
class DivisionPorCeroException : Exception("No se puede dividir por cero")

fun dividir(a: Int, b: Int): Int {
    if (b == 0) {
        throw DivisionPorCeroException()
    }
    return a / b
}
```

# Sesión 8: Programacion Asíncrona


#### 1. Lanzamiento de una corrutina básica

*Escribe una función main que lance una corrutina usando GlobalScope.launch. 

*La corrutina debe imprimir "Hola desde la corrutina" después de un retraso de 1 segundo.

```Kotlin
import kotlinx.coroutines.*

fun main() = runBlocking {
    GlobalScope.launch {
        delay(1000)
        println("Hola desde la corrutina")
    }
    delay(2000) // Esperamos para que la corrutina tenga tiempo de ejecutarse
}
Esta solución lanza una corrutina global que imprime un mensaje después de un segundo de retraso.
```

#### 2. Uso de runBlocking

* Modifica el ejercicio anterior para usar runBlocking en lugar de GlobalScope.launch. Elimina la necesidad de esperar explícitamente al final de la función main.

```Kotlin
import kotlinx.coroutines.*

fun main() = runBlocking {
    launch {
        delay(1000)
        println("Hola desde la corrutina")
    }
}
Esta solución utiliza runBlocking para crear un scope de corrutina y launch para iniciar una nueva corrutina dentro de ese scope.
```

#### 3.Funciones de suspensión

* Crea una función de suspensión llamada obtenerDatos que simule la obtención de datos de una API.
* Debe tomar un tiempo aleatorio entre 500ms y 2000ms, y devolver un String. 
* Usa esta función en la main.

```Kotlin
import kotlinx.coroutines.*
import kotlin.random.Random

suspend fun obtenerDatos(): String {
    delay(Random.nextLong(500, 2000))
    return "Datos obtenidos"
}

fun main() = runBlocking {
    println("Iniciando obtención de datos...")
    val resultado = obtenerDatos()
    println(resultado)
}
Esta solución define una función de suspensión que simula una operación de larga duración y la utiliza en la función main.
```

#### 4. Manejo de Jobs

* Lanza dos corrutinas, una que imprima números del 1 al 5 cada 500ms, y otra que imprima letras de la 'a' a la 'e' cada 750ms. Usa Jobs para esperar a que ambas corrutinas terminen antes de finalizar el programa.

```Kotlin
import kotlinx.coroutines.*

fun main() = runBlocking {
    val job1 = launch {
        for (i in 1..5) {
            delay(500)
            println(i)
        }
    }
    
    val job2 = launch {
        for (c in 'a'..'e') {
            delay(750)
            println(c)
        }
    }
    
    job1.join()
    job2.join()
    println("Todas las corrutinas han terminado")
}
Esta solución lanza dos corrutinas y utiliza join() para esperar a que ambas terminen antes de finalizar el programa.
```

#### 5. Cancelación de corrutinas

*Crea una corrutina que imprima números incrementalmente cada segundo. Después de 5 segundos, cancela la corrutina.

```Kotlin
import kotlinx.coroutines.*

fun main() = runBlocking {
    val job = launch {
        var i = 1
        while (isActive) {
            println(i++)
            delay(1000)
        }
    }
    
    delay(5000)
    job.cancel()
    println("Corrutina cancelada")
}
Esta solución lanza una corrutina que se ejecuta indefinidamente, pero se cancela después de 5 segundos usando job.cancel().
```

#### 6. Corrutinas en paralelo con async

* Crea dos funciones de suspensión que simulen operaciones largas (por ejemplo, obtenerUsuario y obtenerPerfil).
* Usa async para ejecutarlas en paralelo y combina sus resultados.

```Kotlin
import kotlinx.coroutines.*

suspend fun obtenerUsuario(): String {
    delay(1000)
    return "Usuario123"
}

suspend fun obtenerPerfil(): String {
    delay(1000)
    return "Perfil de desarrollador"
}

fun main() = runBlocking {
    val usuario = async { obtenerUsuario() }
    val perfil = async { obtenerPerfil() }
    
    println("Usuario: ${usuario.await()}")
    println("Perfil: ${perfil.await()}")
}
Esta solución utiliza async para ejecutar dos operaciones en paralelo y luego combina sus resultados usando await()
```
