# FUNDAMENTOS KOTLIN

![_f8f85b7e-0373-479b-8595-5ea5766dd43e](https://github.com/user-attachments/assets/11aa9363-51dd-4d38-b0cd-5bd064ace9ec)

*Autora: Aura Nicte-Ha Pech Reyes.*


## SESION 1 ¿QUE ES KOTLIN? 💻

### 1.Declaración de Variables
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
### 2.Operaciones Aritméticas
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
### 3.Incremento y Decremento
Declara una variable numérica e:

* Incrementa su valor en 1 y muestra el resultado Decrementa su valor en 1 y muestra el resultado:

```Kotlin
fun main(){
  var contador = 5
  println("Incremento: ${++contador}")
  println("Decremento: ${--contador}")
}
```

### 4.Operadores de Asignación Compuesta

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
### 5.Comparaciones

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

### 6.Operaciones con Strings

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
### 7. Cálculo de Descuento

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
### 8. Conversión de Tipos

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

### 9. Operaciones Booleanas

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
### 10. Cálculo de IMC

* Crea variables para el peso (en kg) y la altura (en metros) de una persona. Calcula el Índice de Masa Corporal (IMC) usando la fórmula: IMC = peso / (altura * altura) Muestra el resultado del IMC.

```Kotlin
fun main(){
  val peso = 70.0 // kg
  val altura = 1.75 // metros
  val imc = peso / (altura * altura)
  
  println("IMC: ${"%.2f".format(imc)}")
}
```
## Sesión 2 Fundamentos de programación. 🖱️

### 1. Calculadora de volumen de cilindro

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

### 2. Verificador de número primo

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

### 3. Validador de email con función local

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

### 4. Clasificador de edades usando when

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

### 5. Imprimir números pares en un rango

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

### 6. Contar vocales en una lista de palabras

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

### 7. Diccionario de sinónimos

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


## Sesión 3: Programación orientada a objetos - Parte I 👨‍💻


### 1. Clase Libro

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

### 2. Clase Cuenta Bancaria

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

### 3. Clase con Constructor Secundario

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

### 4. Getters y Setters Personalizados

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

### 5. Clase con Propiedades Lazy

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

### 6. Clase con Métodos de Extensión


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







































