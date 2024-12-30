# Ejercicio Práctico: Integración Completa del Sistema del Hospital con ReactJS
## Descripción 
En esta actividad, todas las vistas del sistema del hospital (Home, Servicios, Equipo Médico, Citas) deberán integrar componentes avanzados y técnicas de optimización de ReactJS.Ademas, se manejarán interacciones complejas con datos a través de APIs.

### Estructura principal de carpetas
- **assets:** carpeta que contiene los elementos graficos del sitio web, en este caso, imagenes.
- **components:** carpeta que contiene todos los componentes creados y utilizados en el sitio web, como header y footer.
- **public:** contiene los archivos JSON con los cuales se trabaja.
  - appointment.json: archivo que contiene toda la información asociada las citas medicas registradas
  - doctors.json: archivo que contiene toda la información respecto a cada doctor de la clinica.
  - services.json: archivo que contiene toda la información respecto a cada servicio medico ofrecido por la clinica a sus pacientes.
- **views:** contienen la estructura basica de las 5 pantallas principales del sitio web, desde ellas se llaman y utilizan los componentes.
  - contact: contiene la pantalla asociada al formulario de contacto.
  - home: pantalla principal del sitio, aqui, se listan los servicios ofrecidos por la clinica, llamando al componente ServiceList.
  - services: presenta información asociada al equipo medico de la clinica, llamando al componente DoctorCard.
  - RegisterAppointment: presenta un listado con todas las citas medicas registradas.
  - Appointment: contiene el formulario que permite agendar una cita medica, llamando al componente AppointmentForm.

### Implementación de Vistas Complejas con ReactJS
en las tres vistas principales se implementaron las siguientes funcionalidades: 
- **Home:** cuenta con la lista de servicios pero solo de aquellos considerados destacados, ademas de una sección con información general de la clinica. 
- **Services (equipo medico):** Muestra información de los doctores utilizando el componente DoctorCard para cada miembro del equipo y se implementa un filtro por especialidad.
- **Appointment (citas):** al formulario para reservar citas ya implementado con hooks, se le incorporan validaciones.
### Optimización del DOM Virtual y Uso de Fragmentos
A lo largo del sitio web se utilizan fragmentos para evitar el uso de <div> innecesarios en el codigo, ademas, se trabaja de forma efectiva con el DOM virtual, logrando que solo los elementos necesarios se actualicen, optimizando el rendimiento de la aplicación.
### Uso de Referencias y Callbacks
En los formularios de contacto y reservar cita se utilizan referencias para enfocar el primer input al ingresar en la vista, ademas, se utilizan referencias para navegar por la pagina principal Home, al presionar el boton de la sección princiapl "Conoce testimonios" la pagina se desplaza directamente a esa sección ubicada al inferior de Home.
### Manejo de Datos con API REST Simulada
En las vistas de services donde se cargan los datos del equipo medico de public/doctors.json y en home donde se cargan los servicios disponibles de la clinica de public/services.json se simula la obtención de datos de una API REST utilizando fetch y se manejan las respuestas de manera asíncrona con async/await.
### Optimización de Rendimiento y Uso de Profiler
Se utiliza Profiles para evaluar el rendimiento de la aplicación en los componentes donde se manejan mas volumenes de datos, como DoctorCard en services, ServicesList en home y TableList en registerAppointment.
### Comprobación de Tipos con PropTypes
Se implementan PropTypes en todos los componenetes que reciben props, asegurando que el tipo de dato es el correcto, de lo contrario se señala el error a travez de la consola en las herramientas del desarrollador del navegador.

 ### Visualización del proyecto
Para visualizar este proyecto se necesita que previamente cuentes con la instalación de:
- **Git**: [sitio de descarga] (https://git-scm.com/downloads)
- **Node.js**: [sitio de descarga] (https://nodejs.org/en/download/package-manager)
- **Visual Studio Code**: [sitio de descarga] (https://code.visualstudio.com/download)
  
Una vez que ya cuentes con lo descrito anteriormente, debes clonar este repositorio en una carpeta local, mediante el siguiente comando:
```bash
git clone https://github.com/lorenasotosanmartin/M4_EP1.git
```
cuando ya este clonado, escribir el siguiente comando en la consola: 
```bash
npm  i
```
y ejecutar el comando, para inicializar el proyecto: 
```bash
npm run dev
```
Finalmente, para visualizar el proyecto en tu navegador debes abrir la url http://localhost:3000/ 
