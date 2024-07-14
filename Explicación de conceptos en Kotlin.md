# Explicación de conceptos en Kotlin

## 1. Variables:
En Kotlin, una variable es un contenedor que almacena un valor que puede cambiar durante la ejecución del programa. Las variables se definen utilizando la palabra clave `var`. A diferencia de las constantes, las variables pueden reasignarse a nuevos valores después de su inicialización.

**Ejemplo:**
var variable: String = "hola"
variable = "adios"
println(variable)

## 2. Constantes:
En Kotlin, una constante es una referencia a un valor que no puede ser modificado después de su inicialización. Las constantes se definen utilizando la palabra clave val. A diferencia de las variables (var), una vez que se asigna un valor a una constante, no se puede cambiar.

**Ejemplo:**

val constante: String = "hola"
// constante = "No puedo cambiar mi valor"
println(constante)

## 3. Opcionales y manejo de nulos:
En Kotlin, el manejo de nulos y las variables opcionales están diseñados para prevenir errores comunes relacionados con valores nulos (como las excepciones NullPointerException), proporcionando un sistema de tipos que permite declarar explícitamente cuándo una variable puede ser nula.

**Ejemplo:**
var nombre: String? = "Paola"
println("Nombre: \$nombre")
nombre = null // Esto es válido porque la variable es de tipo String?
println("Nombre después de asignar null: \$nombre")

val longitud: Int = nombre?.length ?: 0
println("Longitud del nombre: \$longitud")

// val longitudForzada: Int = nombre!!.length // Esto lanzará una excepción si nombre es nulo

## 4. Funciones con parámetros opcionales:
En Kotlin, las funciones con parámetros opcionales permiten definir valores predeterminados para algunos de sus parámetros. Esto hace que esos parámetros sean opcionales al momento de llamar a la función. Si no se proporciona un valor para un parámetro opcional, se utilizará el valor predeterminado definido en la función.

**Ejemplo:**
fun saludo(saludo: String = "Hola", nombre: String? = null) {
    val nombreSaludo = nombre ?: "Desconocido"
    println("\$saludo, \$nombreSaludo!")
}
saludo() // Llamada con valores por defecto
saludo(nombre = "Danna") // Llamada con parámetro opcional
saludo(saludo = "Buenos días", nombre = "Jhon") // Llamada con todos los parámetros



