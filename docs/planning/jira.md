# Jira — El Restaurante (Comida Rápida)

---

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
| Evidencia               | ![alt text](image.png)                                                                                                                                                                                                                                                                                  |

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
| Evidencia             | ![alt text](image-1.png)                                                                                                                                  |

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
| Evidencia               | ![alt text](image-2.png)                                                                                                                |

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
| Story Points      | Pendiente de Parte 7           |
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
![alt text](image-3.png)
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
| Story Points      | Pendiente de Parte 7             |
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
![alt text](image-4.png)
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
| Story Points      | Pendiente de Parte 7                   |
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
![alt text](image-5.png)
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
| Story Points      | Pendiente de Parte 7            |
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
![alt text](image-6.png)
---

# 4. Subtareas


---

## Subtareas de HU-01 — Armar y modificar el pedido (DOSW3-10)

| Campo          | ST-01                                       | ST-02                               | ST-03                                        |
| -------------- | ------------------------------------------- | ------------------------------------ | --------------------------------------------- |
| Subtarea       | Implementar gestión de productos del pedido | Validar disponibilidad de productos | Actualizar cantidades y productos del pedido |
| Historia padre | `HU-01` (DOSW3-10)                          | `HU-01` (DOSW3-10)                  | `HU-01` (DOSW3-10)                            |
| Prioridad      | Alta                                        | Alta                                 | Alta                                          |
| Responsable    | Pendiente de asignación                     | Pendiente de asignación             | Pendiente de asignación                       |
                            
![alt text](image-7.png)
---

## Subtareas de HU-02 — Gestionar el pedido de una mesa (DOSW3-11)

| Campo          | ST-04                                | ST-05                                      | ST-06                                      |
| -------------- | -------------------------------------- | -------------------------------------------- | --------------------------------------------- |
| Subtarea       | Registrar pedido asociado a una mesa | Consultar productos del pedido de una mesa | Modificar productos del pedido de una mesa |
| Historia padre | `HU-02` (DOSW3-11)                   | `HU-02` (DOSW3-11)                          | `HU-02` (DOSW3-11)                            |
| Prioridad      | Alta                                  | Alta                                         | Alta                                          |
| Responsable    | Pendiente de asignación              | Pendiente de asignación                     | Pendiente de asignación                       |

![alt text](image-8.png)
---

## Subtareas de HU-03 — Confirmar pedido y enviarlo a cocina (DOSW3-12)

| Campo          | ST-07                          | ST-08                             | ST-09                              |
| -------------- | --------------------------------- | ------------------------------------ | ------------------------------------- |
| Subtarea       | Validar información del pedido | Registrar confirmación del pedido | Enviar pedido al proceso de cocina |
| Historia padre | `HU-03` (DOSW3-12)              | `HU-03` (DOSW3-12)                 | `HU-03` (DOSW3-12)                    |
| Prioridad      | Alta                             | Alta                                 | Alta                                   |
| Responsable    | Pendiente de asignación         | Pendiente de asignación             | Pendiente de asignación               |

![alt text](image-9.png)
---

## Subtareas de HU-04 — Cambiar el estado del pedido (DOSW3-13)

| Campo          | ST-10                        | ST-11                         | ST-12                        |
| -------------- | ------------------------------- | -------------------------------- | -------------------------------- |
| Subtarea       | Registrar estados del pedido | Validar transición de estados | Actualizar estado del pedido |
| Historia padre | `HU-04` (DOSW3-13)            | `HU-04` (DOSW3-13)             | `HU-04` (DOSW3-13)              |
| Prioridad      | Media                          | Media                            | Media                             |
| Responsable    | Pendiente de asignación       | Pendiente de asignación         | Pendiente de asignación          |

![alt text](image-10.png)
---

# 5. Priorización del Product Backlog

La prioridad de las historias se establece de acuerdo con su importancia dentro del flujo principal de pedidos.

| Historia                                     | Jira Key   | Prioridad | Justificación                                                          |
| --------------------------------------------- | ---------- | --------- | ------------------------------------------------------------------------ |
| HU-01 — Armar y modificar el pedido          | DOSW3-10   | Alta      | Es necesaria para construir y modificar el pedido.                     |
| HU-02 — Gestionar el pedido de una mesa      | DOSW3-11   | Alta      | Permite registrar y administrar los pedidos realizados en las mesas.   |
| HU-03 — Confirmar pedido y enviarlo a cocina | DOSW3-12   | Alta      | Permite continuar el flujo del pedido hacia el proceso de preparación. |
| HU-04 — Cambiar el estado del pedido         | DOSW3-13   | Media     | Gestiona el avance del pedido después de su envío a cocina.            |

6. Evidencias de Jira
6.1 Creación de la Épica

Evidencia: 
![alt text](image-11.png)

6.2 Features vinculadas a la Épica

Evidencia: ![alt text](image-12.png)

6.3 Historias de Usuario

Evidencia HU-01 (DOSW3-10): ![alt text](image-13.png) Evidencia HU-02 (DOSW3-11): ![alt text](image-14.png) Evidencia HU-03 (DOSW3-12): ![alt text](image-15.png) Evidencia HU-04 (DOSW3-13): ![alt text](image-16.png)

6.4 Subtareas

Evidencia: 
![alt text](image-18.png)
![alt text](image-19.png)
![alt text](image-20.png)
![alt text](image-21.png)
6.5 Product Backlog y prioridades

Evidencia: 
![alt text](image-22.png)
---

