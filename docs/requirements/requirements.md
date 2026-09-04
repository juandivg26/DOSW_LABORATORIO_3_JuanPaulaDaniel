
# Requirements — Restaurante Comida Rápida

## Requerimientos Funcionales

| Código | Nombre | Descripción | Cómo se ejecutará | Actor Principal | Precondiciones |
|---|---|---|---|---|---|
| RF-01 | Consultar carta digital con disponibilidad | El sistema debe permitir consultar los productos disponibles del restaurante mostrando nombre, descripción, precio e ingredientes disponibles. | El cliente ingresa al sistema, consulta la carta y visualiza los productos habilitados para ordenar. | Cliente | La carta debe estar registrada por el administrador y los productos deben tener disponibilidad actualizada. |
| RF-02 | Crear y modificar pedido | El sistema debe permitir agregar, eliminar y modificar productos dentro de un pedido mientras la cuenta permanezca abierta. | El cliente o mesero selecciona productos de la carta y los agrega al pedido activo de la mesa. | Cliente / Mesero | La mesa debe tener una cuenta abierta y los productos deben estar disponibles. |
| RF-03 | Confirmar pedido y enviarlo a cocina | El sistema debe permitir confirmar un pedido y enviarlo automáticamente al tablero de cocina para su preparación. | El cliente o mesero confirma la orden y el sistema cambia el estado del pedido a RECIBIDO. | Cliente / Mesero | El pedido debe contener al menos un producto válido y la mesa debe estar activa. |
| RF-04 | Gestionar estado del pedido en cocina | El sistema debe permitir que cocina actualice el estado del pedido durante su preparación. | El personal de cocina cambia el estado del pedido entre RECIBIDO, EN PREPARACIÓN, LISTO y ENTREGADO. | Cocina | Debe existir un pedido confirmado enviado desde el sistema. |
| RF-05 | Administrar productos de la carta | El sistema debe permitir crear, editar y desactivar productos disponibles en la carta digital. | El administrador ingresa al módulo de administración y modifica la información de los productos. | Administrador | El usuario debe tener permisos administrativos. |
| RF-06 | Controlar disponibilidad de ingredientes | El sistema debe bloquear automáticamente productos cuyos ingredientes estén agotados. | Cuando un ingrediente llega a disponibilidad cero, el sistema cambia el producto a no disponible. | Administrador / Cocina | Los ingredientes deben estar registrados dentro del inventario. |
| RF-07 | Registrar pago y cerrar cuenta | El sistema debe permitir registrar el pago de una mesa y cerrar la cuenta cuando finalice la compra. | El mesero registra el método de pago y el sistema almacena la transacción realizada. | Mesero / Administrador | La cuenta debe estar abierta y tener productos asociados. |

---

# Requerimientos No Funcionales

| Código | Nombre | Descripción |
|---|---|---|
| RNF-01 | Seguridad y control de acceso | El sistema debe controlar los permisos según el rol del usuario (cliente, mesero, cocina y administrador). |
| RNF-02 | Rendimiento | El tablero de cocina debe reflejar un nuevo pedido en menos de 2 segundos después de su confirmación. |
| RNF-03 | Disponibilidad | El sistema debe permanecer operativo durante todo el horario de servicio del restaurante sin interrupciones críticas. |
| RNF-04 | Usabilidad | Un cliente nuevo debe poder realizar su primer pedido utilizando una interfaz sencilla e intuitiva. |
| RNF-05 | Auditabilidad | Cada cambio de estado de un pedido debe almacenar usuario responsable, fecha y hora del cambio. |
| RNF-06 | Compatibilidad | La plataforma debe funcionar correctamente en navegadores modernos y dispositivos móviles. |

---

# Requerimientos Seleccionados

Los requerimientos seleccionados para realizar los diagramas UML y análisis detallado son:

- RF-02: Crear y modificar pedido.
- RF-03: Confirmar pedido y enviarlo a cocina.
- RF-04: Gestionar estado del pedido en cocina.

---

# RF-02 — Crear y modificar pedido

## Descripción

El sistema debe permitir que el cliente o mesero pueda agregar, eliminar y modificar productos dentro de un pedido activo antes de enviarlo a cocina.

## Actores involucrados

| Actor | Participación |
|---|---|
| Cliente | Selecciona productos y modifica su pedido. |
| Mesero | Gestiona pedidos realizados desde una mesa. |
| Sistema | Calcula valores y valida disponibilidad. |

## Precondiciones

- La mesa debe tener una cuenta abierta.
- Los productos deben estar disponibles.
- El usuario debe estar autenticado.

## Datos de entrada

| Nombre | Descripción | Tipo |
|---|---|---|
| Producto | Producto seleccionado de la carta | Objeto |
| Cantidad | Número de unidades solicitadas | Entero |
| Observaciones | Indicaciones adicionales del cliente | Texto |

## Datos de salida

| Nombre | Descripción | Tipo |
|---|---|---|
| Pedido actualizado | Información del pedido con sus productos | Objeto |
| Total pedido | Valor actualizado de la cuenta | Decimal |

## Flujo principal

| Paso | Actor | Descripción |
|---|---|---|
| 1 | Cliente/Mesero | Ingresa al módulo de pedidos. |
| 2 | Sistema | Muestra la carta disponible. |
| 3 | Cliente/Mesero | Selecciona productos y cantidades. |
| 4 | Sistema | Valida disponibilidad y actualiza el pedido. |
| 5 | Sistema | Calcula el nuevo valor total. |

## Flujo alternativo

| Paso | Actor | Descripción |
|---|---|---|
| 1 | Sistema | Detecta que un producto no tiene disponibilidad. |
| 2 | Sistema | Bloquea la selección del producto. |
| 3 | Usuario | Selecciona otro producto disponible. |

## Reglas de negocio

| Código | Descripción |
|---|---|
| RN-01 | Un pedido solo puede modificarse mientras esté en estado RECIBIDO. |
| RN-02 | El precio del producto queda congelado cuando se agrega al pedido. |
| RN-03 | Un combo siempre incluye bebida y su precio no cambia si se elimina la bebida. |

---

# RF-03 — Confirmar pedido y enviarlo a cocina

## Descripción

El sistema debe permitir confirmar un pedido completo y enviarlo automáticamente al tablero de cocina.

## Actores involucrados

| Actor | Participación |
|---|---|
| Cliente/Mesero | Confirma la orden. |
| Cocina | Recibe la orden para preparación. |
| Sistema | Cambia el estado del pedido. |

## Precondiciones

- El pedido debe contener productos.
- Los productos deben estar disponibles.

## Datos de entrada

| Nombre | Descripción | Tipo |
|---|---|---|
| ID Pedido | Identificador del pedido | Número |
| Confirmación | Acción de envío a cocina | Booleano |

## Datos de salida

| Nombre | Descripción | Tipo |
|---|---|---|
| Estado pedido | Nuevo estado RECIBIDO | Texto |
| Orden cocina | Información enviada al tablero | Objeto |

## Flujo principal

| Paso | Actor | Descripción |
|---|---|---|
| 1 | Usuario | Selecciona confirmar pedido. |
| 2 | Sistema | Valida los productos. |
| 3 | Sistema | Cambia estado a RECIBIDO. |
| 4 | Sistema | Envía pedido a cocina. |

## Flujo alternativo

| Paso | Actor | Descripción |
|---|---|---|
| 1 | Sistema | Encuentra un producto agotado. |
| 2 | Sistema | Solicita modificar el pedido antes de confirmar. |

## Reglas de negocio

| Código | Descripción |
|---|---|
| RN-04 | Un pedido enviado a preparación no puede modificarse. |
| RN-05 | Todo pedido confirmado debe aparecer en el tablero de cocina. |

---

# RF-04 — Gestionar estado del pedido en cocina

## Descripción

El sistema debe permitir actualizar el estado de preparación de cada pedido.

## Actores involucrados

| Actor | Participación |
|---|---|
| Cocina | Actualiza el estado del pedido. |
| Sistema | Registra los cambios realizados. |

## Precondiciones

- El pedido debe estar confirmado.
- Cocina debe tener permisos de acceso.

## Datos de entrada

| Nombre | Descripción | Tipo |
|---|---|---|
| Estado nuevo | Estado seleccionado del pedido | Enum |

## Datos de salida

| Nombre | Descripción | Tipo |
|---|---|---|
| Estado actualizado | Nuevo estado del pedido | Texto |
| Registro histórico | Fecha y usuario del cambio | Objeto |

## Flujo principal

| Paso | Actor | Descripción |
|---|---|---|
| 1 | Cocina | Visualiza pedidos pendientes. |
| 2 | Cocina | Selecciona un pedido. |
| 3 | Cocina | Cambia su estado. |
| 4 | Sistema | Guarda el cambio realizado. |

## Flujo alternativo

| Paso | Actor | Descripción |
|---|---|---|
| 1 | Sistema | Detecta intento de cambio inválido. |
| 2 | Sistema | Rechaza la operación. |

## Reglas de negocio

| Código | Descripción |
|---|---|
| RN-06 | Los estados deben seguir el flujo RECIBIDO → EN PREPARACIÓN → LISTO → ENTREGADO. |
| RN-07 | Cada cambio debe quedar registrado con fecha y usuario. |

# Análisis crítico de requerimientos

## 1. Requerimientos que necesitan más detalle

Los requerimientos que necesitan mayor especificación son:

### RF-02 — Crear y modificar pedido

Este requerimiento necesita más detalle sobre las reglas para modificar un pedido. Se debe definir hasta qué momento un cliente o mesero puede agregar, eliminar o cambiar productos, por ejemplo, si estas modificaciones son permitidas únicamente antes de que cocina inicie la preparación.

También es necesario especificar cómo se manejarán productos con diferentes tamaños, complementos o modificaciones especiales.

### RF-03 — Confirmar pedido y enviarlo a cocina

Este requerimiento requiere aclarar el proceso de confirmación del pedido, especialmente qué sucede cuando un producto deja de estar disponible justo antes de enviarlo a cocina.

También se debe definir cómo se notifica al cliente o mesero cuando la orden fue recibida correctamente por cocina.

### RF-04 — Gestionar estado del pedido en cocina

Se requiere mayor detalle sobre los estados permitidos del pedido y las transiciones válidas entre ellos.

Por ejemplo:

RECIBIDO → EN PREPARACIÓN → LISTO → ENTREGADO

Además, se debe definir quién tiene permisos para realizar cada cambio de estado.

---

# 2. Contradicciones o ambigüedades encontradas

Durante el análisis se identificaron algunas posibles ambigüedades:

- No está definido si el cliente puede modificar directamente su pedido o si siempre debe hacerlo mediante un mesero.
- No está especificado qué ocurre cuando un producto solicitado se agota mientras el pedido está en proceso.
- No está definido si el sistema manejará pagos antes o después de la preparación del pedido.
- No está definido si varios pedidos pueden asociarse a una misma mesa o cliente.

Estas situaciones deben aclararse antes del desarrollo para evitar interpretaciones diferentes del sistema.

---

# 3. Requerimientos priorizados para la primera iteración

Para la primera iteración del desarrollo se priorizarían los siguientes requerimientos:

| Prioridad | Requerimiento | Justificación |
|---|---|---|
| Alta | RF-01 Consultar carta digital | Es la base para que los clientes conozcan los productos disponibles. |
| Alta | RF-02 Crear y modificar pedido | Representa la funcionalidad principal del sistema y permite generar órdenes. |
| Alta | RF-03 Confirmar pedido y enviarlo a cocina | Permite conectar la solicitud del cliente con el proceso operativo del restaurante. |
| Media | RF-04 Gestionar estado del pedido | Es necesario para controlar la preparación, pero depende de que existan pedidos creados. |
| Media | RF-07 Registrar pago y cerrar cuenta | Puede implementarse después del flujo principal de pedidos. |

---

# 4. Funcionalidades fuera del MVP

Para la primera versión del producto se dejarían fuera algunas funcionalidades que no son esenciales:

## Sistema de fidelización de clientes

Aunque puede aportar valor al negocio, no es necesario para validar el funcionamiento principal del restaurante.

## Promociones y descuentos personalizados

Requiere reglas adicionales y análisis de clientes, por lo que puede desarrollarse en versiones posteriores.

## Integración con plataformas externas de domicilios

Aunque puede ser útil, aumenta la complejidad inicial del sistema.

## Reportes avanzados de ventas e inventario

Los reportes pueden agregarse posteriormente cuando exista suficiente información histórica.

El MVP se enfocará en el flujo principal:

Consultar productos → Crear pedido → Confirmar pedido → Preparación en cocina → Entrega.
