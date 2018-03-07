
# Componente Badge

El componente Badge es un componente que que se utiliza para dar formato a pequeños elementos como etiquetas, contadores etc...

Para convertir un elemento en un componente *badge* deberemos añadir la clase ***badge*** y al hacer esto a nivel de estilo básicamente se produce lo siguiente

* Adapta su tamaño al elemento padre.
* Le podemos dar un fondo coloreado atendiendo a la paleta de colores de BootStrap 4 ***badge-X***. Siendo X uno de los colores (*secondary, primary ....*)
* Redondea los bordes de ese elemento.

A continuación vamos a ver un ejemplo de uso. No es necesario la estructura del DOM por ser un elemento:

```html

    <h3>Cesta<span class="badge badge-info">4 productos</h3>

```

Si queremos que sean aún más redondeados podemos cambiar la clase ***badge*** por la clase ***badge-pill***.

```html

    <h3>Cesta<span class="badge-pill badge-info">4 productos</h3>

```

Si el elemento que contiene el badge es un enlace BootStrap añade por defecto estilos diferentes para los estado *hover* y *focus*.


```html

    <a ref="#">Cesta<span class="badge badge-info">4 productos</a>

```

No hay métodos asociados a este elemento.
