npm-app

## Entorno de desarrollo Basado en Java Script basado en el stack MEAN (MongoDb,ExpressJs,AngularJS,NodeJs). Stack MEAN
Es uno de los entornos de desarrollo para el ecosistema JavaScript

## Workflow de desarrollo utilizando NodeJs y NPM Scripts:

NodeJs| npm: el primer paso consiste en instalar NodeJs, cabe destacar  que NodeJs es un entorno de ejecución para JavaScript construido con el motor de JavaScript V8 de chrome. trae incorporado su gestor de paquetes NPM(Node Package Manager) que no solo permite gestionar sus librerías y dependencias sino que también  se puede utilizar como automatizador de tareas a través de scripts.

Para instalar en Linux lo recomendable es instalarlo a través de su gestor de paquetes. en su web se encuentran las instrucciones para hacerlo.

### Pasos:
1. Abrir la terminal 
2. user root
3. apt update
4. apt install nodejs
5. nodejs -v
##### Actualizando nodeJs
6. apt update
7. apt install curl
8. curl -sL https://deb.nodesource.com/setup_12.x -o nodesource_setup.sh
9. bash nodesource_setup.sh
10. verifica gcc con (gcc -v); apt install gcc 
11. sudo apt-get install -y nodejs
12. verificando las versiones nodejs -v , npm -v 

Una vez tenemos instalado NodeJs + NPM tenemos todo para configurar nuestro entorno de desarrollo.

1. Iniciamos nuestro repositorio github
2. Creamos un nuevo repositorio (npm-app)
3. Clonamos el nuevo repositorio en nuestra maquina.

Una vez clonado empezamos la configuración.

## Inicializamos el proyecto NPM
Para comenzar nuestra configuración debemos inicializar el proyecto npm. ejecutando en la terminal  el comando **npm init**.

   Este asistente nos hará una serie de preguntas para ayudarnos a crear nuestro package.json inicial. Este es el archivo de configuración del proyecto, que contendrá toda la información sobre el mismo y sobre el cual escribiremos los scripts de automatización.

##### Debemos completar:
- package name: Es el nombre que identifica al proyecto. Por defecto completa el nombre del directorio actual. El nombre del mismo no puede contener caracteres en mayúscula.
- versión: (1.0.0) Versión de la app.por defecto es la 1.0 
- description: Breve descripcion del proyecto.
- entry point: (index.js) Punto de enytrada de la aplicación. Se recomienda dejar el que viene por defecto.
- test command: Comando para pruebas de funcionamiento. Lo dejamos vacío.
- git repository: (https://github.com/...) Repositorio Git. Como ya habíamos inicializado uno autocompletará con la URL de dicho repo.
- keywords: Conjunto de palabras clave relacionadas al proyecto. En este caso podríamos poner “frontend”, “boilerplate”, “proyecto”, “plantilla”, etc.
- license:(ISC) Tipo de licencia para el proyecto (MIT, ISC, etc).

Una vez completados estos datos nos dará un preview del package.json que está a punto de crear. Si todo está bien damos el OK.

Observar dentro de este archivo JSON la key “scripts”. Allí es donde escribiremos los scripts de automatización para nuestro workflow. Por ahora solo contiene un script de test con un mensaje de error, ya que no hemos definido uno al inicializar el proyecto. Como no tiene utilidad por el momento, procederemos a borrarlo y comenzaremos a agregar tareas de automatización a continuación.

## Módulos NPM y Scripts

Hay módulos NPM para casi todo. Son el equivalente a los paquetes o librerías de otros lenguajes de programación. Muchos de ellos traen una interfaz de línea de comandos -CLI o Command Line Interface- para poder hacer uso de ellos. Veamos como utilizarlos mediante un ejemplo.

Supongamos que nuestro proyecto requiere la utilización de SASS.

SASS (Syntactically Awesome Style Sheet) es un lenguaje de preprocesamiento de CSS que permite extender las características del CSS añadiendo funcionalidades como variables, funciones, mixins, herencia y nesting.

No vamos a extendernos mucho en este tema, pero básicamente un archivo escrito en SASS (extensiones .sass o .scss) se debe compilar para obtener como resultado un archivo .css tradicional, capaz de ser procesado por el navegador en el lado cliente. Para esto, vamos a usar la módulo disponible en NPM llamado node-sass.

Con Node, los módulos pueden instalarse de manera global, que los hace disponibles para todos los proyectos, o como dependencia local del proyecto sobre el cual estamos trabajando.

En este caso, vamos a instalarlo como dependencia local de desarrollo. Para ello debemos ejecutar en la terminal npm install node-sass --save-dev

Una vez finalizada la instalación podremos ver que la librería aparecerá como dependencia de desarrollo dentro del archivo package.json

##### palabras claves:
- entorno de ejecución
- motor de JavaScript V8 de Chorme
