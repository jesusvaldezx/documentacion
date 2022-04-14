# Javascript

- Es un lenguaje multiplataforma estandar de la web.
- JavaScript es un lenguaje interpretado.
- Los navegadores web son los encargados de interpretar este lenguaje.
- Los navegadores web no estan actualizados con la misma version del EMACScript.

---

## Hello World

    console.log('Hello World!'):

En este caso ```console``` es un objeto que mediante el ```.``` llama a su metodo ```log```.

---

## document

    document.write('Hello World!'):

El objeto ```document``` hace referencia a todo el documento ```HTML```.

---

## NodeJS

Node nos permite interpretar JavaScript fuera del navegador.

---

## Variables y Comentarios

```Comentarios:``` Son lineas de codigo que el interprete de JavaScript ignorara a la hora de ejecutarlo.

    // Esto es un comentario de una sola linea.

    /*
        Esto es un comentario
        de multiples lineas.
    */

```Variable:``` Es un contenedor de informacion que apunta a un lugar en memoria. Dicha informacion puede cambiar en el futuro.

```
let a = 10, b = 20;
var c = 10;
const d = 10;
```
Para inicializar una variable se pueden utilizar las palabras reservadas ```var``` y ```let```.

- Uno de los problemas con la declaracion de ```var``` es que nos permite remplazar propiedades y objetos propios del objeto global ```window```.
- El ```let``` y el ```const``` no sobre escriben las variables que se encuentran en el objeto global ```window``` o donde sea que este corriendo JS.

Las constantes ```const``` hace referencia a un lugar en memoria que no va poder cambiar.

---

## Consola

- Los mensajes en consola son utilizados para no interferir cons el flujo normal del programa.
```
console.log('Mensaje normal'):
console.warn('Mensaje precaucion-alerta'):
console.error('Mensaje de error'):
console.info('Mensaje de informacion'):
console.table({ a, b, c, d, x }):
```
---

## Lugar y Orden de las importaciones de archivos JS

Los archivos ```.js``` deben de importarse al final del ```body``` en el archivo ```.html```, de esta forma cargara todo y el final se aplicara el JS. Ademas puede haber funciones o partes del codigo que interrumpan la carga del ```HTML``` y ```CSS```.

---

## Prompt, confirm y alert

```prompt```, ```confirm``` y ```alert``` son 3 formas de ingresar datos por parte del usuario.

---

## Window - Global

 - ```window``` es el objeto global en un navegador.
 - ```global``` es el objeto global en node.

 ```window``` y ```global``` no contienen exactamente lo mismo pero su proposito si es el mismo.

---

## Tipos de datos primitivos

JavaScript es un lenguaje debilmente tipado.

```Primitivos```: Es una informacion que no es un objeto y son inmutables.
Existen 6 tipos de datos primitivos:

| Tipo |  | Descripcion |
| :-- | :--: | :-- |
| ```Boolean``` | - | true / false |
| ```Null``` | - | Sin valor en lo absoluto |
| ```Undefined``` | - | Una variable declarada que aun no se le asigna valor |
| ```Number``` | - | integer, floats, etc. |
| ```String``` | - | Una cadena de caracteres, ej: Palabras, nombre de persona |
| ```Symbol``` | - | Es un valor unico que no es igual a ningun otro valor |

Para saber de que tipo es una variable podemos usar el operador ```typeof```.

---

## Palabras reservadas y nombre de variables

Son palabras que tienen un uso especifico.

El nombre de los archivos debe de ser en minusculas, y en caso de ser dos o mas palabras, estas se deben dividir por un ```-```. ej: ```nombre-archivo.js```

La declaracion de variables en JavaScript tiene por estandar: 
- Que sean en ```camelCase```
- No deben comenzar con numeros
- No deben contener ```.```
- No deben contener caracteres especiales
- El ```_``` se debe de usar preferentemente para separar numeros de palabras

Para los nombres de clases ```class``` los nombres deben de ser ```UpperCamelCase```.

|      |      | Palabras reservadas |      |      | 
| :--: | :--: | :--: | :--: | :--: |
| break | export | super | case | extends |
| switch | catch | finally | this | class |
| for | throw | const | function | try |
| continue | if | typeof | debugger | import |
| var | default | in | void | delete |
| instanceof | while | do | new | with |
| else | return | yield | let |  |

|  |  | Palabras reservadas en un futuro |  |  |
| :--: | :--: | :--: | :--: | :--: |
| enum | package | public | implements | private |
| static | interface | protected | await |  |

|  |  | Evitar usar |  |  |
| :--: | :--: | :--: | :--: | :--: |
| null | undefined | true | false | hasOwnProperty |
| isNaN | Infinity | isFinite | NaN | length |
| Math | isPrototypeOf | prototype | valueOf | name |
| Number | Object | String | toString | prompt |
| alert | conform |  |  |  |

---

## Arreglos

Son un objeto muy parecido a una lista de informacion, que contienen un grupo de elementos.
Usualmente, esa informacion dentro del arreglo es del mismo tipo de dato.
- En JavaScript cada vez que haya ```[]``` es un arreglo.
- Los arreglos en JavaScript comienzan con el indice ```0```.

Para obtener la longitud de un arreglo se usa:

    arr.length

Para recorrer un arreglo se utiliza el ```.forEach()```

Para insertar un nuevo elemento al ```final``` del arreglo se utiliza el metodo ```.push()```

Para insertear un nuevo elemento al ```principio``` del arreglo se utiliza el metodo ```unshift()```

Para borrar el ultimo elemento del arreglo se utiliza ```.pop()```

Para borrar un elemento en especifico se utiliza el ```.splice(start, deleteCount)```

Para encontrar el numero de indice de un elemento se utiliza ```.indexOf(searchElement)```

---

## Objetos literales

Son los tipos de datos que no son primitivos. Es una variable-objeto que tiene pares de valores. ej:

```
let personaje = {
    nombre: 'Steve Rogers',
    codeName: 'Captain America',
    vivo: true,
    edad: 85,
    coords: {
        lat: 34.034,
        lng: -118.70,
    },
    suits: ['Avenger', 'Winter Soldier', 'Civil War'],
}
```
En este ejemplo ```nombre``` es la ```llave(key)``` y ```'Steve Rogers'``` el ```valor(value)```.


---



---

## Glosario:
- ```Metodo```: Una funcion que se encuentra dentro de un objeto.
- ```Polyfill```: Es un codigo que provee el funcionamiento de una nueva caracteristica de JavaScript (ES6), en versiones viejas como ES5.

