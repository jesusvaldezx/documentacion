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


## Glosario:
- ```Metodo```: Una funcion que se encuentra dentro de un objeto.
- ```Polyfill```: Es un codigo que provee el funcionamiento de una nueva caracteristica de JavaScript (ES6), en versiones viejas como ES5.

