
# INTRODUCCIÓN

> Redux en Angular se usa para manejar el <strong style="color: orange;">estado global</strong> de una aplicación de manera predecible y eficiente. En pocas palabras, ayuda a <strong style="color: orange;">organizar y controlar los datos</strong> de la app para que diferentes componentes puedan acceder a ellos sin necesidad de pasarlos manualmente.

Nos va apermitir conocer ¿cual es el estado de la aplicación?, ¿como se encuentra determinada variable?, ¿como cambio la informació y en que momento?

<div style="border: 1px solid purple; padding: 10px; border-radius: 6px; margin: 10px 0;">
  Redux (NgRx en Angular) ayuda a <span style="color: purple; font-weight: bold; ">manejar el estado de la aplicación</span> de forma eficiente, evitando problemas con la gestión de datos y mejorando la escalabilidad. 🚀
</div>

## <strong style="color: blue;">🔹¿Para qué sirve en Angular?</strong>
Angular usa una librería llamada NgRx, que es una implementación de Redux adaptada a Angular. Se utiliza para:

- Centralizar los datos en un solo lugar (Store).
- Evitar cambios de estado desordenados y hacerlos más predecibles.
- Facilitar la comunicación entre componentes sin necesidad de muchos @Input() y @Output().
- Mejorar el rendimiento, ya que evita recargas innecesarias en la UI.

## <strong style="color: blue;">🔹 Ideas principlaes</strong>
- Toda la data de la aplicación se en cuentra en una estructura <strong style="color: orange;">previemente DEFINIDA </strong> . Es decir, antes de que nosotros realizemos algun cambio, nosotros ya sabemos de antemano que es lo que se va alamacenar en la misma
- Toda la información se encontrará lamacenada en un único lugar llamado <strong style="color: orange;">STORE</strong>
- El estor <strong style="color: orange;">nuNca</strong> se modifica de forma directa
- Cualquier iteracción del usuario y/o código dispara acciones que describen que sucedió. POdremos saber que código cambio, como y donde, además de porder revertirlo.
- El valor actual de la app se llama <strong style="color: orange;">STATE</strong>
- Un nuevo estado es creado, en base a la combienación del viejo estado y una acción (describe lo que va a suceder) y todo es flujo se hace a través de un afunción llamada <strong style="color: orange;">REDUCER()</strong>. El reducer toma la accion y el viejo estado como argumentos y entonces genera un nuevo estado.

## <strong style="color: blue;">🔹¿Cómo funciona? ACTION - REDUCER - STATE - STORE</strong> 
- <strong style="color: orange;">Store:</strong> Un lugar donde se guardan los datos globales de la app.
- <strong style="color: orange;">Actions:</strong> Eventos que indican qué cambios deben ocurrir en el estado. Es la única funte de información  ue se envía por interacciones de usuario o programa. Por lo general se busca que sean lo más simples posibles. 
Tienen 2 propiedades:
    - **type<obligatorio>** (completar_tarea).
    - **payload<opcional>** (la menos cantidad de información posible para completar la tarea)

- <strong style="color: orange;">reducer:</strong>Funciones puras que actualizan el estado basándose en las acciones. Recibe 2 argumentos y <strong style="color: orange;">SIEMPRE retorna un STATE</strong>
    - **oldState<obligatorio>:** Es el estado actual de la aplicación.
    - **action<obligatorio>:** Es un objeto plano que indica que hay que hacer. Deben ser lo más simples posibles.
- Selectors (selectores): Permiten obtener datos del estado de forma optimizada.

## 🔹Ejemplo simple:
Si tienes una app de carrito de compras:

1. El Store guarda los productos añadidos.
2. Un Action puede ser "Agregar producto".
3. El Reducer recibe esa acción y actualiza la lista de productos.
4. Un Selector permite que cualquier componente acceda a los productos en el carrito.




