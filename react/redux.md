# REDUX

Cuatro estructuras de redux, ```[Action, Reducer, State, Store]```.

---

## Action

Es la unica fuente de informacion que se envia por interacciones de usuario o programa. Por lo general, se busca que las acciones sean lo mas simples posibles.

Las acciones buscan ser lo mas simple posible, se debe buscar no tener mucha logica en ellas.

Las acciones tienen unicamente 2 propiedades:
* ```type:``` Describe que es lo que quiere hacer o cual es la tarea que debe completar(COMPLETAR_TAREAS).
* ```payload:``` Es opcional ya que no siempre tendremos que mandar informacion para realizar alguna accion. Es la menor cantidad posible de informacion para realizar dicha tarea.

---

## Reducer

Es una funcion que recibe dos argumentos y siempre debe de retornar un estado.

#### Algumentos:
* ```oldState:``` Es el estado actual de la aplicacion.

    ```
    {
        visibilityFilter: 'MOSTRAR_TODOS',
        todos: [
            {
                text: 'Hacer la tarea.',
                completed: true,
            },
            {
                text: 'Ver una pelicula.',
                completed: false,
            }
        ]
    }
    ```

* ```action:``` Es un objeto plano que indica que hacer.

    ```
    {
        type: COMPLETAR_TAREA,
        index: 1
    }
    ```
    En este caso, tiene como objetivo completar la tarea cuya posicion index sea igual a 1.

    Cuando el ```Reducer``` toma el viejo estado y la accion ```pruduce un nuevo estado.``` 

    ```
    {
        visibilityFilter: 'MOSTRAR_TODOS',
        todos: [
            {
                text: 'Hacer la tarea.',
                completed: true,
            },
            {
                text: 'Ver una pelicula.',
                completed: true,
            }
        ]
    }
    ```
    En este caso marca como ```Ver una pelicula.``` como ```true```.

---

## State

Reglas que debe de cumplir el ```State```:

* El State es de solo lectura.
* Nunca se mutara el state de forma directa.
* Hay funciones que estan prohibidas de Javascript.
    Por ejemplo:
    - Push.
    - Manipulacion directa del objeto oldState.


---

## Store

Tiene las siguientes responsabilidades:

* Contiene el estado de la aplicacion.
* Permite la lectura del estado via: ```getState[]```.
* Permite crear un nuevo estado utilizando: ```dispatch[ACTION]``` y le mandamos una accion.
* Permite notificar cambios de estado via: ```subscribe[]```.

---

## Resumen

* ```ACTION```: Describen que es lo que vamos a hacer.
* ```REDUCER```: Toma el estado anterior y una accion y produce un nuevo estado. 
* ```STATE```: Es como se encuentra la informacion actualmente.
* ```STORE```: Se va a encargar de gestionar todo por nosotros.

---

### NOTA: 
Todos los objetos en Javascript son pasados por referencia, esto hace que cuando se modifique un objeto siemprese mantenga la referencia al objeto original.

Se debe de prevenir que los estados sean inmutableas y que solo se creen nuevos estados.  