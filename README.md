# Smart Contracts – Curso Solidity

Este repositorio contiene distintos proyectos desarrollados como parte del aprendizaje en **Solidity** y **contratos inteligentes**.  
Cada proyecto aborda un conjunto de conceptos fundamentales para la construcción de dApps en la blockchain de Ethereum.

---

## 📂 Contenido del repositorio

- **Proyecto I – SimpleStorage**  
  Contrato inteligente básico que almacena y recupera un valor.  
  Conceptos clave:  
  - Tipos de datos simples (uint256, string, address)  
  - Funciones getter/setter  
  - Variables globales  
  - Fundamentos de almacenamiento en la blockchain  

- **Proyecto II – ToDoList**  
  Contrato que implementa una lista de tareas.  
  Conceptos clave:  
  - Uso de `struct` y arrays dinámicos  
  - Variables globales (`block.timestamp`)  
  - Control de flujo (`for`, `if`)  
  - Comparación de strings con `keccak256`  
  - Eventos (`emit`)  
  - Buenas prácticas en el diseño de contratos  

---

## 🚀 Deploys en Sepolia

- **Proyecto I – SimpleStorage**  
  - Dirección del contrato: `0x...`  
  - Tx Hash: `0x...`

- **Proyecto II – ToDoList**  
  - Dirección del contrato: `0x5456861ef3d10d95255a25176b5c16f0443e068a2b87eb347d6ee686b7da6d96`  
  - Tx Hash: `0x6eDD2C66811e2994375230caefCE6Ec96dc62aD8`

---

## 🛠️ Cómo probar los contratos

1. Ir a [Remix IDE](https://remix.ethereum.org/)  
2. Compilar el contrato (`.sol`) en la versión indicada  
3. Usar la pestaña **Deploy & Run** con la red **Sepolia**  
4. Conectar una wallet (MetaMask)  
5. Interactuar con las funciones expuestas en la interfaz de Remix  

También es posible interactuar con los contratos ya desplegados desde **[Sepolia Etherscan](https://sepolia.etherscan.io/)**, pegando la dirección del contrato y utilizando las secciones **Read Contract** y **Write Contract**.

---

## 📌 Próximos pasos

- Añadir **pruebas automatizadas** (Hardhat / Foundry)  
- Mejorar la lógica de los contratos con nuevas funcionalidades  
- Desplegar interfaces frontend (React / Next.js) para interactuar con los contratos  
- Documentar patrones de diseño y seguridad en Solidity  

---

## 👨‍💻 Autor

Desarrollado por Matías Chacón – Desarrollador FullStack.  
El repositorio es parte del proceso de formación en desarrollo blockchain.  

