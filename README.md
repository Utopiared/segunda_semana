# FUNDAMENTOS KOTLIN

![_f8f85b7e-0373-479b-8595-5ea5766dd43e](https://github.com/user-attachments/assets/11aa9363-51dd-4d38-b0cd-5bd064ace9ec)

*Autora: Aura Nicte-Ha Pech Reyes.*

## 1.Declaración de Variables
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
