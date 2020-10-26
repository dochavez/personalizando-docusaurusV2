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

![Barra de Navegacion](https://github.com/dochavez/personalizando-docusaurusV2/blob/main/Barra%20de%20Navegacion.jpg)     
     
     
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
![AVISO](https://github.com/dochavez/personalizando-docusaurusV2/blob/main/Agregando%20anuncio.jpg)


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
![index](https://github.com/dochavez/personalizando-docusaurusV2/blob/main/cambiando%20el%20index.jpg)

IMPORTANTE: Recuerda que todas estas imagnes que hemos puesto en nuestra página principal deben de estar adentro de nuestra carpeta **/img** que se encuentra en la ruta de nuestro proyecto **/static/img**

* ## Documentos.🖺

Para crear un documento que nos aparezca en nuestro sitio web debemos de seguir los siguientes pasos:

1. Crear un archivo con extensión **.md** dentro de la carpeta **docs**
2. Agregamos las siguientes directivas: 
```
---
id: doc4
title: La Historía del Chocolate
---
AGREGAR TU CONTENIDO AQUI
```
3. Luego, debes de agregar el título de la categoría en el archivo **sidebar.js**
```
'El Chocolate': ['doc4', 'doc5' ],
```

* ## Pestañas dentro de nuestro documento. 📑
Para agregar multiples pestañas dentro de nuestro documento, solo debemos de agregar el siguiente código:

```
<Tabs
  defaultValue="apple"
  values={[
    {label: 'Periodo Maya' , value: 'maya'},
    {label: 'Periodo Azteca', value: 'azteca'},
    {label: 'Periodo Europeo', value: 'europeo'},
  ]}>

  <TabItem value="maya">
  El pueblo maya, cuyo origen se remonta cada vez más atrás con cada avance en los estudios arqueológicos, ha dejado descripciones en forma de jeroglíficos que conforman la denominada escritura maya.  
  </TabItem>
    
  <TabItem value="azteca">
  El origen de la palabra cacao y chocolate es hoy en día una controversia entre los científicos estudiosos del término.
  </TabItem>
  
  <TabItem value="europeo">
  El descubrimiento del cacao tuvo varios episodios iniciales de contacto entre los conquistadores españoles, y los pueblos mesoamericanos.
  </TabItem>
  
</Tabs>

```
* ## Agrengando mensajes en nuestro documento.💬

También, en los documentos podemos crear una serie de **mensajes o llamadas** que pueden servir como referencia para el usuario en cuanto al tipo de información que deseamos mostrar. Para eso, podemos agregar el siguiente código dentro de nuestro archivo **.md**

```
:::note Nota
El contenido y el titutlo puede incluir markdown.
:::

:::tip Consejo
Aquí hay un útil consejo que te ayudará a desarrollar tu proyecto
:::

:::info Información
Información muy relevante y actualizada.
:::

:::caution Advertencia
Presta atención a esto que es muy importante!
:::

:::danger Peligro
Eliminar archivos del sistema no es recomendable!
:::
```

* ## Agregas bloques para mostrar nuestro código fuente.🪟

Recuerda que una de las caracteristicas principales de Docusaurus es poder compartir información de forma ordenada. Por lo tanto, si estas trabajando en algun proyecto que incluya una actualización de código fuente, puedes agregar **bloques** adentro de tus documentos para que muestren la información que deseas compartir. Para esto solo debes de agregar el siguiente código dentro de nuestros archivos **.md** en donde puedes sustituir el valor del titulo que se encuentra en la directiva ```jsx title="Poner tu título aquí"```:

```jsx title="Nueva funcion en HelloCodeTitle.js"

function HelloCodeTitle(props) {
  return <h1>Hello, {props.name}</h1>;
}
```
Otra interesante propiedad de los bloques es que podemos agregar un código fuente y dentro del mismo podemos resaltar una o varias líneas de código por si queremos hacer énfasis en que hemos realizado alguna modificación en una función especifica o hacer referencia a algun tópico que estemos abordando. Por ejemplo, agrega el siguiente código dentro de tu archivo **.md** y notaras como algunas líneas son resaltadas.

```jsx {3}
function HighlightSomeText(highlight) {
  if (highlight) {
    return 'This text is highlighted!';
  }

  return 'Nothing highlighted';
}
```

* ## Incorporando imagenes en nuestros documentos.📸

A veces una imagen puede reflejar muchas palabras que deseamos expresar, es por eso que con Markdown podemos incluir imagenes dentro de nuestro documento. Simplemente agregamos la siguiente línea de comando. 

```
# Mi doc5

<img src={require('./assets/docusaurus-asset-example-banner.png').default} />

or

![](./assets/docusaurus-asset-example-banner.png)
```

* ## Incorporando archivos de descarga en nuestros documentos. 📂

De la misma manera que hicimos con el apartado anterior, también podemos poner a disposición enlaces de descargas para nuestros usuarios. Estos enlaces nos pueden llevar a descargar videos, audios, documentos en pdf, etc. Para hacer esto, podemos agregar la siguiente linea de comando dentro de nuestro archivo en el cual estamos editando nuestro documento.

```
# Mi doc5

<a
  target="_blank"
  href={require('./assets/docusauru_github.pdf').default}>
  Descargar documento PDF
</a>

or

[Descargar documento PDF](./assets/docusauru_github.pdf)

```
* ## Es hora de crear Blogs. 💪

Si ya llegastes hasta esta sección del tutorial, quiero decirte que estas poniendo tu máximo esfuerzo para alcanzar tus logros. Es por eso que ahora vamos a ver la parte de crear Blogs que van a estar en nuestro sitio web. Por definición podemos decir que un **Blog o bitácora** es *es un sitio web que incluye, a modo de diario personal de su autor o autores, contenidos de su interés, que suelen estar actualizados con frecuencia y a menudo son comentados por los lectores*. Por lo tanto, para poder crear **Blogs** podemos incorporar el siguiente código fuente:

```
---
title: Docusaurus Avanzado
author: Danny Chavez
author_title: Autor del Tutorial
author_url: https://github.com/dochavez
author_image_url: https://graph.facebook.com/611217057/picture/?height=200&width=200
tags: [persona, docusaurus-v2]
description: Blog personal.
image: https://i.imgur.com/mErPwqL.png
hide_table_of_contents: false
---
Este es mi tutorial sobre Docusaurus. Cubriremos aspectos avanzados.

```

Donde:

- **autor:** el nombre del autor que se mostrará.
- **author_url:** la URL a la que se vinculará el nombre del autor. Esto podría ser una URL de perfil de GitHub, Twitter, Facebook, etc.
- **author_image_url:** la URL de la imagen en miniatura del autor.
- **author_title:** una descripción del autor.
- **title:** el título de la publicación del blog.
- **etiquetas:** una lista de cadenas para etiquetar en su publicación.
- **borrador:** una marca booleana para indicar que la publicación del blog está en progreso y, por lo tanto, aún no debe publicarse. Sin embargo, los borradores de las publicaciones del blog se mostrarán durante el desarrollo.
    descripción: la descripción de tu publicación, que se convertirá en <meta name = "description" content = "..." /> y <meta property = "og: description" content = "..." /> en <head >, utilizado por los motores de búsqueda. Si este campo no está presente, estará predeterminado en la primera línea del contenido.
- **imagen:** imagen de portada o miniatura que se utilizará al mostrar el enlace a su publicación.
- **hide_table_of_contents:** si ocultar la tabla de contenido a la derecha. Por defecto es falso.


Es imporntante destacar que para publicar en el blog, cree un archivo dentro del directorio del blog con un nombre formateado de YYYY-MM-DD-my-blog-post-title.md. La fecha de publicación se extrae del nombre del archivo.






  




