# Anexos-introdución al Diseño Orientado a Objetos

## Decripción al diseño orientado a objetos
<p>Un paradigma de programación que se basa en la abstracción de entidades del mundo real , que organiza el
software en entidades llamadas (objetos), que contienen tanto datos como comportamientos</p>


## Los cuatro fudamentos de diseño orientado a objetos
![Captura de pantalla 2025-03-31 124246](https://github.com/user-attachments/assets/df2aef0d-7f49-45a5-9bab-18097bf8171e)

## Requisitos iniciales del sistema
<p>1:Poder pedir un turno</p>
<p>2:historial de turnos de cada paciente</p>
<p>3:Aviso de confirmación de turno al medico</p>
<p>4:agenda de turnos se registra la fecha y hora del turno y estado del turno</p>
<p>5: registrar a los pacientes como a los profesionales de la salud</p>

## Casos de uso 
### 1 poder pedir un turno 
 **Actor(es):** Recepcionista, paciente  
- **Descripción:** El recepcionista ingresa los datos del paciente  al sistema para pedir un turno .  
- **Flujo principal:**  
  1. El recepcionista accede al módulo de pacientes.
  2. El paciente le dice la fecha del turno y cual es su problema  
  3. Ingresa la fecha del turno y la especialidad.  
  4. Guarda el registro y se muestra una confirmación.  
- **Precondiciones:**  
  - El paciente  debe estar registrado previamente en la base de datos .  
- **Postcondiciones:**  
  - El paciente le queda registrado el turno  en la base de datos de turnos.  

### 2 historial de turnos de cada paciente 
 **Actor(es):**  Medico  
- **Descripción:** El  Medico ingresa los datos del turno al historial   .  
- **Flujo principal:**  
  1. El Medico accede al módulo historial de turnos de cada paciente.  
  2. Ingresa los datos importantes del turno y la medicacion recertada (si es necesario)  .  
  3. Guarda el registro y se muestra una confirmación .  
- **Precondiciones:**  
  - El paciente  debe tener  un turno en el sistema.  
- **Postcondiciones:**  
  - El paciente le queda registrado el turno y todo  los datos y la medicacion (si es necesario) dada en la consulta .  

### 3 Aviso de confirmación de turno al medico
 **Actor(es):**  paciente , medico
- **Descripción:** El  paciente confirma al turno y el medico lo recibe.   .  
- **Flujo principal:**  
  1. Al paciente le llega un gmail y dentro si confima o no el turno .  
  2. La confirmación del turno se guarda  .  
  3. Y al medico le llega la notificación de la confirmación .  
- **Precondiciones:**  
  - El paciente  debe haber sacado  un turno  en el sistema.  
- **Postcondiciones:**  
  - Al medico  le queda registrado el la confirmación del turno.
    ### 4 agenda de turnos se registra la fecha y hora del turno y estado del turno.
 **Actor(es):**  Recepcionista y Medico
- **Descripción:** El  recepcionita  pueden consultar los turnos del dia o de otros dias.   .  
- **Flujo principal:**  
  1. El recepcionista consulta los turnos del dia y le dice al medico cuales son los turnos del dia y hora .  
  2. El recepcionista borra los turnos cancelados  .  
  3. El recepcionista confirma los cambios .
     
- **Precondiciones:**  
  - El recepcionista debe haber agendado el turno y el paciente confirmado para ese dia.  
- **Postcondiciones:**  
  - El medico y el recepcionista saben los turnos del dia
    ### 3 Aviso de confirmación de turno al medico
 **Actor(es):**  paciente , medico
- **Descripción:** El  paciente confirma al turno y el medico lo recibe.   .  
- **Flujo principal:**  
  1. Al paciente le llega un gmail y dentro si confima o no el turno .  
  2. La confirmación del turno se guarda  .  
  3. Y al medico le llega la notificación de la confirmación .  
- **Precondiciones:**  
  - El paciente  debe haber sacado  un turno  en el sistema.  
- **Postcondiciones:**  
  - Al medico  le queda registrado el la confirmación del turno.
    ### 5  registrar a los pacientes como a los profesionales de la salud.
 **Actor(es):**  Recepcionista , Medico o paciente .
- **Descripción:** El  recepcionita  registra al paciente o al medico nuevo en la base de datos   .  
- **Flujo principal:**  
  1. El recepcionista recibe la información del medico o paciente nuevo .  
  2. El recepcionista los ingresa en la base de datos .  
  3. El recepcionista confirma el ingreso .
     
- **Precondiciones:**  
  -El medico o paciente no debe estar registrado .  
- **Postcondiciones:**  
  - El medico o el paciente quedan registrados
## Boceto inicial del diseño de clases
