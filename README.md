# ProyectosWeb3

Este repositorio contiene un proyecto básico de **Web3** desarrollado y desplegado en la blockchain de **Sepolia Testnet**.

## Proyecto I

## Descripción

El proyecto incluye un contrato inteligente simple escrito en **Solidity**, el cual fue compilado y desplegado utilizando **Remix IDE** y gestionado mediante **Metamask**.

## Tecnologías utilizadas

- Solidity
- Remix IDE
- Metamask
- Sepolia Testnet
- Git & GitHub

## Contrato desplegado

- Dirección del contrato: `0x6961c0bfbad6e8f54c6a2a0377c4f4b6306445a0`
- Transaction Hash del deploy: `0x59db85744b92a3f58a3d647b55d1354b045033b16a8298a10be03fd509acb548`

## Cómo interactuar con el contrato

- Ingresar a [Etherscan de Sepolia](https://sepolia.etherscan.io/)
- Pegar la dirección del contrato en la barra de búsqueda
- Desde la pestaña **Contract** se puede verificar, leer y escribir funciones según lo permita el contrato.

## Clonar el repositorio

Para clonar el repositorio en tu máquina local:

git clone https://github.com/Maty910/ProyectosWeb3.git

## Próximos pasos

- Mejorar la lógica del contrato inteligente
- Agregar pruebas automáticas
- Integrar con una aplicación frontend

# Proyecto II - ToDoList

Este contrato inteligente en Solidity implementa una lista de tareas (ToDo List) que permite a los usuarios organizar sus pendientes en la blockchain.  
A través de este proyecto se ponen en práctica conceptos más avanzados de Solidity como **structs, arrays dinámicos, variables globales, funciones hash, eventos y estructuras de control**.

## Características principales

- Añadir nuevas tareas con descripción y marca de tiempo (`block.timestamp`).
- Eliminar tareas completadas mediante comparación de strings con `keccak256` y `abi.encodePacked`.
- Consultar todas las tareas almacenadas en el contrato.
- Uso de eventos para notificar al cliente cuando se añade o elimina una tarea.

## Clonar y usar el proyecto

Clonar el repositorio:

git clone https://github.com/Maty910/ProyectosWeb3.git

Abrir el contrato en [Remix IDE](https://remix.ethereum.org/):

1. Copiar el archivo `ToDoList.sol` en la carpeta `contracts/` de Remix.  
2. Compilar con el compilador **Solidity 0.8.26**.  
3. Desplegar el contrato usando la red **Sepolia Testnet** conectada a MetaMask.  
4. Interactuar desde la pestaña **Deploy & Run Transactions**:
   - `setTarea(string)` → Añadir tarea.
   - `eliminarTarea(string)` → Eliminar tarea completada.
   - `getTarea()` → Listar tareas almacenadas.

## Contrato desplegado

- Dirección del contrato: `0x6edd2c66811e2994375230caefce6ec96dc62ad8`
- Enlace al Block Explorer (Etherscan Sepolia): `*[a completar]*`  

## Temas abordados

Este proyecto práctico abarca:

- Structs  
- Asignación de datos  
- Tipos de datos: Valor y Referencia  
- Arrays  
- Variables globales  
- Estructuras de control y flujo  
- Operadores de incremento y comparación  
- Función Hash y Función ABI  
- Buenas prácticas de desarrollo  

