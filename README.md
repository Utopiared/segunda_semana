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

*Verificar si son iguales Verificar si la primera es mayor que la segunda Verificar si la segunda es menor o igual que la primera Muestra el resultado de cada comparación.

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

*Crea variables para el peso (en kg) y la altura (en metros) de una persona. Calcula el Índice de Masa Corporal (IMC) usando la fórmula: IMC = peso / (altura * altura) Muestra el resultado del IMC.

```Kotlin
fun main(){
  val peso = 70.0 // kg
  val altura = 1.75 // metros
  val imc = peso / (altura * altura)
  
  println("IMC: ${"%.2f".format(imc)}")
}
```











































