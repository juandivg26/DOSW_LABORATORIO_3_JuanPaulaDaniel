# Scrum Work Breakdown — El Restaurante (Comida Rápida)

# ÉPICA

**EPIC-01** — Gestión del ciclo de pedidos del restaurante de comida rápida


**Descripción:** Agrupa el flujo completo de una orden: armar el pedido (RF-02), confirmarlo y enviarlo a cocina (RF-03), y gestionar su preparación (RF-04), con la participación de cliente, mesero y cocina. Por su alcance, no cabe en un solo sprint.


---

# FEATURE 1 — Armado del pedido (RF-02)

**FEAT-01** — Armado del pedido


**Descripción:** Capacidad que permite al cliente y al mesero agregar, eliminar y modificar productos de un pedido mientras la cuenta de la mesa esté abierta. La confirmación del pedido hacia cocina y el pago quedan fuera de este feature.

---

## HU-01 — Armar y modificar el pedido

**Historia:** Como cliente, quiero agregar, eliminar y modificar productos de mi pedido mientras la cuenta esté abierta, para armar mi orden de acuerdo con lo que deseo solicitar.

**Criterios de aceptación:**

- **Dado** que la mesa tiene una cuenta abierta y el producto está disponible, cuando agrego el producto al pedido, entonces el sistema lo incorpora y conserva el precio que tenía en el momento de agregarlo, aunque posteriormente cambie el precio en la carta (RN-02).
- Dado que el pedido ya pasó a estado EN PREPARACIÓN, cuando intento agregar, eliminar o modificar un producto, entonces el sistema rechaza el cambio y mantiene el pedido sin modificaciones (RN-01).

**Prioridad:** Alta — RF-02 fue priorizado como Alta en el análisis crítico de la Parte 3, debido a que permite construir y modificar las órdenes del restaurante.

| Story Points | 5 |

### Subtareas

- **ST-01** — Implementar la gestión de ítems del pedido para agregar, eliminar y modificar productos.
- **ST-02** — Validar la disponibilidad del producto, la cuenta abierta y el estado del pedido antes de realizar modificaciones.
- **ST-03** — Implementar la aplicación de las reglas de precio congelado y actualización del total del pedido.

---

## HU-02 — Gestionar el pedido de una mesa

**Historia:** Como mesero, quiero agregar, eliminar y modificar productos en el pedido de una mesa, para registrar correctamente lo solicitado por los clientes durante la atención.

**Criterios de aceptación:**

- Dado que la mesa tiene una cuenta abierta y el producto está disponible, cuando agrego el producto al pedido, entonces el sistema lo incorpora al pedido activo de la mesa y conserva su precio en el momento de agregarlo.
- Dado que un producto no tiene disponibilidad, cuando intento agregarlo al pedido, entonces el sistema bloquea la operación y permite seleccionar otro producto disponible.
- Dado que el pedido se encuentra en estado EN PREPARACIÓN, cuando intento modificarlo, entonces el sistema rechaza la modificación.

**Prioridad:** Alta — RF-02 involucra directamente al mesero en la creación y modificación de pedidos, por lo que esta capacidad es necesaria para soportar el flujo de atención del restaurante.

| Story Points | 3 |

### Subtareas

- **ST-04** — Implementar la gestión de ítems del pedido para que el mesero pueda agregar, eliminar y modificar productos.
- **ST-05** — Validar disponibilidad, cuenta abierta y estado del pedido antes de permitir modificaciones.
- **ST-06** — Implementar la interfaz de gestión del pedido para el mesero.

---

# FEATURE 2 — Confirmación y preparación del pedido (RF-03, RF-04)

**FEAT-02** — Confirmación y preparación del pedido

**Descripción:** Capacidad que permite confirmar el pedido y enviarlo a cocina, y que el personal de cocina gestione su estado de preparación. El armado del pedido y el pago quedan fuera de este feature.

---

## HU-03 — Confirmar pedido y enviarlo a cocina

**Historia:** Como cliente o mesero, quiero confirmar el pedido y enviarlo automáticamente a cocina, para que la preparación inicie sin demoras.

**Criterios de aceptación:**

- Dado que el pedido contiene al menos un producto disponible, cuando lo confirmo, entonces el sistema cambia su estado a RECIBIDO y lo envía al tablero de cocina (RN-05).
- Dado que un producto del pedido se agotó justo antes de confirmar, cuando intento confirmarlo, entonces el sistema bloquea la confirmación y solicita modificar el pedido antes de enviarlo.

**Prioridad:** Alta — RF-03 fue priorizado como Alta en el análisis crítico de la Parte 3, porque conecta la solicitud del cliente o mesero con el proceso de preparación en cocina.

| Story Points | 2 |

### Subtareas

- **ST-07** — Implementar la operación de confirmación del pedido para enviarlo a cocina.
- **ST-08** — Validar que todos los productos del pedido continúen disponibles antes de confirmar.
- **ST-09** — Cambiar el estado del pedido a RECIBIDO y enviarlo al tablero de cocina.

---

## HU-04 — Cambiar el estado del pedido

**Historia:** Como personal de cocina, quiero cambiar el estado de un pedido, para que el restaurante pueda conocer y controlar el avance de su preparación hasta la entrega.

**Criterios de aceptación:**

- Dado que un pedido está en RECIBIDO, cuando el personal de cocina lo marca como EN PREPARACIÓN, entonces el sistema actualiza el estado y el pedido deja de poder modificarse.
- Dado que el personal de cocina cambia el estado de un pedido, cuando se guarda el cambio, entonces el sistema registra el usuario responsable y la fecha del cambio (RN-07).

**Prioridad:** Media — RF-04 fue priorizado como Media en el análisis crítico de la Parte 3, porque es necesario para controlar la preparación, pero depende de que previamente existan pedidos confirmados.

| Story Points | 3 |

### Subtareas

- **ST-10** — Implementar la operación para cambiar el estado del pedido.
- **ST-11** — Validar las transiciones permitidas: RECIBIDO → EN PREPARACIÓN → LISTO → ENTREGADO, según RN-06.
- **ST-12** — Registrar en el historial el usuario y la fecha de cada cambio de estado, según RN-07.

---

# Resumen de prioridades

| Historia | RF trazado | Prioridad | Feature |
|---|---|---|---|
| HU-01 — Armar y modificar el pedido | RF-02 | Alta | FEAT-01 |
| HU-02 — Gestionar el pedido de una mesa | RF-02 | Alta | FEAT-01 |
| HU-03 — Confirmar pedido y enviarlo a cocina | RF-03 | Alta | FEAT-02 |
| HU-04 — Cambiar el estado del pedido | RF-04 | Media | FEAT-02 |



## PLANNING POKER
[Ver grabación de la estimación](https://drive.google.com/file/d/1yVfTMcWP48FxcfJTUduJDUVYESF0P4hb/view?usp=sharing)
