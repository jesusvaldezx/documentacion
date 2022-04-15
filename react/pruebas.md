# Pruebas Unitarias y de Integracion

## Unitarias:
Enfocadas en pequenas funcionalidades.

## Integracion:
Enfocadas en como reaccionan varias piezas en conjunto.

---

## Caracteristicas de las pruebas
- Faciles de escribir
- Faciles de leer
- Confiables
- Rapidas
- Principalmente unitarias

---

## Pasos a seguir en las pruebas (AAA)
* __Arrange__ (Arreglar): Es el paso en el que establecemos el estado inicial. Tambien se conoce como el sujeto a probar.
    - Inicializamos variables.
    - Importaciones necesarias.
    - Preparamos el ambiente a probar.
* __Act__ (Actuar): Aplicamos acciones o estimulos al sujeto de pruebas.
    - LLamar metodos.
    - Simular clicks.
    - Realizar acciones sobre el paso anterior.
* __Assert__ (Afirmar): Observar el comportamiento resultante.
    - Son los resultados esperados.
    - Ej: Que algo cambie, algo incremente o bien que nada suceda.

---

## Archivos Test

El nombre de los archivos de prueba es indiferente pero deben de tener la extencion:
```
.test.js
```

---

## Ejecucion de Pruebas

```
    npm run test
```

---

## Test Suites

Se puede considerar como __test suits__ a cada uno de los __archivos de pruebas__.

---

## Funcion expected()

Con la funcion ```expected()``` podemos evaluar si el resultado de la prueba es correcto. En ella se envia como parametro lo que esparamos de resultado de la prueba y con ayuda de las siguientes funciones __comparamos si lo que obtenemos de resultado es igual a lo que esperamos.__

* ```.toBe()```: Compara si dos resultados son iguales.
* ```.toStrictEqual()```: Compara si dos objetos son iguales.

---

## JEST

Es una libreria para hacer pruebas en JavaScript. [Esta es su documentacion oficial.](https://jestjs.io/)

