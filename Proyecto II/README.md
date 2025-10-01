# Proyecto II – ToDoList

Este contrato inteligente en Solidity implementa una lista de tareas (ToDo List).  
Sirve como ejercicio práctico para aplicar conceptos fundamentales de Solidity como **structs, arrays dinámicos, variables globales, eventos y funciones hash/ABI**.

## Descripción del contrato

- Estructura `Tarea` con campos:
  - `descripcion` (string)
  - `tiempoDeCreacion` (uint256)
- Array dinámico `s_tareas` para almacenar todas las tareas.
- Función `setTarea(string)` para añadir una tarea — se registra la descripción y el timestamp (`block.timestamp`).
- Función `eliminarTarea(string)` para eliminar la tarea que coincide (por descripción), usando `keccak256(abi.encodePacked(...))` para comparar strings.
- Función `getTarea()` que devuelve el array completo de tareas almacenadas.
- Eventos:
  - `ToDoList_TareaAnadida` (descripcion, tiempoDeCreacion)
  - `ToDoList_TareaCompletadaYEliminada` (descripcion)

## Contrato desplegado

- Dirección del contrato ToDoList: **0x5456861ef3d10d95255a25176b5c16f0443e068a2b87eb347d6ee686b7da6d96**  
- Transaction Hash del deploy: **0x6eDD2C66811e2994375230caefCE6Ec96dc62aD8**

## Cómo interactuar con el contrato

1. Ir a [Sepolia Etherscan](https://sepolia.etherscan.io/)  
2. Pegar la dirección del contrato en la búsqueda  
3. En la pestaña **Read Contract**, ejecutar `getTarea()` para ver las tareas actuales  
4. En **Write Contract**, conectar una wallet (MetaMask) y usar:  
   - `setTarea(string descripcion)` para añadir tareas  
   - `eliminarTarea(string descripcion)` para borrar una tarea  

También podés interactuar desde Remix una vez desplegado:  
- Bajo *Deployed Contracts* seleccioná la instancia y llamá las funciones directamente.

## Temas que aborda este proyecto

- Structs y asignación de datos  
- Tipos de datos por valor y referencia  
- Arrays dinámicos  
- Uso de variables globales (`block.timestamp`)  
- Estructuras de control (`for`, `if`)  
- Operadores de incremento y comparación  
- Comparación de strings con hash (`keccak256` + `abi.encodePacked`)  
- Eventos y buenas prácticas de contrato  

## Próximos pasos sugeridos

- Agregar un campo booleano `completa` a la `Tarea` para marcar tareas sin borrarlas  
- Filtrar tareas según estado (pendientes / completadas)  
- Escribir pruebas automáticas (Hardhat / Foundry)  
- Crear una interfaz frontend (React, Vue, etc.) para interactuar con el contrato desde el navegador  
