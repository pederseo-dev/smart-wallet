# Physical Wallet P2P Miner (NVP)

## Descripción

Este proyecto es un **concepto de wallet física para criptomonedas** que funciona como un **nodo P2P de cómputo distribuido**.
La wallet, inicialmente implementada en una **PC**, ofrece su capacidad de cómputo a una red P2P mientras está conectada a Wi-Fi.
A cambio, recibe **recompensas en criptomonedas** por procesar tareas enviadas por usuarios que necesitan entrenamiento de modelos u otras tareas computacionales.

**Idea central:** una wallet que **mina criptomonedas de manera pasiva mientras la llevas conectada a tu red**, sin necesidad de pagos directos o interacción compleja.

---

## Funcionalidades

* **Almacenamiento seguro de criptomonedas**

  * Puede usar **MetaMask** como wallet para gestionar claves y transacciones.
* **Cómputo distribuido**

  * Participa en la ejecución de tareas fraccionadas enviadas por clientes.
  * No requiere baja latencia; cada wallet contribuye a su propio ritmo.
* **Recompensas automáticas**

  * Un **smart contract** registra las tareas y distribuye el fee proporcionalmente a las wallets que completan su trabajo.
* **Red P2P**

  * Comunicación entre wallets mediante **UDP**.
  * Soporta **hole punching** a través de Wi-Fi o tethering para superar NAT móviles.

---

## Arquitectura

1. **Cliente**

   * Quiere entrenar modelos o realizar cálculos.
   * Paga un fee al smart contract asociado.

2. **Smart Contract**

   * Fragmenta las tareas en chunks.
   * Mantiene un registro de contribuciones de cada wallet.
   * Distribuye recompensas automáticamente.

3. **Wallet / Nodo P2P**

   * Procesa los chunks recibidos desde la red P2P.
   * Envía resultados de vuelta para validación.
   * Recibe recompensas en la wallet física o MetaMask.

4. **Red P2P**

   * Coordina la distribución de chunks.
   * Permite que wallets se conecten entre sí, incluso detrás de NATs móviles.

---

## Roadmap

**Fase 1 (NVP)**

* Wallet física en PC conectada a Wi-Fi.
* Procesamiento de tareas fraccionadas desde la red P2P.
* Distribución de recompensas vía smart contract.

**Fase 2**

* Wallets en smartphones con sistema operativo propio.
* Escalado a miles de nodos móviles.
* Optimización del cómputo distribuido y seguridad adicional.

**Fase 3 (opcional)**

* Integración de pagos contactless en POS.
* Wallet física híbrida tipo cartera que también almacena tarjetas físicas.

---

## Requisitos

* **Hardware:** PC con conexión Wi-Fi.
* **Software:**

  * Node.js / Python (dependiendo de la implementación P2P).
  * MetaMask para la gestión de criptomonedas.
  * Cliente P2P compatible con UDP.
* **Blockchain:** Smart contract en Ethereum o testnet compatible.

---

## Licencia

Proyecto conceptual – uso y modificación libre para prototipos y pruebas.

