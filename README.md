# DOM-en-JavaScript
En esta seccion veremos los metodos y propiedades de JavaScript a fin de manipular el DOM o Document Objet Model de la esctructura HTML o XML.


# En que consiste el DOM o Document Object Model

El Document Object Model es una representación estructural en forma de árbol de un documento HTML o XML. La estructura del DOM sigue una jerarquía donde cada elemento del documento se representa como un nodo en el árbol. 

Del concepto precedente, surge que los "elementos" del documento se representan como un "nodo", aqui hay dos palabras fundamentales para entender, el elemento y el nodo.

  # Cuales son los elementos dentro de un archivo HTML o XML?
  
  Tanto en un archivo HTML como en un archivo XML, se pueden encontrar diversos elementos que conforman la estructura del documento. Estos se puede dividir en:
  
1 - Etiquetas o tags:
    
    <html>: Define el elemento raíz del documento HTML.
    <head>: Contiene información sobre el documento, como el título y enlaces a archivos externos.
    <body>: Contiene el contenido visible del documento.
    <div>: Crea un contenedor genérico para agrupar elementos y aplicar estilos.
    <p>: Define un párrafo de texto.
    <h1>, <h2>, <h3>, <h4>, <h5>, <h6>: Definen encabezados de diferentes niveles.
    <a>: Crea un enlace a otra página o recurso.
    <img>: Inserta una imagen en el documento.
    <ul>: Crea una lista desordenada.
    <ol>: Crea una lista ordenada.
    <li>: Define un elemento de lista en <ul> o <ol>.
    <table>: Crea una tabla para mostrar datos.
    <tr>: Define una fila en una tabla.
    <td>: Define una celda en una tabla.
    <form>: Crea un formulario para recopilar datos del usuario.
    <input>: Crea un campo de entrada en un formulario.
    <button>: Crea un botón interactivo.
    
2 - Atributos: Los atributos proporcionan información adicional a las etiquetas. 

        <h1 style="color: blue;">Título principal</h1>
        <!-- El atributo "style" define estilos CSS para aplicar al elemento -->

        <img src="imagen.jpg" alt="Imagen de ejemplo">
        <!-- El atributo "src" especifica la ruta de la imagen a mostrar -->
        <!-- El atributo "alt" proporciona un texto alternativo para la imagen -->

        <a href="https://www.ejemplo.com" target="_blank">Enlace a Ejemplo</a>
        <!-- El atributo "href" define la URL a la que se enlaza -->
        <!-- El atributo "target" indica cómo se abre el enlace (en este caso, en una nueva pestaña o ventana) -->

        <input type="text" id="nombre" name="nombre" placeholder="Ingrese su nombre">
        <!-- El atributo "type" especifica el tipo de entrada (en este caso, un campo de texto) -->
        <!-- El atributo "id" define un identificador único para el elemento -->
        <!-- El atributo "name" especifica el nombre del campo de entrada -->
        <!-- El atributo "placeholder" muestra un texto de ejemplo dentro del campo de entrada -->

        <button type="submit" disabled>Enviar</button>
        <!-- El atributo "type" define el tipo de botón (en este caso, un botón de envío de formulario) -->
        <!-- El atributo "disabled" desactiva el botón, lo que impide que sea interactivo -->

3 - Contenido de texto: Es el texto que se encuentra dentro de las etiquetas y proporciona información o el contenido visible en el documento.

      <h1>Esto es un título principal</h1>
      <p>Este es un párrafo de ejemplo que contiene texto de relleno.</p>

      <a href="https://www.ejemplo.com">Enlace a Ejemplo</a>

      <button>Click aquí</button>

      <span>Este es un texto dentro de un elemento span</span>
      

Estos son algunos de los elementos dentro de una escructura HTML o XML, los cuales son suficiente para entenderlo. Algo muy importante dentro de la definicion del DOM que hemos mencionado anteriormente, es que dicha estructura se representa como un arbol de nodos, teniendo diferenciado los distintos elementos el arbol de nodos quedaria de la siguiente manera:

 
          Document Node
      |
      +-- Element Node (Etiqueta: <html>)
      |    |
      |    +-- Element Node (Etiqueta: <head>)
      |    |    |
      |    |    +-- Element Node (Etiqueta: <title>)
      |    |         |
      |    |         +-- Text Node (Texto: Ejemplo de árbol de nodos)
      |    |
      |    +-- Element Node (Etiqueta: <body>)
      |         |
      |         +-- Element Node (Etiqueta: <h1>)
      |         |    |
      |         |    +-- Text Node (Texto: Título principal)
      |         |
      |         +-- Element Node (Etiqueta: <p>)
      |         |    |
      |         |    +-- Text Node (Texto: Este es un párrafo de ejemplo)
      |         |
      |         +-- Element Node (Etiqueta: <a>)
      |         |    |
      |         |    +-- Attribute Node (Atributo: href)
      |         |    |
      |         |    +-- Text Node (Texto: Enlace a Ejemplo)
      |         |
      |         +-- Text Node (Texto: Texto adicional)
      |
      +-- Text Node (Texto: Espacio en blanco)


# Manipulacion del DOM con JavaScript

La manipulación del DOM (Document Object Model) con JavaScript ofrece métodos y propiedades específicas que permiten a los desarrolladores acceder, modificar y manipular los elementos del DOM de una página web. La manipulación del DOM con JavaScript es una parte fundamental del desarrollo web interactivo y dinámico. 

# Cuales son los metodos y propiedades de JavaScript que permiten manipular el DOM?


     Métodos para seleccionar elementos:

        getElementById(): Permite seleccionar un elemento por su atributo "id".
        getElementsByClassName(): Permite seleccionar elementos por su clase.
        getElementsByTagName(): Permite seleccionar elementos por su nombre de etiqueta.
        querySelector(): Permite seleccionar un elemento usando selectores CSS.
        querySelectorAll(): Permite seleccionar varios elementos usando selectores CSS.

    Métodos para modificar el contenido y los atributos de elementos:

        innerHTML: Permite obtener o establecer el contenido HTML de un elemento.
        textContent: Permite obtener o establecer el contenido de texto de un elemento.
        setAttribute(): Permite establecer el valor de un atributo de un elemento.
        getAttribute(): Permite obtener el valor de un atributo de un elemento.
        appendChild(): Permite agregar un nuevo nodo como hijo de un elemento.
        removeChild(): Permite eliminar un nodo hijo de un elemento.
        replaceChild(): Permite reemplazar un nodo hijo de un elemento con otro nodo.
        classList: Proporciona métodos para agregar, eliminar o verificar clases CSS en un elemento.

    Métodos para manipulación de estilos CSS:

        style: Proporciona acceso a las propiedades de estilo CSS de un elemento.
        classList: Proporciona métodos para agregar, eliminar o verificar clases CSS en un elemento.

    Métodos para trabajar con eventos:

        addEventListener(): Permite agregar un controlador de eventos a un elemento.
        removeEventListener(): Permite eliminar un controlador de eventos de un elemento.
        
    Metodos para trabajar con eventos del mouse:
    
          click: Se activa cuando se hace clic en un elemento.
          dblclick: Se activa cuando se hace doble clic en un elemento.
          mousedown: Se activa cuando se presiona un botón del mouse sobre un elemento.
          mouseup: Se activa cuando se suelta un botón del mouse sobre un elemento.
          mousemove: Se activa cuando se mueve el mouse sobre un elemento.
          mouseenter: Se activa cuando el mouse entra en un elemento.
          mouseleave: Se activa cuando el mouse sale de un elemento.
          mouseover: Se activa cuando el mouse se mueve sobre un elemento o sus elementos secundarios.
          mouseout: Se activa cuando el mouse se mueve fuera de un elemento o sus elementos secundarios.
          contextmenu: Se activa cuando se hace clic con el botón derecho del mouse sobre un elemento para abrir el menú contextual.
          
    Metodos para trabjar con eventos del teclado:
    
           keydown: Se activa cuando se presiona una tecla.
           keyup: Se activa cuando se suelta una tecla.
           keypress: Se activa cuando se mantiene presionada una tecla y se repite la acción de entrada de la tecla.
           
    Metodos para trabjar con eventos de formularios:
    
          submit: Se activa cuando se envía un formulario, ya sea mediante el botón de envío o mediante programación.
          input: Se activa cuando se realiza un cambio en un campo de entrada de texto, como <input> o <textarea>.
          change: Se activa cuando se realiza un cambio y se pierde el foco de un campo de entrada, como <input> o <select>.
          focus: Se activa cuando un campo de entrada obtiene el foco, es decir, cuando el usuario hace clic en él o se desplaza a él                 utilizando la tecla Tab.
          blur: Se activa cuando un campo de entrada pierde el foco, es decir, cuando el usuario hace clic en otro lugar o se desplaza a             otro campo.

    Propiedades para navegación y acceso a nodos relacionados:

        parentNode: Proporciona acceso al nodo padre de un elemento.
        childNodes: Proporciona acceso a una lista de nodos hijos de un elemento.
        nextSibling: Proporciona acceso al siguiente nodo hermano de un elemento.
        previousSibling: Proporciona acceso al nodo hermano anterior de un elemento.


