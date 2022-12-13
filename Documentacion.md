# Documentacion

## Ambientes de Desarrollo

### Front-end

#### Setup

Antes de comenzar a codear es necesario tener instalado VSCode, Node.js y Chrome, utilizamos la extension `git Graph` de VSCode para manejar versionado. Una vez clonado el proyecto de nuestra repo debes correr `npm i` para instalar todos los paquetes requeridos por el proyecto.

Para iniciar un servidor local de prueba se utiliza el comando `npm run start`.

#### Buenas practicas

Se pide que se utilize el siguiente esquema para realizar cambios en la estructura del proyecto a la hora de agregar archivos:

```
.
├─ components
│   └─ simpleComponent
│       ├─ simpleComponent.module.scss
│       └─ simpleCOmpoennt.js
├─ directives
│   ├─ directivaCompleja
│   │   ├─ directivaCompleja.js
│   │   └─ directivaCompleja.scss
│   └─ directivaSimple.js
├─ models
│   └─ className.model.js
├─ pages
│   └─ login
│       ├─ components
│       │   └─ simpleComponent
│       │       ├─ simpleComponent.module.scss
│       │       └─ simpleCOmpoennt.js
│       ├─ login.module.scss
│       └─ login.js
├─ scss
│   ├─ _colors.scss
│   └─ _globalTheme.scss
├─ services
│   └─ apiConnection.js
├─ utils
│   └─ parseBool.js
├─ App.js
├─ App.scss
├─ App.test.js
├─ Context.js
└─ Routes.js
```

Para realizar un feature nueva se crea una rama proveniente de `develop` con el numero de requerimiento y un nombre comprensible, ejemplo: `#45-template-login`. En el mejor de los casos esta rama se mergea a `develop` cuando se termina.

Una vez testeada la estabilidad de la rama de `develop` esta se mergea a la rama `main` y se crea una _tag_ con el numero de version correspondiente.

### Principales partes de la aplicación y cómo se conectan

La aplicación se compone de 2 partes principales que son:
Actividad: Se da la interacción del usuario con el aplicativo, representa cada interfaz de usuario (página principal, creación del propiedad, detalle del propiedad reservas), las cuales se conecta por medio de una api al back y trayendo consigo cada dato almacenado, permitiendo crear o realizar una consulta.

Servicios: Brinda una conexión entre la api y la interfaz de usuario en la cual dicho usuario puede realizar filtros, búsquedas, registrarse o realizar reservas dentro de la misma.

### APIs disponibles y su documentación (pueden linkear a un sitio externo)

El equipo utilizó Swagger para la documentación de la API
http://localhost:8080/swagger-ui/index.html/

### Testing y Calidad

Para asegurar la calidad del software durante éste proyecto se realizaron pruebas exploratorias libres las cuales nos permitieron tener un enfoque más amplio sobre el uso de la aplicación y también nos permitió realizar un informe más completo ya que durante estas pruebas se puede evidenciar la necesidad de generar más casos de pruebas.

Link al Reporte Final y Casos de prueba ejecutados:
https://docs.google.com/spreadsheets/d/1vvhWIxnokFKOzOPjiKJ8rnLsjr-Gwll3DEeeuWUTwK8/edit?usp=sharing

### Base de datos
-Diagrama
![Alt text](DER%20DigitalBooking.png "Diagrama de base de datos Digital Booking")

-[Script creación base de datos](Script%20DB.txt)

### Back-end
Antes de comenzar, es necesario tener instalado el IntelliJ IDEA (u otro IDE de preferencia). Se debe modificar las variables de entorno para que coincida con la base de datos a la que apunte, poniendo el usuario y contraseña correspondientes. Luego, correr el programa, el cual generará en la base de datos las tablas pertinentes.