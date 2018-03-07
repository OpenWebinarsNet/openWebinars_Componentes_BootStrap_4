# Componente PopOver

El componente BootStrap 4 *popover* es lo que tradicionalmente hemos conocido en español como *bocadillo*.  Es un elemento que aparecerá al hacer click sobre otro y que no servirá para aportar explicaciones o aclaraciones sobre el elemento sobre el que hemos interaccionado.

Para que funcionen requieren que hayamos añadido la librería popper.js a nuestro proyecto.

Un ejemplo básico de utilización podría ser el siguiente. No es necesario mostrar el DOM por ser un único elemento:

```html

  <div class="btn btn-danger mt-5"
       data-toggle="popover"
       title="Título del bocadillo"
       data-content="Explicación o aclaración sobre el el elemento">
       Muestra el bocadillo
  </div>

```

Debemos fijarnos en los atributos que hemos añadido al elemento:

* ***data-toggle:*** Atributo BootStrap que indica que el elemento tiene una interacción como popover.
* ***title:*** Título del bocadillo
* ***data-content:*** Contenido del bocadillo.

Necesitamos, para que todo funcione de manera correcta tener *data-toggle* y al menos uno de los otros dos atributos.

**IMPORTANTE:** Para que todo funcione correctamente el estilo de otros elementos no debe interferir con el popover. Si queremos asegurarnos de que esto suceda debemos añadir el siguiente script a nuestra página:

```html

<script>
  $(function () {
    $('.clase_de_popover').popover({
      container: 'body'
    })
  })
</script>

```

Siendo ***.clase_de_popover*** el selector para escoger este tipo de elementos (lo habremos decidido nosotros) y con el parámetro ***container:'body'*** especificaremos que el bocadillo aparece en relación a dicho elemento.

Eso, o poner el atributo ***data-container='body'*** a los elementos afectados.

Con BootStrap 4 podemos elegir entre 4 posibles posiciones en las que puede aparecer el componente *popover*:

* Arriba o ***top***
* Abajo o ***bottom***
* A la derecha o ***right***
* A la izquiera o ***left***

Para especificar esta posición deberemos añadir el atributo el atributo ***data-placement*** con alguno de los valores anteriormente mencionados.

## Funciones asociadas

Las más importantes son, bajo mi punto de vista:

* ***.popover(options)*** Habilita los popovers. Para más información sobre las posibles opciones visitar el manual.
* ***.popover('show')*** Muestra el bocadillo asociado a un elemento.
* ***.popover('hide')*** Oculta el bocadillo asociado a un elemento.
* ***.popover('toogle')*** Cambio el estado de visibilidad del bocadillo asociado a un elemento.
* ***.popover('dispose')*** El popover deja de funcionar.
* ***.popover('enable')*** Habilita el bocadillo asociado a un elemento
* ***.popover('disable')*** Deshabilita el bocadillo asociado a un elemento.


## Eventos asociados

La interacción con este tipo de elementos genera 5 nuevos tipos de eventos, bastante auto explicativos por su nombre y de los cuáles, para saber más detalles deberemos visitar el manual de referencia.

* ***show.bs.popover***
* ***shown.bs.popover***
* ***hide.bs.popover***
* ***hidden.bs.popover***
* ***inserted.bs.popover***
