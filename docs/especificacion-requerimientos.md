# Especificación de Requerimientos

## 1. Descripción del sistema
El sistema es una plataforma web para centralizar y gestionar el proceso de tutorías académicas en la Universidad, eliminando la coordinación informal previa entre profesores y alumnos.

El sistema cubre el ciclo de vida completo de una tutoría mediante cuatro procesos clave:

Gestión de la oferta: Permite a los docentes programar tutorías especificando sus datos, fecha, hora y límite de participantes, asignándoles un ID único tras validar las restricciones de agenda y aforo.

Búsqueda y consulta: Ofrece a los estudiantes un buscador por fecha y tema para visualizar las tutorías activas junto con los cupos restantes en tiempo real.

Inscripción de cupos: Valida la elegibilidad del estudiante (estado activo, cupo libre y no estar registrado previamente) para confirmar su asistencia y restar el cupo correspondiente.

Cancelación de registros: Permite a los alumnos dados de alta anular su asistencia antes del inicio de la sesión, liberando automáticamente el espacio para otros usuarios.

## 2. Integrantes

- Nombre:
- Nombre:
- Nombre:
- Nombre:
- Nombre:

## 3. Requerimientos Funcionales

### RF-01 - [Nombre del requerimiento]

#### Resumen

#### Entradas

| Entrada | Tipo de dato | Descripción |
|---|---|---|

#### Reglas o condiciones

#### Salidas

| Salida | Tipo de dato | Descripción |
|---|---|---|

#### Resultado esperado


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
