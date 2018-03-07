
# Componente Alert

El componente Alert nos va a servir para mostrar mensaje destacados que queremos que el usuario vea. 

Tiene, de manera general, la siguiente estructura (no se representa el DOM por ser de un único elemento):


```html

  <div class="alert alert-x">

    Some content

  </div>

```

Siendo ***alert-X*** la clase BootStrap para definir la gama de colores de nuestro mensaje, tanto para el fondo como para el texto que contenga la alerta. Esta gama de colores ya ha sido explicada en anteriores capítulos.


Al añadir colores tanto al texto como al fondo nos podemos encontrar con que los colores de los enlaces pasan desapercibidos, por ello, si queremos añadir un enlace que destaque de manera correcta dentro de una alerta debemos añadirle la clase ***alert-link***. Como ejemplo:

```html

<div class="alert alert-x">

  Some content with <a href="#" class="alert-link"> a link</a>.

</div>

```
Adicionalmente, si quiero que la alerta desaparezca tengo que:

* Añadir la clase ***alert-dismissible*** al elmento que tenía la clase *alert*. Esto además me servirá para posicionar el elemento que, al hacer click en él, hará que desaparezca la alerta.
* Añadir al elemento de cierre el atributo ***data-dismiss="alert"*** para asociar correctamente la acción javascript. La documentación recomienda que esto sea una etiqueta ***button***
* Y para animar los elementos al desaparecer podremos añadir las clases ***fade*** y ***show*** al elemento principal.


Un ejemplo sería:

```html

  <div class="alert alert-warning alert-dismissible fade show" role="alert">
    Texto de la alerta
    <button type="button" class="close" data-dismiss="alert" aria-label="Close">
      <span aria-hidden="true">X</span>
    </button>
  </div>  

```

Puedo además interaccionar con estos elementos alert mediante el uso de una serie de métodos:

* $().alert(). Enlaza manejadores de click con los elementos hijo que tengan ***data-dismiss="alert"*** para que al ahcer click sobre ellos desaparezcan los elementos seleccionados.
* $().alert('close'). Cierra las alertas y las elimina del DOM.
* $().alert('dispose'). XXXXXXX

Y los eventos asociados son:

* ***close.bs.alert*** que se dispara al cerrar la alerta.
* ***closed.bs.alert*** que se dispara cuando la alerta se está cerrando del todo.
