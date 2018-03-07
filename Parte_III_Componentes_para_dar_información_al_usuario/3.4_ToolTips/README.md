# Componente Tooltip

El componente BootStrap 4 *tooltip* es un componente muy similar al componente *popover* pero difiere de este en que el llamado *bocadillo* no aparece al hacer click en el elemento si no al mover el ratón por encima de éste.

Para que funcionen requieren que hayamos añadido la librería popper.js a nuestro proyecto.

Un ejemplo básico de utilización podría ser el siguiente. No es necesario mostrar la estructura del DOM ya que sólo es un elemento:

```html

  <div class="btn btn-danger mt-5"
       data-toggle="popover"
       title="Título del bocadillo">
       Muestra el bocadillo
  </div>

```
Debemos fijarnos en los atributos que hemos añadido al elemento:

* ***data-toggle:*** Atributo BootStrap que indica que el elemento tiene una interacción como tooltip.
* ***title:*** Texto del tooltip o pista.

Si queremos añadir HTML dentro del atributo *title* debemos añadir al componente ***data-html="true"***.

Con BootStrap 4 podemos elegir entre 4 posibles posiciones en las que puede aparecer el componente *tooltip*:

* Arriba o ***top***
* Abajo o ***bottom***
* A la derecha o ***right***
* A la izquiera o ***left***

Para especificar esta posición deberemos añadir el atributo el atributo ***data-placement*** con alguno de los valores anteriormente mencionados.

**IMPORTANTE:** Para que todo funcione correctamente debemos añadir el siguiente script (o alguno similar) a nuestra página:

```html

  <script>

    $(function () {
      $('[data-toggle="tooltip"]').tooltip()
    });

  </script>

```

## Funciones asociadas

Las más importantes son, bajo mi punto de vista:

* ***.tooltip(options)*** Habilita los tooltips. Para más información sobre las posibles opciones visitar el manual.
* ***.tooltip('show')*** Muestra el bocadillo asociado a un elemento.
* ***.tooltip('hide')*** Oculta el bocadillo asociado a un elemento.
* ***.tooltip('toogle')*** Cambio el estado de visibilidad del bocadillo asociado a un elemento.
* ***.tooltip('dispose')*** El popover deja de funcionar.
* ***.tooltip('enable')*** Habilita el bocadillo asociado a un elemento
* ***.tooltip('disable')*** Deshabilita el bocadillo asociado a un elemento.

## Eventos asociados

La interacción con este tipo de elementos genera 5 nuevos tipos de eventos, bastante auto explicativos por su nombre y de los cuáles, para saber más detalles deberemos visitar el manual de referencia.

* ***show.bs.tooltip***
* ***shown.bs.tooltip***
* ***hide.bs.tooltip***
* ***hidden.bs.tooltip***
* ***inserted.bs.tooltip***
