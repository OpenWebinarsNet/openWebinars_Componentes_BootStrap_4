# Componente ScrollSpy

El componente BootStrap 4 ***ScroolSpy*** nos va a permtir actualizar el elemento activo de componentes como un ***ListGroup***,***Nav*** o ***NavBar*** de tal manera que conforme vamos haciendo scroll sobre los contenidos se destacará el elemento sobre el que estamos.

Para conseguir tenemos que seguir los siguiente pasos:

* Añadir a los distintos elementos que conforman el elemento de navegación un atributo ***data-target="#SeccionID"*** o ***href="#SeccionID*** en caso de que estos elementos sean enlaces. Además ponerle a ese elemento un ID.
* Meter los distintos contenidos sobre los que queremos hacer *scroll* dentro de un elemento que contenga el atributo ***data-spy="scroll"*** y ***data-target="#ID"** del componente de navegación. Además debemos dar a ese elemento un altura determinada y darle ***overflow:auto*** para que aparezca el scroll.
* Añadir a los contenidos de la zona de *scroll* los mismos IDs que habíamos referenciado en al punto 1.
* Podemos fijar la distancia con respecto al inicio de un elemento con ***data-offet=X***. La distancia se mide en pixel.


Podemos verlo en un ejemplo con una ***ListGroup***

```html

    <ul class="list-group" id="navegacion">
        <li class="list-group-item" data-target="#s1">Sección 1</li>
        <li class="list-group-item" data-target="#s1">Sección 2</li>
        <li class="list-group-item" data-target="#s1">Sección 3</li>
        <li class="list-group-item" data-target="#s1">Sección 4</li>
    </ul>

    <div data-spy="scroll" data-target="#navegacion" data-offset="0" class="ejemploscroll">
            <h1 id="s1">Sección 1</h1>
            <p>LoremOccaecat mollit enim non ullamco sunt exercitation et sit labore. Cillum elit magna voluptate sunt deserunt est irure. Nostrud commodo exercitation dolore enim voluptate sit laborum laboris aute. Id laborum anim irure sint consectetur
                ullamco ullamco irure qui minim ea. Exercitation sint ut ex magna culpa elit duis officia ad sit. Deserunt exercitation tempor quis ut. Exercitation eu aliqua labore magna duis esse in elit ullamco qui est quis ut proident.</p>
            <h1 id="s2">Sección 2</h1>
            <p>LoremOccaecat mollit enim non ullamco sunt exercitation et sit labore. Cillum elit magna voluptate sunt deserunt est irure. Nostrud commodo exercitation dolore enim voluptate sit laborum laboris aute. Id laborum anim irure sint consectetur
                ullamco ullamco irure qui minim ea. Exercitation sint ut ex magna culpa elit duis officia ad sit. Deserunt exercitation tempor quis ut. Exercitation eu aliqua labore magna duis esse in elit ullamco qui est quis ut proident.</p>
            <h1 id="s3">Sección 3</h1>
            <p>LoremOccaecat mollit enim non ullamco sunt exercitation et sit labore. Cillum elit magna voluptate sunt deserunt est irure. Nostrud commodo exercitation dolore enim voluptate sit laborum laboris aute. Id laborum anim irure sint consectetur
                ullamco ullamco irure qui minim ea. Exercitation sint ut ex magna culpa elit duis officia ad sit. Deserunt exercitation tempor quis ut. Exercitation eu aliqua labore magna duis esse in elit ullamco qui est quis ut proident.</p>
            <h1 id="s4">Sección 4</h1>
            <p>LoremOccaecat mollit enim non ullamco sunt exercitation et sit labore. Cillum elit magna voluptate sunt deserunt est irure. Nostrud commodo exercitation dolore enim voluptate sit laborum laboris aute. Id laborum anim irure sint consectetur
                ullamco ullamco irure qui minim ea. Exercitation sint ut ex magna culpa elit duis officia ad sit. Deserunt exercitation tempor quis ut. Exercitation eu aliqua labore magna duis esse in elit ullamco qui est quis ut proident.</p>
    
    </div>
```

### Funciones asociadas

* ***.scrollspy({target: "#idnavegación"})*** Habilita el componente para ese elemento de navegación que hemos identificado mediante un ID.
* ***.scrollspy('refresh')*** Si añado/quito elementos al DOM para que siga funcionando el componente tengo que hacer recargar usando este método.
* ***.scrollspy('dispose')*** Destruye el componente ScrollSpy. Deja de funcionar.

## Eventos asociados.

La interacción con este tipo de elementos genera 1 nuevos tipo de eventos, bastante auto explicativos por su nombre. Para saber más detalles deberemos visitar el manual de referencia.

* ***activate.bs.scrollspy***