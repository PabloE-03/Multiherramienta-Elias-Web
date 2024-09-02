
# Multiherramienta Elías - Web
Documentación de la web del proyecto <b>Multiherramienta:</b>
## Índice
- [Introducción](#introducción)
- [Tecnologías](#tecnologías)
- [Dependencias](#dependencias)
- [Manual de instalación](#manual-de-instalación)
- [Extra](#extra)

## Introducción
La web de <b>multiherramienta elías</b> se encarga de que los usuarios puedan interactuar con los microservicios del servidor anotando las capturas que van realizando además de guardar las tareas que necesiten en su día a día, se adapta tanto para ordenadores de escritorio, portátiles y móviles gracias al diseño responsivo que tiene, la web contiene 4 apartados con los que el usuario pueda interactuar siendo los mismos el apartado de loggin/home, apartado de configuración, apartado de pesca y apartado de To Do List, siendo el diseño de cada apartado sencillo y cómodo para la vista del usuario.

## Tecnologías
Las tecnologías que se han decidido usar para el desarrollo de la web son:
 - Vue.js: es un framework de JavaScript basado en componentes que es sencillo de usar y facilita un desarrollo muy rápido gracias a la estructura de sus ficheros organizados en código JS/HTML/CSS que permiten una organización del mismo sin tener que estar cambiando o comprobando ficheros conforme avance el desarrollo
 - Vite: es una herramienta de compilación que permite crear fácilmente proyectos de Vue.js y React, que además posee una compilación empaquetando en código en Rollup creando recursos estáticos optimizados directamente para subir el proyecto a producción 
 - SASS: es un preprocesador que convierte css en un lenguaje de programación gracias a que permite el uso de variables, condicionales, bucles, etc. Además de que nos permite generar estilos como un componente e insertarlo en reglas sin que tengamos que repetir código
 
 ## Dependencias
 Una vez conocidas las tecnologías ( Vue.js, SASS, Vite ) hay dependencias dentro de ellas que facilitan y aceleran el desarrollo de la web:

 ### Dependencias de Vue.js
 - vue-router: vue-router es el enrutador de vue que permite crear rutas y asociarlas a los componentes dando lugar a un almacenamiento organizado de los componentes de ka web y sobre permite guiar al usuario para que sepa en todo momento en que parte de la web está ubicado
 - pinia: pinia es un gestor de estados que permite guardar y compartir información entre componentes sin estar usando props en cada componente para comunicar información entre ellos

 ### Dependencias de sass
 - sassdoc: sassdoc es una herramienta que crea un html con la documentación de las variables, mixings y funciones que se usan en sass 

## Manual de instalación
Para ejecutar el proyecto se requiere tener [Node.JS](https://nodejs.org/dist/v20.17.0/node-v20.17.0-x64.msi) y [NVM](https://github.com/coreybutler/nvm-windows/releases/download/1.1.12/nvm-setup.exe), node lo requerimos para gestionar las dependencias de Vue, SASS, Vite, y ejecutar el arranque y compilación que Vite ofrece, NVM lo requerimos ya que necesitamos la versión de node 20.11.1 para ejecutar SASS y sassdoc.

### Versionado de node
Una vez tengamos node tendremos que ajustar su versionado ya que la dependencia de nodesass para ejecutar sass en Vue js requiere de la versión de node 20.11.1 o superior para ejecutarse para ello ejecutamos los siguientes comandos:

Instalación de la versión de node:
```console
nvm install 20.11.1
```

Cambio de la versión de node:
```console
nvm use 20.11.1
```

Comprobación de la versión:
```console
node --version
```

### Instalación de dependencias
Nos dirigimos a la raiz del proyecto y ejecutamos:
```console
npm install
```

### Arranque del proyecto
Si queremos abrir un servidor donde comprobemos los cambios que realicemos sobre la web ejecutamos en la raiz del proyecto:
```console
npm run dev
```

En caso de que queramos que se ve en más dispositivos que estén conectados a la misma red ejecutamos:
```console
npm run dev -- --host
```

Aparecerán dos direcciones, localhost y la ip de la conexión wifi donde podremos conectarnos con los dispositivos que estén conectados

## Extra
Para los archivos .env que se usen para api keys o contraseñas la variable se ha de nombrar como VITE_(nombre_variable) por ejemplo para una api key la nombraríamos VITE_API_KEY = valor, esto se usa de esta forma ya que al ser un proyecto de Vue js no se usa el objeto process.env de node, ya que el proyecto está configurado como un módulo, es decir si queremos realizar importaciones deberemos de usar la sintaxis de JavaScript
