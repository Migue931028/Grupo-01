# Especificación de Requerimientos

## 1. Descripción del sistema
El sistema es una plataforma web para centralizar y gestionar el proceso de tutorías académicas en la Universidad, eliminando la coordinación informal previa entre profesores y alumnos.

El sistema cubre el ciclo de vida completo de una tutoría mediante cuatro procesos clave:

Gestión de la oferta: Permite a los docentes programar tutorías especificando sus datos, fecha, hora y límite de participantes, asignándoles un ID único tras validar las restricciones de agenda y aforo.

Búsqueda y consulta: Ofrece a los estudiantes un buscador por fecha y tema para visualizar las tutorías activas junto con los cupos restantes en tiempo real.

Inscripción de cupos: Valida la elegibilidad del estudiante (estado activo, cupo libre y no estar registrado previamente) para confirmar su asistencia y restar el cupo correspondiente.

Cancelación de registros: Permite a los alumnos dados de alta anular su asistencia antes del inicio de la sesión, liberando automáticamente el espacio para otros usuarios.

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

### RF-02 - consulta-tutorias 

#### Resumen
Los estudiantes podrán consultar las tutorías que se encuentran disponibles. Indicando la fecha y asignatura de interes

#### Entradas

| Entrada | Tipo de dato | Descripción |
|---|---|---|
|01-Fecha|LocalDate|fecha a consultar|
|02-Asignatura|String|Asignatura a consultar|

#### Reglas o condiciones
- Condicion 1. si no hay tutorias disponibles, se mostrara un mensaje informandolo 

#### Salidas

| Salida | Tipo de dato | Descripción |
|---|---|---|
|01-ID|String|identificador de la tutoria|
|02-Tema|String|tema de la consultoria|
|03-profesor|String|profesor responsable de la tutoria|
|04-fecha|LocalDate|fecha de la tutoria|
|05-hora|double|hora de la tutoria|
|06-cupos|Int|cupos disponibles|
|07-mensaje|String|mensaje en caso entrar o no|

#### Resultado esperado
Se muestra la informacion de la tutoria a consultar. 


### RF-03 - [Inscribir estudiante en tutoría]

#### Resumen
Permite a un estudiante registrar su participación en una tutoría académica de su interés utilizando su código estudiantil y el identificador de la tutoría. Al procesar la solicitud, el sistema registra la inscripción, actualiza la disponibilidad de cupos y muestra el mensaje correspondiente al resultado de la operación.

#### Entradas

| Entrada | Tipo de dato | Descripción |
|---|---|---|
codigo estudiantil|string|el estudiante ingresara su código de estudiante
id|string|el estudiante ingresara el id de la tutoría 
#### Reglas o condiciones
- La tutoría deberá tener cupo disponible para poder solicitar inscripción
- Para poder inscribirse el estudiante necesitara estar activo en la universidad
- la tutoría deberá previamente existir
-  el estudiante no podrá encontrarse previamente inscrito en una tutoría

#### Salidas

| Salida | Tipo de dato | Descripción |
|---|---|---|
inscripcion exitosa| string|mensaje de confirmacion que se registro con exito
condicion necesaria|string| mensaje mostrando la informacion de la situacion

#### Resultado esperado
El sistema registra exitosamente la inscripción del estudiante a la tutoría, reduce en uno (1) la cantidad de cupos disponibles y despliega un mensaje de confirmación en pantalla.

(En caso de fallo, el sistema no realiza el registro ni modifica los cupos, y despliega un mensaje notificando la causa del error).


### RF-04 - Cancelacion inscripcion 

#### Resumen
un estudiante que ya se encuentre inscrito podrá cancelar su participación utilizando su código estudiantil y el identificador de la tutoría. La cancelación solamente podrá realizarse si existe una inscripción previa y si la tutoría aún no ha comenzado. 

#### Entradas

| Entrada | Tipo de dato | Descripción |
|---|---|---|
|01-IdEstusiante|String|codigo estudiantil del estudiante que quiere cancelar|
|02-ID|String|identificador de la tutoria|

#### Reglas o condiciones
- Condicion 1. La cancelación solamente podrá realizarse si existe una inscripción previa y si la tutoría aún no ha comenzado.
- - Condicion 2. Si no es posible realizarla, deberá mostrarse un mensaje indicando el motivo.

#### Salidas

| Salida | Tipo de dato | Descripción |
|---|---|---|
|01-mensaje|String|mensaje de cancelacion exitosa|

#### Resultado esperado
Cuando la cancelación sea realizada correctamente, el sistema deberá eliminar la inscripción, liberar nuevamente el cupo correspondiente e informar al estudiante que la operación fue exitosa.


## 4. Gestión de Versiones

### Ramas utilizadas
- main
- dev
- docs/Gestión-de-versiones
- feature/rf01-registro-tutoria
- feature/rf02-consulta-tutorias-rf04-cancelacion-inscripcion
- feature/rf03-inscripcion-tutoria
### Proceso de integración
Primero creamos la rama dev a partir de main. Posteriormente, cada integrante trabajó en una rama individual derivada de dev para, finalmente, integrar los cambios y verificar que no existieran conflictos
### Conflictos encontrados
No tuvimos ningún conflicto como equipo
