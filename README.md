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
