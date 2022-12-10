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

Una vez testeada la estabilidad de la rama de `develop` esta se mergea a la rama `main` y se crea una *tag* con el numero de version correspondiente.