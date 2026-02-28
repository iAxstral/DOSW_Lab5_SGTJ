# 📄 Planeación del Sistema

## Desglose de trabajo: Épicas, Historias de Usuario y Tareas

La implementación de los requerimientos identificados de Bankify se desglosa de la siguiente manera:

### 1. Épica:

| Campo | Descripción |
|------|-------------|
| **ID** | KAN-01 |
| **Título** |Gestión de Accesos y Transacciones Bancarias |
| **Descripción** | Establecer la infraestructura principal del sistema Bankify para permitir el registro controlado de nuevas cuentas, el acceso seguro de los usuarios y la ejecución de las operaciones financieras fundamentales (consulta de saldos y recepción de depósitos). |
| **Stakeholder** | Cliente de Bankify|

### 2. Historias de usuario:

| Campo | Descripción |
|------|-------------|
| **ID** | KAN-03 |
| **Título** | Autenticación de Usuarios en la Plataforma |
| **Descripción** | Como cliente o asesor, quiero poder autenticarme utilizando mi usuario y contraseña para acceder de forma segura a mis operaciones permitidas dentro del sistema.|
| **Prioridad** | Alta. Es la puerta de entrada y el candado del sistema. Sin ella, no hay seguridad ni separación de roles (no podríamos saber si quien entra es un Asesor o un Cliente).|
| **Estimación** | Pendiente de Planning Poker |

| Campo | Descripción |
|------|-------------|
| **ID** | KAN-04 |
| **Título** | Registrar Nueva Cuenta Bancaria |
| **Descripción** | Como Asesor, quiero registrar una nueva cuenta bancaria asociándola a un cliente existente, para que este pueda comenzar a utilizar los servicios financieros.|
| **Prioridad** | Alta. No se puede depositar dinero ni consultar saldos si no existen cuentas creadas previamente. |
| **Estimación** | Pendiente de Planning Poker |

| Campo | Descripción |
|------|-------------|
| **ID** | KAN-05 |
| **Título** | Realizar Depósito a Cuenta |
| **Descripción** | Como Cliente o Usuario Externo, quiero realizar un depósito ingresando dinero a una cuenta de forma controlada, para incrementar el saldo disponible.|
| **Prioridad** | Alta. Es la transacción principal que permite el ingreso de dinero. Es lo que le da valor al modelo de negocio del banco. |
| **Estimación** | Pendiente de Planning Poker |

| Campo | Descripción |
|------|-------------|
| **ID** | KAN-06 |
| **Título** | Consultar Saldo de Cuenta |
| **Descripción** | Como Cliente autenticado, quiero consultar el saldo actual de mi cuenta para conocer exactamente mi disponibilidad de dinero en cualquier momento.|
| **Prioridad** | Alta. Aunque es vital para la experiencia del usuario, es una operación de "lectura" que depende totalmente de que las tres anteriores ya existan y funcionen. |
| **Estimación** | Pendiente de Planning Poker |

### 3. Tareas:

**Tareas para Historia de Usuario 1**

| Campo | Descripción |
|------|-------------|
| **ID** | KAN-07 |
| **Título** | Desarrollar Interfaz de Login |
| **ID de la Historia de Uso asociada** | KAN-01 |
| **Descripción** | Como desarrollador frontend, quiero construir la interfaz visual de login basada en los mockups de Figma para que el usuario pueda ingresar sus credenciales. |
| **Tareas requisito** | Ninguna |

| Campo | Descripción |
|------|-------------|
| **ID** | KAN-08 |
| **Título** | Crear Endpoint de Autenticación |
| **ID de la Historia de Uso asociada** | KAN-01 |
| **Descripción** | Como desarrollador backend, quiero construir el endpoint de inicio de sesión en Java para recibir y procesar las peticiones del frontend. |
| **Tareas requisito** | Ninguna |

| Campo | Descripción |
|------|-------------|
| **ID** | KAN-09 |
| **Título** | Validar Credenciales en Base de Datos |
| **ID de la Historia de Uso asociada** | KAN-01 |
| **Descripción** | Como desarrollador backend, quiero implementar la lógica de validación contra la base de datos para garantizar que solo usuarios registrados ingresen. |
| **Tareas requisito** | TR-02|

**Tareas para Historias de Usuario 2**

| Campo | Descripción |
|------|-------------|
| **ID** | KAN-10 |
| **Título** | Codificar Reglas de Validación de Cuenta |
| **ID de la Historia de Uso asociada** | KAN-02 |
| **Descripción** | Como desarrollador backend, quiero programar la validación en Java que exige 10 dígitos y un prefijo válido para evitar cuentas erróneas. |
| **Tareas requisito** | Ninguna |

| Campo | Descripción |
|------|-------------|
| **ID** | KAN-11 |
| **Título** | Crear Endpoint de Registro de Cuenta |
| **ID de la Historia de Uso asociada** | KAN-02 |
| **Descripción** | Como desarrollador backend, quiero crear el endpoint POST para guardar los datos de la nueva cuenta bancaria en la base de datos. |
| **Tareas requisito** | TR-04 |

| Campo | Descripción |
|------|-------------|
| **ID** | KAN-12 |
| **Título** | Desarrollar Formulario de Creación de Cuenta |
| **ID de la Historia de Uso asociada** | KAN-02 |
| **Descripción** | Como desarrollador frontend, quiero maquetar el formulario donde el asesor ingresará el número de cuenta y seleccionará al cliente. |
| **Tareas requisito** | Ninguna |

**Tareas para Historia de Usuario 3**

| Campo | Descripción |
|------|-------------|
| **ID** | KAN-13 |
| **Título** | Crear Endpoint de Recepción de Depósitos |
| **ID de la Historia de Uso asociada** | KAN-03 |
| **Descripción** | Como desarrollador backend, quiero construir el endpoint que reciba el número de cuenta destino y el monto a depositar para iniciar la transacción. |
| **Tareas requisito** | Ninguna |

| Campo | Descripción |
|------|-------------|
| **ID** | KAN-14 |
| **Título** | Actualizar Saldo en Base de Datos |
| **ID de la Historia de Uso asociada** | KAN-03 |
| **Descripción** | Como desarrollador backend, quiero implementar la lógica que sume el depósito al saldo actual de la cuenta, validando previamente que la cuenta exista. |
| **Tareas requisito** | TR-07 |

| Campo | Descripción |
|------|-------------|
| **ID** | KAN-15 |
| **Título** | Desarrollar Vista de Depósitos |
| **ID de la Historia de Uso asociada** | KAN-03 |
| **Descripción** | Como desarrollador frontend, quiero crear la vista simulada de la pasarela para que el usuario ingrese el monto y confirme su transacción visualmente. |
| **Tareas requisito** | Ninguna |

**Tareas para la Historia de Usuario 4**

| Campo | Descripción |
|------|-------------|
| **ID** | KAN-16 |
| **Título** | Crear Endpoint de Consulta de Saldo |
| **ID de la Historia de Uso asociada** | KAN-04 |
| **Descripción** | Como desarrollador backend, quiero desarrollar un endpoint GET en Java que recupere el saldo actualizado de un cliente específico. |
| **Tareas requisito** | Ninguna |

| Campo | Descripción |
|------|-------------|
| **ID** | KAN-17 |
| **Título** | Proteger Endpoint de Consulta |
| **ID de la Historia de Uso asociada** | KAN-04 |
| **Descripción** | Como desarrollador backend, quiero añadir validación de seguridad para asegurar que solo el cliente dueño de la cuenta autenticado pueda consultar su saldo. |
| **Tareas requisito** | TR-10 |

| Campo | Descripción |
|------|-------------|
| **ID** | KAN-18 |
| **Título** | Diseñar Dashboard de Saldo del Cliente |
| **ID de la Historia de Uso asociada** | KAN-04 |
| **Descripción** | Como desarrollador frontend, quiero maquetar el panel principal del cliente mostrando el saldo recuperado del backend de forma clara.|
| **Tareas requisito** | Ninguna |

![](../videos/a.mp4)
