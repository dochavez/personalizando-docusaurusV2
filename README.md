#  👨🏼‍💻Personalizando-DocusaurusV2. 👨🏼‍💻 
## Tutorial Avanzado.
### Autor: Danny Chávez <br>

[![Twitter Follow](https://img.shields.io/twitter/follow/docusaurus.svg?style=social&label=Follow)](https://twitter.com/docusaurus)
[![npm](https://img.shields.io/npm/v/npm?style=plastic)](https://github.com/npm)
[![yarn](https://img.shields.io/badge/yarn-download-blue)](https://classic.yarnpkg.com/en/docs/install/#windows-stable)
[![gitbash](https://img.shields.io/badge/gitbash-download-blue)](https://git-scm.com/downloads)
[![nodejs](https://img.shields.io/badge/nodejs-download-blue)](https://nodejs.org/en/)
[![visualstudio](https://img.shields.io/badge/visual%20studio%20code-download-blue)](https://code.visualstudio.com/)
[![Docusaurus](https://img.shields.io/badge/docusaurus-download-green)](https://github.com/facebook/docusaurus)

* ## Resumen. 📔

Docusaurus es un generador de sitios estáticos de código abierto que convierte archivos Markdown en un sitio web de documentación. La herramienta está equipada con funcionalidades para el correcto versionamiento de los documentos, un avanzado buscador, la posibilidad de documentar y rediseñar nuestro sitio de documentación en tiempo real, integración con traducciones y muchas otras características que le ayudará a preocuparse menos por documentar o mejor dicho por hacer el proceso de documentación más sencillo y con acabado más agradable.

Si eres nuevo y quieres saber como se realiza el proceso de ***instalación, configuración y despliegue*** de tu sitio web de forma local y en línea, te invito a que mires este <a href="https://github.com/dochavez/DocusaurusV2" target="_blank">**tutorial**</a> donde te mostrare paso a paso lo que debe de realizar para que puedas probar esta poderosa y fácil herramienta. 

* ## Agregando un Título, lema e icono para el navegador.🏡

Cuando se instala Docusauru por primera vez, nos muestra una plantilla por defecto. La cual se ejecuta en la dirección **http://localhost:3000**. Esta plantilla contiene 3 elementos importantes:
- **Barra de Navegación:** la cual se encuentra en la parte superior de la plantilla.
- **Contenido Principal:** donde se agrega toda la información que el usuario observará.
- **Pie de Página:** la cual se encuentra en la parte final de la página.

Para agregar un titulo a nuestra plantilla, debemos de hacer lo siguiente:

1. Ubicar el archivo llamado **docusaurus.config.js**, una vez que tenemos el contenido del archivo procedemos a cambiar el título en la etiqueta "**title**". En nuestro caso pondremos ***Fábrica de Chocolate***
IMPORTANTE: El titulo que agreguemos, es el que se pondra en la ventana de navegacion de nuestro navegador web.

2. Agregamos un lema dentro de la etiqueta **tagline**. En nuestro caso pondremos ***Una Dulce Tentación***

3. Agregamos una imagen de formato **.ico**. Para esto debemos de reemplazar la imagen que se encuentra en la ruta **/static/img/favicon.ico**

* ## Agregando un nuevo color a nuestra página principal.🎆

Docusaurus trabaja con Hojas de Estilos conocidas como CSS, las cuales son implementadas en la plantilla que tenemos por defecto. Ademas, utiliza **Infima** que es un marco de estilo moderno para sitios web basados en contenido. Para cambiar el color principal de nuestra pagina principal hacemos lo siguiente:

1. Ubicar el archivo **custom.css** que se encuentra en la ruta **src/css/custom.css**
2. Modificamos el color que se encuentra en ```--ifm-color-primary:``` por cualquier otro código. Es importante destacar que **Infima** trabaja con dos parámetros importantes para las hojas de estilo; el primero es el **primary** y el segundo es el **dark**. Por lo tanto, ambos parámetros pueden ser cambiados para personalizar nuestro sitio.

* ## Modificando la Barra de Navegación.📌

Para agregar nuevas secciones dentro de nuestra Barra de Navegación debemos de seguir los siguientes pasos:

1. Ubicar el archivo llamado **docusaurus.config.js**
2. Agregamos el siguiente código dentro de **items**

```
   {
      label: 'Facebook',
      href: 'https://www.facebook.com',
      position: 'left' // también se puede ubicar a la derecha con el valor "right"
    },
      {
      label: 'Twitter',
      href: 'https://www.twitter.com',
      position: 'left',  
    },
    {
      label: 'Instagram',
      href: 'https://www.instagram.com',
      position: 'right',
    },
    {
      label: 'Whatsapp',
      href: 'https://www.whatsapp.com/',
      position: 'right'
    },
```
     
* ### PRO-TIPS: 😉
* Si queremos ocultar la Barra de Navegación cuando el usuario se desplace por nuestra Página Principal hacia abajo, podemos agregar la siguiente instruccion dentro de nuestro archivo **docusaurus.config.js** ```hideOnScroll: true,```

* Por otro lado, si queremos agregar un color diferente a nuestra Barra de Navegación, se puede hacer agregando la siguiente línea de código fuente ```style: 'dark',```

* ## Agregar un AVISO. 📢

Para agregar un aviso que se ponga en la parte superior de la Barra de Navegación, puedes utilizar el siguiente código fuente. El cual debes de ubicarlo encima de la directiva **footer**

```
announcementBar: {
  id: 'Aviso', // Any value that will identify this message.
  content:
    'Tutorial Avanzado sobre Docusaurus Versión 2 ya disponible! <a target="_blank" href="https://github.com/dochavez/personalizando-docusaurusV2">Ir al Repositorio</a>',
  backgroundColor: '#fafbfc', // Defaults to `#fff`.
  textColor: '#091E42', // Defaults to `#000`.
  isCloseable: false, // Defaults to `true`.
  
```

* ## Modificando nuestra Página Principal.🏗

Todo el contenido que mira el usuario cuando accede a nuestra página principal es por medio del archivo **index.js**. Por lo tanto, vamos a cambiar las imagenes y agregar más secciones a la misma. Para eso agregamos el siguiente código fuente debajo de **const features**:

```
{
    title: 'Es saludable!',
    imageUrl: 'img/undraw_healthy_options_sdo3.svg',
    description: (
      <>
        Alivia el estrés y es un antidepresivo natural.
      </>
    ),
  },
  {
    title: 'Una bebida relajante',
    imageUrl: 'img/undraw_coffee_break_j3of.svg',
    description: (
      <>
        El chocolate es una fuente de energia capaz de mejorar el estado de ánimo. 
        Contiene cafeína y es capaz de aumentar su resistencia al cansancio.
      </>
    ),
  },
  {
    title: 'Reuniones de Amigo',
    imageUrl: 'img/undraw_hang_out_h9ud.svg',
    description: (
      <>
        Reune a tus amigos con toda la tarde por delante para una buena selección
        de juegos de mesa o videojuegos, según las preferencias.
      </>
      
    ),
  },
  {
    title: 'Refresca tu cuerpo',
    imageUrl: 'img/undraw_hot_beverage_2vw3.svg',
    description: (
      <>
        Una buena bebida para pasar un excelente día!
      </>
    ),
  },
  {
    title: 'Supermercados y Tiendas',
    imageUrl: 'img/undraw_shopping_app_flsj.svg',
    description: (
      <>
        Lo puedes obtener en cualquier supermercado y tienda de conveniencia.
      </>
    ),
  },

  {
    title: 'Para mostrar amor',
    imageUrl: 'img/undraw_love_xfcv.svg',
    description: (
      <>
        El chocolate inclusive a sido usado para expresar nuestros sentimientos
        por nuestra persona favorita. :)
      </>
    ),
  },
```



  
  




