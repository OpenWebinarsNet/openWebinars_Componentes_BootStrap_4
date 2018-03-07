
# Componente Collapse

El componente BootStrap 4 ***Collapse*** es un componente que nos ayudará a mostrar/ocultar otros elementos con el efecto de *cortinilla* (ya sea arriba o abajo).

Tenemos por lo tanto dos elementos principales dentro de este componente:

* El elemento que muestra/oculta lo demás al hacer *click* sobre él. Este normalmente será o bien un botón o un enlace con dos atributos especiales ***data-toggle="collapse"***  y o bien ***data-target="#MyCollapseID"*** si es un botón o bien ***href="#MyCollapseID"*** si es un enlace. *#MyCollapseID* será el id del elemento que quiero ocultar/mostrar.
* El elemento que se muestra/oculta que debe de tener un id y la clase ***collapse***.


Un ejemplo sería el siguiente. No se muestra la estructura del DOM por ser sólo un componente:

```html

  <a class="btn btn-danger" data-toggle="collapse" href="#MyCollapseID">Ocultar/Mostrar</a>

  <button class="btn btn-warning" data-toggle="collapse" data-target="#MyCollapseID">Ocultar/Mostrar</button>


  <div class="collapse" id="MyCollapseID">
    Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.
  </div>

```

Si queremos que el elemento en el que vamos a hacer click oculte/muestre varias cosas a la vez tenemos que modificar el selector que hemos añadido en *href* o en *data-target* de tal manera que con ese selector estemos abarcando todos los elementos que queremos ocultar/mostrar.

Un ejemplo sería el siguiente:

```html

<button class="btn btn-primary" data-toggle="collapse" data-target=".varios">Ocultar/Mostrar</button>

<div class="collapse varios border">
  Primer elemento
</div>

<div class="collapse varios border">
  Segundo elemento
</div>

```

Como se puede apreciar el ***data-target=".varios"*** tiene un selector que está seleccionando, en este caso, dos elementos. Estos son los elementos que mostrará/ocultará cada vez.

Con este componente es muy fácil conseguir *Acordeones horizontales*.

## Funciones asociadas

Las más importantes son, bajo mi punto de vista:

* ***.collapse(options)*** Habilita un elemento como colapsable. Para más información sobre las posibles opciones visitar el manual.
* ***.collapse('show')*** Muestra los elementos seleccionados que tengan la clase *collapse*.
* ***.collapse('hide')*** Oculta los elementos seleccionados que tengan la clase *collapse*.
* ***.collapse('toogle')*** Cambio el estado de visibilidad los elementos seleccionados que tengan la clase *collapse*.
* ***.collapse('dispose')*** Destruye el elemento colapsable. Deja de funcionar.

## Eventos asociados

La interacción con este tipo de elementos genera 4 nuevos tipos de eventos, bastante auto explicativos por su nombre y de los cuáles, para saber más detalles deberemos visitar el manual de referencia.

* ***show.bs.collpase***
* ***shown.bs.collapse***
* ***hide.bs.collpase***
* ***hidden.bs.collapse***
