# Funciones

* Su objetivo es __centralizar__ la logica de un procedimiento que se puede reutilizar varias veces.

* La diferendia entre una funcion y un metodo, es que el metodo de encuentra dentro de un objeto.

* Es buena practica que la definicion de las funciones esten siempre al principio.

* Todas las funciones tradicionales internamente cuando se ejecutan tienen un objeto llamado __arguments__.

---

## Declaracion de funciones

__Forma tradicional de declarar una funcion:__
```
function nombreFuncion() {
    // Cuerpo de la funcion
}
```
__Funcion anonima:__
```
const nombreFuncion = function() {
    // Cuerpo de la funcion
}
```

__Arrow function:__
```
const nombreFuncion = () => {
    // Cuerpo de la funcion
}
```

---

## Retorno de las funciones

Si la funciones __no__ tienen la palabra __return__ explicita no regresa nada(undefined).

El __return__ de una funcion puede regresar cualquier cosa.

---

## Protip - Retorno

Forma corta de trabjar con funciones.

__Definicion de la funcion:__
```
const crearPersona = ( nombre, apellido ) => ( {nombre, apellido} )
```
__Ejecucion de la funcion:__
```
const persona = crearPersona('Steve','Rogers');
```
__El valor obtenido es:__
```
{nombre: "Steve", apellido: "Rogers"}
```

Cuando retornamos algo entre ```{}``` le estamos diciendo a JavaScript que retorne eso como un __objeto__ pero debe de ir encerrado entre ```()```.

Las ```arrow function``` no cuentan con el objeto ```arguments``` de las funciones tradicionales. pero es posible acceder a el objeto agregandolo como un parametro tipo ```rest```.  Ej:

```
const nombreFuncion = ( ...args ) => {
    // Cuerpo de la funcion
}
```

Consideraciones en los parametros __rest__:
- Despues del parametro rest no puede venir ningun otro argumento.
- Si se necesita extraer una variable del parametro rest, entonces lo extraido tendra su valor independiente.

## Desestructuracion de valores

```
const nombreFuncion = ( ..args ) => {
    return args;
}
```
En este caso los valores que se envian a la funcion anterior son obtenidos en variables independientes en la desestructuracion.
```
const [ valor1, valor2, valor3 ] = nombreFuncion( 10, 'hello', true );
```
se obtiene:
```
{ valor1: 10, valor2: 'hello', valor3: true }
```

Tambien podemos cambiar el nombre de la llave cuando desestructuramos un valor. Ej:

```
const nombreFuncion = ( nombre, apellido ) => {
    return {
        nombre,
        apellido,
    };
}
```
```
const { apellido: nuevoApellido } = nombreFuncion( 'Steve', 'Rogers' ):
```

## Desestructuracion de argumentos

```
const persona = {
    nombre: 'Steve',
    apellido: 'Rogers',
    codeName: 'Cap',
    vivo: true,
    edad: 85,
}
```
```
const nombreFuncion( persona );
```
```
const nombreFuncion = ( { nombre = 'Steve', codeName, vivo } ) => {

    console.log({nombre});
    console.log({codeName});
    console.log({vivo});

}
```
En este caso cuando recibe por parametro a el objeto persona, solo desestructura y obtienen los tres valores que le interesan, ```nombre, codeName, vivo```, mientras hace esto le asigna un valor por degecto a nombre, ```nombre = 'Steve'``` esto para que en caso de no traer el valor, le asigne ese.

