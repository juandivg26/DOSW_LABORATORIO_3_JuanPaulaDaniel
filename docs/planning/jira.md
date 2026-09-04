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
| Evidencia               | <img width="1556" height="566" alt="imagen" src="https://github.com/user-attachments/assets/065b2301-7d92-494f-af7e-dd3d91f2869a" />
                                                                                                                                                                                                                                                                              |

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
| Evidencia             | <img width="1509" height="769" alt="imagen" src="https://github.com/user-attachments/assets/42f71f37-49a0-4a68-828a-94135b56ebd5" />
                                                                                                                                |

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
| Evidencia               | P<img width="1513" height="833" alt="imagen" src="https://github.com/user-attachments/assets/f2edaa90-3705-4c8d-97e2-b2cd357c6f99" />
                                                                                                            |

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
| Evidencia         | <img width="1511" height="820" alt="imagen" src="https://github.com/user-attachments/assets/d34e27db-427c-46a3-815d-422ab8a8072b" />
          |

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
| Evidencia         | <img width="1505" height="831" alt="imagen" src="https://github.com/user-attachments/assets/a45f4e05-ed87-4b36-99c7-e22bd2ad1802" />
             |

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
| Evidencia         | <img width="1505" height="756" alt="imagen" src="https://github.com/user-attachments/assets/1b962280-f5fc-48a9-a640-be7d1ebcf726" />
                   |

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
| Evidencia         | <img width="1833" height="817" alt="imagen" src="https://github.com/user-attachments/assets/04fe1ba1-e3de-40e4-b831-5404723d6e7e" />
           |

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

**Evidencia:** <img width="1519" height="444" alt="imagen" src="https://github.com/user-attachments/assets/adda5e98-60bc-41c8-93e7-2351e0604e59" />


## 6.2 Features vinculadas a la Épica

**Evidencia:** <img width="896" height="387" alt="imagen" src="https://github.com/user-attachments/assets/a7f5a67b-fb5e-4da3-91d2-fe9481efe912" />


## 6.3 Historias de Usuario

**Evidencia HU-01 (DOSW3-10):** <img width="1511" height="820" alt="imagen" src="https://github.com/user-attachments/assets/9f77d19a-880c-43ff-aa88-c9994fd1266a" />

**Evidencia HU-02 (DOSW3-11):** <img width="1505" height="831" alt="imagen" src="https://github.com/user-attachments/assets/9c89bd1c-0bf0-4310-9174-54ef23d67a24" />

**Evidencia HU-03 (DOSW3-12):** <img width="1505" height="756" alt="imagen" src="https://github.com/user-attachments/assets/09390e72-b442-4d57-95ce-2f1688dcbe23" />

**Evidencia HU-04 (DOSW3-13):** <img width="1512" height="808" alt="imagen" src="https://github.com/user-attachments/assets/df64e927-51a5-412b-8858-aad046b42364" />


## 6.4 Subtareas

**Evidencia:** <img width="1192" height="543" alt="imagen" src="https://github.com/user-attachments/assets/417fd191-d9ce-40d0-b5eb-f0ebbb520f58" />


## 6.5 Product Backlog y prioridades

**Evidencia:** <img width="1616" height="245" alt="imagen" src="https://github.com/user-attachments/assets/47549c42-107d-421b-8a39-b0a253e7bae5" />


---

# 7. Timeline

**Evidencia:** <img width="1360" height="773" alt="imagen" src="https://github.com/user-attachments/assets/9c29b0bf-ff8a-425f-ae8b-4ed2eb659b15" />


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
| HU-01 — Armar y modificar el pedido | DOSW3-10 | Alta | 5 |
| HU-02 — Gestionar el pedido de una mesa | DOSW3-11 | Alta | 3 |
| HU-03 — Confirmar pedido y enviarlo a cocina | DOSW3-12 | Alta | 2 |

<img width="1534" height="252" alt="imagen" src="https://github.com/user-attachments/assets/0e983716-1b9e-4c73-a474-da0b6082f808" />


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


---

