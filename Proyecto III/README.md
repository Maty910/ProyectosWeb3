# Proyecto III – Donations

## 📌 Descripción
El contrato **Donations** es un contrato inteligente educativo que permite a los usuarios realizar donaciones en Ether y a un beneficiario retirarlas posteriormente.  
El proyecto aborda conceptos fundamentales de Solidity, como **mappings, manejo de Ether, control de acceso y manejo de errores**.

Este contrato **no debe usarse en producción**, ya que está diseñado con fines didácticos.

---

## 🎯 Objetivos
Con este proyecto trabajamos los siguientes temas:

- Funciones `private`, `internal`, `pure` y `payable`  
- `Mappings`  
- `address`  
- Control de acceso  
- Manejo de errores personalizados  
- Manejo de Ether (envío y recepción)  
- Transferencias de Ether mediante `call`  

---

## 📂 Estructura del Contrato

- **Variables**
  - `i_beneficiario`: Dirección inmutable que puede retirar los fondos.
  - `s_doacoes`: Mapping que guarda el total donado por cada usuario.

- **Eventos**
  - `Donations_DoacaoRecebida`: Se emite cuando un usuario dona.
  - `Donations_SaqueRealizado`: Se emite cuando el beneficiario retira fondos.

- **Errores**
  - `Donations_TrasacaoFalhou`: Falla en la transferencia de Ether.
  - `Donations_SacadorNaoPermitido`: Cuando alguien distinto al beneficiario intenta retirar.

- **Funciones**
  - `constructor(address _beneficiario)`: Define al beneficiario.
  - `receive() external payable`: Permite recibir Ether directamente.
  - `fallback() external`: Fallback vacío para llamadas inválidas.
  - `doe() external payable`: Permite donar Ether y lo suma al mapping.
  - `saque(uint256 _valor) external`: Permite al beneficiario retirar fondos.
  - `_transferirEth(uint256 _valor) private`: Maneja la transferencia con `call`.

---

## 🚀 Cómo Ejecutar el Proyecto

Clonar el repositorio:

```
git clone https://github.com/Maty910/ProyectosWeb3.git
cd ProyectosWeb3/Proyecto\ III
```

Abrir en **Remix IDE** o en tu editor de preferencia.  
Compilar con **Solidity 0.8.26**.  
Desplegar el contrato en una red de prueba (ej. Sepolia Testnet).  

En el constructor, pasar la dirección del **beneficiario**.  

Probar funciones:  
- **doe()**: Donar Ether desde cualquier dirección.  
- **saque()**: Retirar Ether (solo el beneficiario).  

---

## 🔗 Contrato en Block Explorer
- **Transaction Hash (deploy):** `0x81feeda9e6ae376bfb376ac7178fe6510c33a499073d1781deb1d48e77720607`
- **Dirección del contrato:** 👉 `0x872a3eb7fe04eb6453dcef7260dae2e9cf1a3d29`

---

## ✅ Conclusiones
Este proyecto permite comprender cómo:
- Usar `mappings` para llevar un registro de donaciones.
- Implementar funciones `payable`.
- Aplicar control de acceso con `require`/`revert`.
- Manejar errores personalizados (`error`).
- Recibir y transferir Ether de forma segura.
