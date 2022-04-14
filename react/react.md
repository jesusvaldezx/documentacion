# React

* Libreria
* Declarativa
* Eficiente
* Predecible
* Componentes
* Server-side con Node
* Aplicaciones moviles con React Native

La libreria ```react-dom``` es la que se encarga de la parte del ```html``` en ```react``` mediante el objeto ```ReactDOM```. 

---
## Babel

Babel funciona en el background y nos permite utilizar caracteristicas actuales de JavaScript y convertirlas a las que le navegador soporta.

[Link al sitio oficial de Babel](https://babeljs.io/)

---

## Create React App

Para crear una aplicacion en react, se escribe el siguiente comandoÑ

    npx create-react-app nombreApp

Para ejecutar la aplicacion se utiliza el comando:

    npm start

[Link a doc oficial del comando](https://create-react-app.dev/)

---

## Componente
Es una pieza de codigo encapsulada re-utilizable que puede tener estado o no.

El nombre de los componenes se declara en ```UpperCamelCase```.

Hay dos tipos de componentes:

- Los que estan basados en ```clases```.
- Los que estan basados en ```funciones```.

Para ***React*** lo correcto es trabajar en base a ***funciones***.

JavaScript solo puede retornar un objeto a la vez. por lo cual se utiliza la etiqueta ```<Fragment>``` para solucionar esto. ej:
```
 return (
    <Fragment>
        <h1>Hello World</h1>
        <p>My first aplication</p>
    </Fragment>
); 
```
## Impresion de variables en HTML

Para imprimir variables en HTML se utilizan los ```{}```, los cuales funcionan bien para datos primitivos.

---
## Propiedades (Props)

Es la forma en la que mandamos informacion entre componentes.

- ```PropTypes``` nos ayuda a forzar a las propiedades a un tipo de dato y ser requeridas.

    ```
    PrimeraApp.propTypes = {
        ejemplo: PropTypes.string.isRequired,
    }
    ```

- ```DefaultProps```Noa ayuda a darle un valor por defecto a las propiedades.

    ```
    PrimeraApp.defaultProps = {
        ejemplo: 'I\'m a example.',
    }
    ```

---



---
---




