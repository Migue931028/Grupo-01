# Especificación de Requerimientos

## 1. Descripción del sistema

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
- dev
- feature/rf02-consulta-turotias
- feature/rf04-cancelacion-inscripcion


### Proceso de integración

### Conflictos encontrados
