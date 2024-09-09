> Detalla en esta sección los prompts principales utilizados durante la creación del proyecto, que justifiquen el uso de asistentes de código en todas las fases del ciclo de vida del desarrollo. Esperamos un máximo de 3 por sección, principalmente los de creación inicial o  los de corrección o adición de funcionalidades que consideres más relevantes.
Puedes añadir adicionalmente la conversación completa como link o archivo adjunto si así lo consideras


## Índice

1. [Descripción general del producto](#1-descripción-general-del-producto)
2. [Arquitectura del sistema](#2-arquitectura-del-sistema)
3. [Modelo de datos](#3-modelo-de-datos)
4. [Especificación de la API](#4-especificación-de-la-api)
5. [Historias de usuario](#5-historias-de-usuario)
6. [Tickets de trabajo](#6-tickets-de-trabajo)
7. [Pull requests](#7-pull-requests)

---

## 1. Descripción general del producto

**Prompt 1:**
Conoces la ley Colombiana que obliga a los hoteles a registrar datos de sus huéspedes durante el checkin?.  Qué exige esa ley en cuanto a información y al proceso de registro

**Prompt 2:**
Enumera los datos obligatorios que se deben registrar en el libro de huéspedes

**Prompt 3:**
Actúa como Product Owner.

Muchos hoteles en Colombia durante el check-in registran los datos de sus huéspedes en un libro físico; esto ocasiona principalmente demoras en el proceso de check-in, errores en el registro de datos y molestias en los huéspedes frecuentes que deben dictar al recepcionista una y otra vez la misma información.      

Un hotel nos contactó para mejorar su proceso de Registro de Datos Personales permitiendo que dichos datos se registren o actualicen desde un formulario web.

El hotel no tiene sistema de gestión hotelera; las reservas las registran en excel. 

Objetivo del Producto: 
Aplicación web en donde los huéspedes puedan entrar a diligenciar sus datos, incluso antes del check-in, y el hotel pueda gestionar esos registros.  
Se debe tener en cuenta las exigencias de la Ley Colombiana que me informaste anteriormente.

Funcionalidades Principales:  
  - Los huéspedes entran a una página web en la que ingresan un número de reserva y documento de identidad; si en la base de datos hay una reserva que coincida con esos datos, se les dirigirá al formulario de Registro o Actualización de Datos.
  - Durante el check-in el recepcionista consulta la reserva y verifica que los datos registrados por el huesped coincidan con los datos que contiene el documento de identificación físico, y realizará las modificaciones que se requiera para los datos que no coinciden.
    Si el huesped no registró/actualizó datos antes de iniciar su check-in, el recepcionista podrá hacerlo por él (durante el check-in). 
  - Para las reservas que tengan más de un huesped asociado se debe poder registrar los datos de todos los huéspedes de la reserva. 
  - Para simplificar el formulario de Registro o Actualización de datos se pide solo los datos personales; datos como tipo de alojamiento, fechas de estadía, medio de pago se asume que están registrados en el sistema de Reservas que utiliza el hotel.
  - Las reservas se seguirán registrando como el hotel lo hace hasta el momento, pero vía e-mail se envía al usuario link y número de reserva para que ingrese a registrar sus datos.

Stack: 
  - Node.js para el backend
  - AngularJS para el frontend
  - Base de datos Firebase
  - La web se desplegará en la nube Google Cloud Platform
  
Se ha identificado que este proceso es muy similar con el del registro de datos en otro tipo de negocios, como la reserva de zonas sociales en conjuntos y edificios residenciales, por lo cual se espera que este MPV pueda evolucionar hasta hacerse genérico y cubrir cualquier Registro de Datos para Reservas Tipo Check-in.  


Tu tarea es definir, diseñar y documentar un Mínimo Producto Viable para la aplicación web que te describí, siguiendo las fases de: 
  1. investigación y análisis
  2. casos de uso
  3. modelado de datos
  4. diseño de arquitectura alto nivel 

Adicionalmente avanzaremos en la planificación del proyecto, definiendo: 
  5. Historias de usuario
  6. Tickets de trabajo
  
Yo te iré indicando el momento en el que empezaremos a trabajar cada fase. 

1. **Iniciemos con la fase 1. investigación y análisis.**
Créame un archivo markdown que contenga: 
- Propósito del producto: Qué valor aporta, qué soluciona, y para quién.
- Características y funcionalidades específicas que tiene el producto para satisfacer las necesidades identificadas; enuméralas. 

### **Casos de uso:**

**Prompt 1:**
Ahora eres un analista de software experto. Enumera y describe brevemente los casos de uso más importantes a implementar para lograr el MVP descrito

**Prompt 2:**
En el caso 7. Gestión de Datos por el Personal del Hotel, tuviste en cuenta qué pasa cuando un huesped no ha registrado datos?.  Solo dime si hay que corregir el caso de uso

**Prompt 3:**
Estamos listos para diagramar los casos de uso.  Representa los 10 casos de uso en el tipo de diagrama más adecuado usando el formato plantUML; no olvides incluir los elementos  connections, directions, y packages para organizar mejor las funcionalidades del diagrama.  También quiero que el diagrama tenga skin blue.  Acorde a la sintaxis y buenas prácticas UML, define y describe lo que sea necesario.

---

## 2. Arquitectura del Sistema

### **2.1. Diagrama de arquitectura:**

**Prompt 1:**
Ahora actúa como un Arquitecto de Software Senior.  Cuáles serían los componentes principales de la aplicación, a nivel de arquitectura de software?; se breve

**Prompt 2:**
Podrías explicarme por qué recomendaste Firebase Realtime Database y no otras bases de datos propias de GCP como Firestore, mySQL o postgreSQL en Cloud SQL ?; se breve

**Prompt 3:**
Dadas las funcionalidades de la aplicación y nuestro stack actualizado, crea un diagrama de arquitectura de la aplicación; dámelo uno en formato mermaid y uno en formato plantuml.


### **2.2. Descripción de componentes principales:**

**Prompt 1:**
Ver prompt 1 del apartado **2.1. Diagrama de arquitectura:**

**Prompt 2:**
Ver prompt 3 del apartado **2.1. Diagrama de arquitectura:**


### **2.3. Descripción de alto nivel del proyecto y estructura de ficheros**

**Prompt 1:**

**Prompt 2:**

**Prompt 3:**

### **2.4. Infraestructura y despliegue**

**Prompt 1:**

**Prompt 2:**

**Prompt 3:**

### **2.5. Seguridad**

**Prompt 1:**

**Prompt 2:**

**Prompt 3:**

### **2.6. Tests**

**Prompt 1:**

**Prompt 2:**

**Prompt 3:**

---

### 3. Modelo de Datos

**Prompt 1:**
Ahora trabajaremos en la fase 3 de nuestro proyecto, el modelado de datos.  Ya que eres un Arquitecto de Software experto, aprovecharemos tu experiencia en diseño de datos para modelar la base de datos para nuestra aplicación web.  

Recuerdas las funcionalidades y el stack que tendrá la aplicación?; qué diagrama crees que se ajustaría mejor para visualizar nuestro modelo de BD?

**Prompt 2:**
Ahora si procede con la creación del Diagrama de Modelo de Documentos para nuestra base de datos. En el modelo se debe tener en cuenta como mínimo:
- Las colecciones que garantizan cubrir los 10 casos de uso que se definieron para la MVP de nuestra aplicación web
- La estructura interna de los documentos en cada colección (campos, tipos de datos y objetos anidados más importantes)
- Si hay variaciones en la estructura de los documentos de una misma colección, muéstrar la estructura de las variaciones que se necesiten
- Si hay documentos que contienen referencias a otros documentos, las flechas o líneas que dejan ver cómo se vinculan o relacionan los documentos entre sí

Dame el modelo en formato mermaid y plantUML

**Prompt 3:**
Tengo algunas observaciones con base en tu modelo de bd; vamos a revisarlas todas y al final de nuestra revisión me actualizas el código del diagrama; yo te indicaré cuándo hemos finalizado la revisión.   

Iniciemos con la revisión de la colección GUEST.  Qué opinas de: 
	1. Dividir el campo nombre como mínimo en nombres y apellidos
	2. En dónde se almacenaría el tipo de documento? 
	3. En qué mecanismo de firmado de documentos has pensado para poder almacenar la firma de los huéspedes en el campo string que propusiste?

---

### 4. Especificación de la API

No aplica

---

### 5. Historias de Usuario

**Prompt 1:**

**Prompt 2:**

**Prompt 3:**

---

### 6. Tickets de Trabajo

**Prompt 1:**

**Prompt 2:**

**Prompt 3:**

---

### 7. Pull Requests

**Prompt 1:**

**Prompt 2:**

**Prompt 3:**
