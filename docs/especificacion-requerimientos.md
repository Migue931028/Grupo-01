# Especificación de Requerimientos

## 1. Descripción del sistema

## 2. Integrantes

- Nombre: Alejandro Aponte Pérez
- Nombre: Miguel Angel Ortega
- Nombre: Samuel Soto Jojoa
- Nombre:
- Nombre:

## 3. Requerimientos Funcionales

### RF-01 - Registro Tutoría

#### Resumen
El sistema debe permitir a un profesor registrar una oferta de tutoría académica especificando su código, tema, fecha, hora de inicio y cupo máximo de estudiantes, para que posteriormente los estudiantes puedan consultar y reservar dicha tutoría

#### Entradas

| Entrada | Tipo de dato |               Descripción               |
|---------|--------------|-----------------------------------------|
|   ID    |    String    |  Código de identificación del profesor  |
|  tema   |    String    |  Contenido tematico de la tutoría       |
|  fecha  |   LocalDate  |  Día, mes y año de la tutoría           |
|  inicio |   double     |  Hora de inicio de la tutoría           |
|  cant   |   int        |  Cantidad máxima de estudiantes         |

#### Reglas o condiciones
- El profesor debe tener asignado el rol correspondiente para programar tutorías.
- El profesor debe estar autenticado en el sistema con un perfil activo.
- No se permitirá programar una tutoría para una fecha anterior a la fecha actual
- La cantidad máxima de participantes deberá estar entre 1 y 10 estudiantes

#### Salidas

| Salida | Tipo de dato |                Descripción               |
|--------|--------------|------------------------------------------|
|  mesg  |   String     |   Un mensaje de confirmación             |
|  cod   |   String     |   Identificador de la tutoría            |

#### Resultado esperado
El sistema guarda la tutoría dejándola disponible para la consulta de los estudiantes y, como resultado, genera un ID único notificando al profesor sobre el registro exitoso.

### RF-02 - [Nombre del requerimiento]

#### Resumen

#### Entradas

| Entrada | Tipo de dato | Descripción |
|---|---|---|

#### Reglas o condiciones

#### Salidas

| Salida | Tipo de dato | Descripción |
|---|---|---|

#### Resultado esperado


### RF-03 - [Nombre del requerimiento]

#### Resumen

#### Entradas

| Entrada | Tipo de dato | Descripción |
|---|---|---|

#### Reglas o condiciones

#### Salidas

| Salida | Tipo de dato | Descripción |
|---|---|---|

#### Resultado esperado


### RF-04 - [Nombre del requerimiento]

#### Resumen

#### Entradas

| Entrada | Tipo de dato | Descripción |
|---|---|---|

#### Reglas o condiciones

#### Salidas

| Salida | Tipo de dato | Descripción |
|---|---|---|

#### Resultado esperado


## 4. Gestión de Versiones

### Ramas utilizadas

### Proceso de integración

### Conflictos encontrados
