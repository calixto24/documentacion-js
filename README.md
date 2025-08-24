# Documentacion JavaScript

Mi apredinzaje en JavaScript

## Indice

- [1. Introduccion](#introduccion)
  - [Caracteristicas](#caracteristicas)
  - [Identificadores](#identificadores)
  - [Nomenclaturas](#nomenclaturas)
  - [Tipos de datos](#tipos-de-datos)
  - [Variables](#variables)
  - [Constantes](#constantes)
  - [Valores especiales](#valores-especiales)
  - [Funciones](#funciones)
  - [Arreglos](#arreglos)
  - [Objetos](#objetos)
  - [Tipos de operadores](#tipos-de-operadores)
  - [Ternarias](#ternarias)
  - [Break & Continue](#break--continue)
- [2. Capitulo 2](#capitulo-2)
  - [Destructuracion](#destructuracion)
  - [Objetos literales](#objetos-literales)
  - [Parametros REST & Spread](#parametros-rest--operador-spread)
  - [Arrow Functions](#arrow-function)

## Introduccion

JavaScript es el unico lenguaje de programacion donde puedes hacer isomorfismo. Es decir, una aplicacion web.

### Caracteristicas

- Alto Nivel: Al ser de alto nivel no necesitamos estar pendiente de obtimizar su rendimiento, ya que es lo que lo diferencia de uno de bajo nivel.

- Interpretado: Se compila en tiempo de ejecucion.

- Debilmente tipado: El tipo de varible puede variar en base a nuestras necesidades, no hay una restriccion.

- Sensible con mayus-minus culas: Son variables distintas aunque tengan el mismo nombre.

### Identificadores

Es el nombre que se le otorga a las funciones, variables, etc. Pueden comenzar con:

- Letra (a-z)
- Signo de dolar ($)
- Guion abajo (\_)

* Jamas con numeros o caracteres especiales

### Nomenclaturas

- ARCHIVOS: Usamos el snake_case

```bash
  mi_archivo.js
```

- CONSTANTES: Usamos el UPPER_CASE

```bash
  const MI_CONSTANTE = 3.14
```

- CLASES: Usamos el UpperCamelCase

```bash
  class UnaClase {}
```

- OBJETOS: Usamos el lowerCamelCase

```bash
  const unObjeto = "Prueba"
```

- Aplica para funciones, primitivos e instancias

### Tipos De Datos

- Primitivos: Se accede directamente al valor

  - string
  - number
  - boolean
  - null
  - undefined
  - NaN

- Compuestos: Se accede a la referencia del valor
  - object = {}
  - array = []
  - function () => {}
  - Class {}

### Variables

Antes en JavaScript no existia el ambito de bloque. Es decir el "var" no respetaba los bloques, ya que eran de ambito global.

Despues llego la palabra reservada "let" que justamente se encargo de cumplir esa funcion.

### Constantes

No puedes tener una constante vacia cuando el dato es primitivo, ya que accedes al dato directamente.

En cambio, para un dato compuesto si puedes ya que estas accediendo a la referencia del valor.

### Valores especiales

- Undefined: Es cuando declaras una variable pero no le asignas ningun valor.

- null: Es cuando quieres intencionalmente que el valor declarado sea nulo.

- NaN: Es cuando quieres realizar una operacion matematica pero no puede ser representada por un numero.

### Funciones

Para utilizar las funciones en javaScript tenemos que utilizar la palabra reservada "function",

- Funciones declaradas: Son funciones que los puedes llamar en cualquier parte del codigo, ya que internamente javaScript por medio del ordenamiento de codigo lo eleva (hoisting).

```bash
  function saludar() {
  }
  saludar()
```

- Funciones expresadas: Es la que se asigna a una variable y no se se puede utilizar antes de su definición.

```bash
  const despedida = function () {
  }
  despedida()
```

### Arreglos

Es un conjunto de elementos, js nos permite guardar cualquier tipo de dato.

- Creacion de un arreglo

  1. Forma 1:

  ```bash
    const a = [1,2,3]
  ```

  2. Forma 2:

  ```bash
    const b = Array.of("a", "b", "c")
  ```

  El metodo array.of tambien nos permite guardar elementos.

  3. Forma 3:

  ```bash
    const c = new Array("a", "b", "c")
  ```

  Esta forma ya esta en desuso, o esta desfasado

- Agregar elementos: Para agregar elementos usamos el push:

  ```bash
    const a = [1,2,3]
    a.push(4)
  ```

- Eliminar elementos: Para eliminar elementos usamos el push:

  ```bash
    const a = [1,2,3,4]
    a.pop()
  ```

- Recorrido de un arreglo:

  Estructura

  ```bash
    const a = [1,2,3,4]
    a.forEach(function (el *Elemento*, index *Posicion*) {})
  ```

### Objetos

Es una coleccion de llaves y valores. Asimimismo, los elementos dentro de un objeto se les conoce como propiedades y a las funciones se les llama metodos.

### Tipos de operadores

- "=" -> Es una asignacion de variables
- "==" -> Comparacion de valores
- "===" -> Comparacion de tipo de dato y de valor

Hoy en dia es buena practica utilizar los tres iguales.

### Ternarias

Es la simplificacion del if-else en una linea de codigo, pero si son varias lineas de codigo es recomendable el anterior.

```bash
    const prueba = (condicion) ? verdadero : falso
```

### Break & Continue

Ayudan a controlar el flujo de una estructura de control

- Break: Sale de la estructura de control.
- Continue: Se encarga de omitir ejecutar el siguiente valor.

## Capitulo 2

En este capitulo vamos a ver temas mas complejos.

### Destructuracion

Es la asignacion dinamica de lo que hay en un arreglo u objeto en nuevas variables.

- Para el caso de arreglos:

```bash
    const numeros = {1,2,3}
    const {one, two, three} = numeros
```

A diferencia de los objetos, si solo queremos un elemento, debemos respetar la posicion en la que se encuentre.

```bash
    const numeros = {1,2,3}
    const {,, three} = numeros
```

- Para los objetos:

```bash
    const persona = {
      nombre: "Jhordan",
      apellido: "Calixto"
    }

    const {nombre, apellido} = persona
```

Es importante que los nombres de las variables donde guardaremos informacion sea el mismo al de las propiedades.

### Objetos literales

Son estandares que introdujo Emascript para facilitar su uso, para crear y definir un objeto ya que en JS todo es un objeto.

Asimismo, se agrego una nueva caracteristica en donde si ya tenemos varibales declaradas y en nuestro objeto tendra una propiedad con el mismo nombre no es necesario sobreescribirlo.

```bash
    const nombre = "Jhordan"

    const persona = {
      nombre,
      apellido: "Calixto"
    }
```

JS entiende que si comparten el mismo nombre, pues el valor es el mismo.

### Parametros REST & Operador Spread

- Los parametros REST sun utiles cuando queremos funciones con una cantidad indefinida de parametros. Cabe aclarar que los almacena por defecto en un arreglo.

```bash
    function suma(a, b, ...c) {}
```

Su caracteristica principal son los 3 puntos.

- Por otra parte, los Operadores Spread sirven para descomponer un arreglo u objeto.

```bash
    const numeros = [1,2,3]
    console.log(...numeros) //1 2 3
```

Podremos visualizar que la impresion ya no saldra con array

### Arrow Function

Son una forma mas sencilla de escribir funciones expresadas.

- Tradicional

```bash
    const suma = function (a,b) {
      return a + b
    }
```

- Arrow Function

```bash
    const suma = (a,b) => a + b
```

Pero cabe recalcar que es una mala practica utilizarlo en objetos literales ¿Porque? Este tipo de funcion no respeta el contexto en el que se encuentra.

### Prototipos

JavaScript es un lenguaje basado en prototipos, todos los objetos tienen prototipos. Es una especie de plantilla u objeto padre que tiene propiedades y metodos, eso es un prototipo.

Si JS no le encuentra una propiedad a un objeto, este accede a buscarlo en su prototipo y si no esta busca en otro. Se le conoce como (Prototype Chain)

- Funciones constructoras: Lo ideal es que solo tengan los atributos y no los metodos se les implemente al prototipo para mejorar el rendimiento y memoria.

```bash
    function Persona(nombre, apellido) {
      this.nombre = nombre,
      this.apellido = apellido
    }

    Persona.prototype.fullName = function () {
      console.log("Hola")
    }
```

### Operador de Cortocircuito

- OR (||) : Cuando el valor de la izquierda tiende a verdadero, es el valor que se cargara por defecto.

- AND : Cuando el valor de la izquierdan tienda a falso, es el valor que se cargara por defecto.

### Expresiones regulares

Son patrones que usamos para validar cadenas de texto

```bash
    let expReg = new RegExp(/*Escribes el patron*/)
```

Puedes utilizar su metodo test que nos dara un true or false, verifica si cumple el patron
