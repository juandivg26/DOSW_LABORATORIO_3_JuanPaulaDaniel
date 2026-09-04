# Jira — El Restaurante (Comida Rápida)


# 1. Épica

| Campo                   | Valor                                                                                                                                                                                                                                                                                                   |
| ----------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| ID interno              | `EPIC-01`                                                                                                                                                                                                                                                                                               |
| Tipo                    | Epic                                                                                                                                                                                                                                                                                                    |
| Título                  | Gestión del ciclo de pedidos del restaurante de comida rápida                                                                                                                                                                                                                                           |
| Descripción             | Centralizar la gestión del ciclo de vida de los pedidos del restaurante de comida rápida, desde su armado y confirmación hasta el envío a cocina y actualización de su estado (RF-02, RF-03, RF-04). Por involucrar a tres roles distintos y varias capacidades del sistema, no cabe en un solo sprint. |
| Requisitos relacionados | RF-02, RF-03, RF-04                                                                                                                                                                                                                                                                                     |
| Concepto                | Comida rápida                                                                                                                                                                                                                                                                                           |
| Etiqueta                | `comida-rapida`                                                                                                                                                                                                                                                                                         |
| Fecha de inicio         | 03/09/2026                                                                                                                                                                                                                                                                                              |
| Fecha límite            | 18/09/2026                                                                                                                                                                                                                                                                                              |
| Jira Issue Key          | **DOSW3-1**                                                                                                                                                                                                                                                                                             |
| Evidencia               | Pendiente de captura                                                                                                                                                                                                                                                                                    |

---

# 2. Features

## FEAT-01 — Armado del pedido

| Campo                 | Valor                                                                                                                                                 |
| --------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------- |
| ID interno            | `FEAT-01`                                                                                                                                             |
| Tipo                  | Feature                                                                                                                                               |
| Título                | Armado del pedido                                                                                                                                     |
| Descripción           | Permitir la creación y gestión de los productos que hacen parte de un pedido, teniendo en cuenta las reglas de negocio definidas para el restaurante. |
| Requisito relacionado | RF-02                                                                                                                                                 |
| Épica padre           | `EPIC-01` (DOSW3-1)                                                                                                                                   |
| Concepto              | Comida rápida                                                                                                                                         |
| Etiqueta              | `comida-rapida`                                                                                                                                       |
| Fecha de inicio       | 03/09/2026                                                                                                                                            |
| Fecha límite          | 11/09/2026                                                                                                                                            |
| Jira Issue Key        | **DOSW3-2**                                                                                                                                           |
| Evidencia             | Pendiente de captura                                                                                                                                  |

---

## FEAT-02 — Confirmación y preparación del pedido

| Campo                   | Valor                                                                                                                               |
| ----------------------- | ----------------------------------------------------------------------------------------------------------------------------------- |
| ID interno              | `FEAT-02`                                                                                                                           |
| Tipo                    | Feature                                                                                                                             |
| Título                  | Confirmación y preparación del pedido                                                                                               |
| Descripción             | Permitir confirmar los pedidos, enviarlos al proceso de preparación y gestionar los cambios de estado durante su ciclo de atención. |
| Requisitos relacionados | RF-03, RF-04                                                                                                                        |
| Épica padre             | `EPIC-01` (DOSW3-1)                                                                                                                 |
| Concepto                | Comida rápida                                                                                                                       |
| Etiqueta                | `comida-rapida`                                                                                                                     |
| Fecha de inicio         | 08/09/2026                                                                                                                          |
| Fecha límite            | 18/09/2026                                                                                                                          |
| Jira Issue Key          | **DOSW3-3**                                                                                                                         |
| Evidencia               | Pendiente de captura                                                                                                                |

---

# 3. Historias de Usuario

## HU-01 — Armar y modificar el pedido

| Campo             | Valor                          |
| ----------------- | ------------------------------- |
| ID interno        | `HU-01`                        |
| Tipo              | Story                          |
| Título            | Armar y modificar el pedido    |
| Rol               | Cliente                        |
| Requisito         | RF-02                          |
| Reglas de negocio | RN-01, RN-02, RN-03            |
| Prioridad         | Alta                           |
| Responsable       | Sin asignar                    |
| Story Points      | **3**                          |
| Feature padre     | `FEAT-01` (DOSW3-2)            |
| Etiqueta          | `pedido`                       |
| Fecha de inicio   | 03/09/2026                     |
| Fecha límite      | 08/09/2026                     |
| Jira Issue Key    | **DOSW3-10**                   |
| Evidencia         | Pendiente de captura           |

### Descripción para Jira

**Historia de Usuario**

 Como cliente, quiero armar y modificar mi pedido, para seleccionar los productos que deseo consumir y ajustar mi pedido antes de confirmarlo.

**Criterios de aceptación**

**Criterio 1**

* **Dado:** que el cliente está armando un pedido.
* **Cuando:** selecciona productos disponibles.
* **Entonces:** los productos seleccionados deben agregarse correctamente al pedido.

**Criterio 2**

* **Dado:** que el cliente tiene productos en su pedido.
* **Cuando:** modifica las cantidades o elimina productos.
* **Entonces:** el pedido debe actualizarse reflejando los cambios realizados.

---

## HU-02 — Gestionar el pedido de una mesa

| Campo             | Valor                            |
| ----------------- | --------------------------------- |
| ID interno        | `HU-02`                          |
| Tipo              | Story                            |
| Título            | Gestionar el pedido de una mesa  |
| Rol               | Mesero                           |
| Requisito         | RF-02                            |
| Reglas de negocio | RN-01, RN-02, RN-03              |
| Prioridad         | Alta                             |
| Responsable       | Sin asignar                      |
| Story Points      | **5**                             |
| Feature padre     | `FEAT-01` (DOSW3-2)              |
| Etiqueta          | `pedido`                         |
| Fecha de inicio   | 05/09/2026                       |
| Fecha límite      | 11/09/2026                       |
| Jira Issue Key    | **DOSW3-11**                     |
| Evidencia         | Pendiente de captura             |

### Descripción para Jira

**Historia de Usuario**

 Como mesero, quiero gestionar el pedido de una mesa, para registrar correctamente los productos solicitados por los clientes.

**Criterios de aceptación**

**Criterio 1**

* **Dado:** que el mesero está atendiendo una mesa.
* **Cuando:** registra los productos solicitados.
* **Entonces:** los productos deben asociarse correctamente al pedido de la mesa.

**Criterio 2**

* **Dado:** que existe un pedido asociado a una mesa.
* **Cuando:** el mesero modifica los productos solicitados.
* **Entonces:** el pedido debe actualizarse correctamente.

**Criterio 3**

* **Dado:** que el mesero consulta el pedido de una mesa.
* **Cuando:** revisa los productos registrados.
* **Entonces:** debe visualizar la información correspondiente al pedido.

---

## HU-03 — Confirmar pedido y enviarlo a cocina

| Campo             | Valor                                 |
| ----------------- | --------------------------------------- |
| ID interno        | `HU-03`                                |
| Tipo              | Story                                  |
| Título            | Confirmar pedido y enviarlo a cocina   |
| Rol               | Mesero                                 |
| Requisito         | RF-03                                  |
| Reglas de negocio | RN-04, RN-05                           |
| Prioridad         | Alta                                   |
| Responsable       | Sin asignar                            |
| Story Points      | **2**                                  |
| Feature padre     | `FEAT-02` (DOSW3-3)                    |
| Etiqueta          | `pedido`                               |
| Fecha de inicio   | 08/09/2026                             |
| Fecha límite      | 15/09/2026                             |
| Jira Issue Key    | **DOSW3-12**                           |
| Evidencia         | Pendiente de captura                   |

### Descripción para Jira

**Historia de Usuario**

 Como mesero, quiero confirmar el pedido y enviarlo a cocina, para que pueda iniciar correctamente su preparación.

**Criterios de aceptación**

**Criterio 1**

* **Dado:** que el pedido está completo.
* **Cuando:** el mesero lo confirma.
* **Entonces:** el pedido debe quedar registrado como confirmado.

**Criterio 2**

* **Dado:** que el pedido ha sido confirmado.
* **Cuando:** se envía a cocina.
* **Entonces:** el pedido debe quedar disponible para iniciar su preparación.

---

## HU-04 — Cambiar el estado del pedido

| Campo             | Valor                          |
| ----------------- | -------------------------------- |
| ID interno        | `HU-04`                         |
| Tipo              | Story                           |
| Título            | Cambiar el estado del pedido    |
| Rol               | Personal de cocina              |
| Requisito         | RF-04                           |
| Reglas de negocio | RN-06, RN-07                    |
| Prioridad         | Media                           |
| Responsable       | Sin asignar                     |
| Story Points      | **3**                            |
| Feature padre     | `FEAT-02` (DOSW3-3)             |
| Etiqueta          | `cocina`                        |
| Fecha de inicio   | 11/09/2026                      |
| Fecha límite      | 18/09/2026                      |
| Jira Issue Key    | **DOSW3-13**                    |
| Evidencia         | Pendiente de captura            |

### Descripción para Jira

**Historia de Usuario**

 Como personal de cocina, quiero cambiar el estado del pedido, para informar el avance de su preparación.

**Criterios de aceptación**

**Criterio 1**

* **Dado:** que existe un pedido enviado a cocina.
* **Cuando:** el personal de cocina actualiza su estado.
* **Entonces:** el nuevo estado debe registrarse correctamente.

**Criterio 2**

* **Dado:** que el pedido tiene un estado determinado.
* **Cuando:** se intenta modificar el pedido de acuerdo con las reglas establecidas.
* **Entonces:** el sistema debe permitir o bloquear la modificación según el estado actual del pedido.

---

# 4. Subtareas

---

## Subtareas de HU-01 — Armar y modificar el pedido (DOSW3-10)

| Campo          | ST-01                                       | ST-02                               | ST-03                                        |
| -------------- | ------------------------------------------- | ------------------------------------ | --------------------------------------------- |
| Subtarea       | Implementar gestión de productos del pedido | Validar disponibilidad de productos | Actualizar cantidades y productos del pedido |
| Historia padre | `HU-01` (DOSW3-10)                          | `HU-01` (DOSW3-10)                  | `HU-01` (DOSW3-10)                            |
| Prioridad      | Alta                                        | Alta                                 | Alta                                          |
| Responsable    | Paula Díaz                                  | Daniel Valero                       | Juan Valderrama                               |
| Jira Issue Key | DOSW3-14                                  | DOSW3-15                           | DOSW3-16                                   |


---

## Subtareas de HU-02 — Gestionar el pedido de una mesa (DOSW3-11)

| Campo          | ST-04                                | ST-05                                      | ST-06                                      |
| -------------- | -------------------------------------- | -------------------------------------------- | --------------------------------------------- |
| Subtarea       | Registrar pedido asociado a una mesa | Consultar productos del pedido de una mesa | Modificar productos del pedido de una mesa |
| Historia padre | `HU-02` (DOSW3-11)                   | `HU-02` (DOSW3-11)                          | `HU-02` (DOSW3-11)                            |
| Prioridad      | Alta                                  | Alta                                         | Alta                                          |
| Responsable    | Daniel Valero                        | Paula Díaz                                  | Juan Valderrama                               |
| Jira Issue Key | DOSW3-17                            | DOSW3-18                                   | DOSW3-19                                   |

---

## Subtareas de HU-03 — Confirmar pedido y enviarlo a cocina (DOSW3-12)

| Campo          | ST-07                          | ST-08                             | ST-09                              |
| -------------- | --------------------------------- | ------------------------------------ | ------------------------------------- |
| Subtarea       | Validar información del pedido | Registrar confirmación del pedido | Enviar pedido al proceso de cocina |
| Historia padre | `HU-03` (DOSW3-12)              | `HU-03` (DOSW3-12)                 | `HU-03` (DOSW3-12)                    |
| Prioridad      | Alta                             | Alta                                 | Alta                                   |
| Responsable    | Paula Díaz                       | Daniel Valero                       | Juan Valderrama                        |
| Jira Issue Key | DOSW3-20                      | DOSW3-21                           | DOSW3-22                              |


---

## Subtareas de HU-04 — Cambiar el estado del pedido (DOSW3-13)

| Campo          | ST-10                        | ST-11                         | ST-12                        |
| -------------- | ------------------------------- | -------------------------------- | -------------------------------- |
| Subtarea       | Registrar estados del pedido | Validar transición de estados | Actualizar estado del pedido |
| Historia padre | `HU-04` (DOSW3-13)            | `HU-04` (DOSW3-13)             | `HU-04` (DOSW3-13)              |
| Prioridad      | Media                          | Media                            | Media                             |
| Responsable    | Pendiente de asignación       | Pendiente de asignación         | Pendiente de asignación          |
| Jira Issue Key | DOSW3-23                     | DOSW3-24                         | DOSW3-25                          |


---

# 5. Priorización del Product Backlog

La prioridad de las historias se establece de acuerdo con su importancia dentro del flujo principal de pedidos.

| Historia                                     | Jira Key   | Prioridad | Justificación                                                          |
| --------------------------------------------- | ---------- | --------- | ------------------------------------------------------------------------ |
| HU-01 — Armar y modificar el pedido          | DOSW3-10   | Alta      | Es necesaria para construir y modificar el pedido.                     |
| HU-02 — Gestionar el pedido de una mesa      | DOSW3-11   | Alta      | Permite registrar y administrar los pedidos realizados en las mesas.   |
| HU-03 — Confirmar pedido y enviarlo a cocina | DOSW3-12   | Alta      | Permite continuar el flujo del pedido hacia el proceso de preparación. |
| HU-04 — Cambiar el estado del pedido         | DOSW3-13   | Media     | Gestiona el avance del pedido después de su envío a cocina.            |


---


# 6. Evidencias de Jira

## 6.1 Creación de la Épica

**Evidencia:** `[Pegar aquí captura de la épica DOSW3-1]`

## 6.2 Features vinculadas a la Épica

**Evidencia:** `[Pegar aquí captura de la jerarquía EPIC → FEATURE, DOSW3-2 y DOSW3-3]`

## 6.3 Historias de Usuario

**Evidencia HU-01 (DOSW3-10):** `[Pegar aquí captura]`
**Evidencia HU-02 (DOSW3-11):** `[Pegar aquí captura]`
**Evidencia HU-03 (DOSW3-12):** `[Pegar aquí captura]`
**Evidencia HU-04 (DOSW3-13):** `[Pegar aquí captura]`

## 6.4 Subtareas

**Evidencia:** `[Pendiente — crear las 12 subtareas primero]`

## 6.5 Product Backlog y prioridades

**Evidencia:** `[Pegar aquí captura del Product Backlog mostrando las historias y sus prioridades]`

---

# 7. Timeline

**Evidencia:** `[Pegar aquí captura de Jira Timeline]`

* Inicio de la épica: **03/09/2026**
* Fin de la épica: **18/09/2026**
* FEAT-01 (DOSW3-2): **03/09/2026 – 11/09/2026**
* FEAT-02 (DOSW3-3): **08/09/2026 – 18/09/2026**

---

# 8. Trazabilidad con Scrum Work Breakdown

| Estructura Scrum | Jira Issue Key |
| ------------------ | ---------------- |
| `EPIC-01`         | **DOSW3-1**     |
| `FEAT-01`         | **DOSW3-2**     |
| `FEAT-02`         | **DOSW3-3**     |
| `HU-01`           | **DOSW3-10**    |
| `HU-02`           | **DOSW3-11**    |
| `HU-03`           | **DOSW3-12**    |
| `HU-04`           | **DOSW3-13**    |
| `ST-01`           | **DOSW3-14**    |
| `ST-02`           | **DOSW3-15**    |
| `ST-03`           | **DOSW3-16**    |
| `ST-04`           | **DOSW3-17**    |
| `ST-05`           | **DOSW3-18**    |
| `ST-06`           | **DOSW3-19**    |
| `ST-07`           | **DOSW3-20**    |
| `ST-08`           | **DOSW3-21**    |
| `ST-09`           | **DOSW3-22**    |
| `ST-10`           | **DOSW3-23**    |
| `ST-11`           | **DOSW3-24**    |
| `ST-12`           | **DOSW3-25**    |

---


# 9. Sprint Backlog (Parte 8 — Planeación del Sprint)

## 10.1 Historias seleccionadas para el Sprint 1

| Historia | Jira Key | Prioridad | Story Points |
| -------- | -------- | --------- | ------------- |
| HU-01 — Armar y modificar el pedido | DOSW3-10 | Alta | 3 |
| HU-02 — Gestionar el pedido de una mesa | DOSW3-11 | Alta | 5 |
| HU-03 — Confirmar pedido y enviarlo a cocina | DOSW3-12 | Alta | 2 |

**Total Sprint 1: 10 puntos.** HU-04 (Media, 3 puntos) queda para el Sprint 2.

## 10.2 Responsables por subtarea en el Sprint 1

| Subtarea | Historia | Responsable |
| -------- | -------- | ------------ |
| ST-01 — Implementar gestión de productos del pedido | HU-01 | Paula Díaz |
| ST-02 — Validar disponibilidad de productos | HU-01 | Daniel Valero |
| ST-03 — Actualizar cantidades y productos del pedido | HU-01 | Juan Valderrama |
| ST-04 — Registrar pedido asociado a una mesa | HU-02 | Daniel Valero |
| ST-05 — Consultar productos del pedido de una mesa | HU-02 | Paula Díaz |
| ST-06 — Modificar productos del pedido de una mesa | HU-02 | Juan Valderrama |
| ST-07 — Validar información del pedido | HU-03 | Paula Díaz |
| ST-08 — Registrar confirmación del pedido | HU-03 | Daniel Valero |
| ST-09 — Enviar pedido al proceso de cocina | HU-03 | Juan Valderrama |

## 10.3 Justificación de la planeación

Se seleccionaron las tres historias de **prioridad Alta** (HU-01, HU-02, HU-03) para el Sprint 1, dejando HU-04 (prioridad Media) para el Sprint 2. Dentro de las historias Alta, el criterio de "menor estimación primero" se aplicó considerando la **dependencia funcional** entre ellas: HU-03 (2 puntos, la más pequeña) no puede entregar valor de forma aislada porque depende de que el pedido ya pueda armarse (HU-01) y asociarse a una mesa (HU-02). Por eso las tres entran juntas al Sprint 1: así, al finalizar el sprint, el equipo tiene el flujo completo cliente → mesero → cocina funcionando de extremo a extremo, generando la entrega de valor más temprana y demostrable posible. HU-04 (cambio de estado desde cocina) se deja para el Sprint 2 porque depende de que un pedido ya haya llegado a cocina (RF-04 depende de RF-03), y por ser de prioridad Media no compromete el valor mínimo demostrable del primer sprint.

**Evidencia:** `[Pegar aquí captura del Sprint Backlog en Jira con las 3 historias, sus 9 subtareas y responsables asignados]`

---

