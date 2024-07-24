---
title: Producto
subtitle: Un producto es un bien, sea fisico o virtual, que esta disponible para su venta.
tags: [catalogo, producto]
author: katlimruiz
---

Un producto es un bien, sea fisico o virtual, que esta disponible para su venta. Si el producto tiene varias opciones como color o talla se subdivide en **variaciones** (o tambien se le puede llamar variante).

Es la unidad de informacion base para muchas de las funciones dentro de la plataforma.

## Segun el tipo de sitio
Si el tipo del site es `singleplace`, el equipo del sitio es el encargado de crear, modificar y eliminar los productos y de en general mantener el catalogo actualizado y limpio.

Todos los productos siempre estan asociados a un merchant y a una tienda. En el caso del `singleplace`, este concepto aun sigue existiendo con un solo merchant y una sola tienda administrados por el mismo equipo del sitio.

Si el tipo del site es `marketplace`, se espera que el merchant se encargue de su propio catalogo con el apoyo del equipo del sitio (que esta a cargo de las marcas y las categorias).

## Cual es la diferencia entre Producto y Variación?
A nivel de informacion, un producto contiene minimo una variacion y dependiendo si presenta varias opciones, puede contener muchas variaciones.

El **producto** representa el concepto o la unidad de informacion. Contiene la informacion general del bien.

En cambio, una **variacion** es la existencia del producto dentro de un almacen. Es la representacion real del producto. Por ello, es que la variacion se le asigna un **SKU** y un **precio**.

Por ejemplo, el producto seria `Pantalon Denim` que tiene unas medidas de 50x100x5 y tiene una marca llamada Tony. Una de las  variaciones serian `Talla L, Color Azul`, `Talla S, Color Azul` y `Talla M, Color Verde`.

## Definicion de Producto
Un producto contiene estos campos:
- **Id**: Identificador unico autogenerado por la plataforma
- **Nombre**: Nombre de producto. Puede contener maximo 100 caracteres y dentro de este rango [A-zÁ-ú0-9\-/+*&%@#,'°" $().].
- **Descripcion**: Descripcion corta del producto en texto plano. Opcional. Maximo 100 caracteres.
- **Contenido**: Texto enriquecido de la presentacion completa del producto. Opcional. Maximo 10,000 caracteres.
- **SeoUrl**: Identificador publico del producto y que se usa para asignarlo en el url del sitio web.
- **Tienda**: La tienda que contiene el producto.
- **Marca**: La marca del producto. La marca solo se asigna en la creacion del producto.
- **Atributos de Variación**: Lista de atributos asignados al producto para determinar las llaves de las variaciones contenidas. Ver seccion separada para mas detalle.
- **Boost del Sitio**: El boost permite impulsar un producto dentro de la busqueda para que aparezca primero o segundo, o etc, solo cuando la busqueda no tiene un ordenamiento fijo (por lo general aparece como Recomendados). El boost por defecto es 0. A un boost mayor, el producto estara mas priorizado dentro de la busqueda.
- **Habilitar Busqueda**: Cuando esta prendido, el producto es incluido en las busquedas. El producto es creado con este campo como apagado. Esto puede servir para ir llenando el producto poco a poco y que no hayan compras del producto. Ver seccion separada.
- **Habilitar Visualizacion**: Cuando esta prendido, el producto se puede visualizar en la pagina de producto. El producto es creado con este campo como apagado. Esto puede servir para ir llenando el producto poco a poco y que no hayan compras del producto. Ver seccion separada.
- **Habilitar Venta**: Cuando esta prendido, el producto se puede agregar al carrito de compras. El producto es creado con este campo como apagado. Esto puede servir para desactivar la venta del producto en base a alguna circunstancia propia de la tienda (algun dia que no se puede laborar, etc). Ver seccion separada.
- **Alto del Producto**: Alto del producto en centimetros. Minimo 0.1cm, maximo 2000cm.
- **Ancho del Producto**: Ancho del producto en centimetros. Minimo 0.1cm, maximo 2000cm.
- **Largo del Producto**: Largo del producto en centimetros. Minimo 0.1cm, maximo 2000cm.
- **Peso del Producto**: Peso del producto en kilogramos. Minimo 0.01kg, maximo 2000kg.
- **Alto del Paquete**: Alto del producto empaquetado en centimetros. Minimo 0.1cm, maximo 2000cm.
- **Ancho del Paquete**: Ancho del producto empaquetado en centimetros. Minimo 0.1cm, maximo 2000cm.
- **Largo del Paquete**: Largo del producto empaquetado en centimetros. Minimo 0.1cm, maximo 2000cm.
- **Peso del Paquete**: Peso del producto empaquetado en kilogramos. Minimo 0.01kg, maximo 2000kg.
- **Meta Keywords**: Lista de palabras clave que permite buscar el producto dentro del sitio web.
(Responsabilidad del frontend) Estos keywords tambien deben aparecer en la pagina de producto como parte de un tag <meta> para que las busquedas en buscadores como Google tambien puedan utilizarlas.
- **Meta Description**: (Responsabilidad del frontend) Texto corto que se debe incrustar en la pagina de producto como un tag <meta> para que aparezca como la descripcion de la pagina de producto en los resultados de buscadores externos como Google.
- **Id externo de producto**: Cuando los productos son creados o actualizados por una integracion con una plataforma externa, este es el identificador del producto en esa plataforma y nos permite mantener una trazabilidad entre ambas.
- **Especificaciones**: Lista de textos cortos que usualmente aparecen como un resumen del producto en viñetas en la pagina de producto.
- **Atributos de Producto**: **NO CONFUNDIR CON ATRIBUTOS DE VARIACION** Lista de atributos o caracteristicas del producto que permiten al usuario conocer el producto mas a detalle tecnico (en formato llave:valor). Por ejemplo, material:algodon. Estos atributos son solo informativos y no participan como filtro en las busquedas de los productos.
- **Categorias**: Lista de categorias asignadas al producto. Ver seccion separada.
- **Imagenes de Producto**: A nivel de producto es posible agregar imagenes. Estas imagenes son usadas como imagenes principales o representativas del producto como un todo. Para poder publicar el producto, al menos una imagen de producto debe estar registrada. Se puede agregar solo hasta 6 imagenes a nivel de producto. Ver seccion separada.

### Atributos de Variación
La plataforma permite escoger entre cuatro atributos posibles: Color, Estilo, Talla y Capacidad. Y solo puede escoger tres de ellos por producto.

Entonces, al crear un producto, el usuario debe primero determinar si el producto tendra variaciones o no.

Si escoge que no tiene variaciones, la plataforma no asigna ningun atributo al producto, y se crea una sola variacion por defecto (dado que es necesario si o si que tenga al menos un SKU asociado).

Un ejemplo de un producto sin atributos de variacion seria una 'Silla de Comedor' donde no hay variaciones posibles dado que se vende un solo modelo. Otro ejemplo, podria ser un 'Teclado de Computadora' del que no hay variaciones posibles.

Si escoge que sí tiene variaciones, entonces debe escoger tres de los cuatro posibles atributos y se pasa a crear el producto.

Una vez creado el producto con los atributos, se pasa a crear una nueva variacion que debe asignarsele un valor por cada atributo seleccionado.

Por ejemplo, si el producto es `Pantalon Denim` y se le crea con dos atributos (Color y Talla), entonces al crear la variacion, el usuario debe asignar un valor a cada uno de los atributos de manera mandatoria (XS y Verde, o S y Azul).

Otro ejemplo, si el producto es `Celular` y se crea con los atributos Color y Capacidad, al crear la variacion se puede asignar Negro y 32GB, o Blanco y 16GB.

Por ultimo, los atributos de variacion si se convierten en filtros dentro de los resultados de busqueda de productos.

### Diferencia entre dimensiones de producto y de paquete
En muchos casos, las dimensiones del producto son las mismas que del paquete. Por ejemplo, una botella de agua.

En otros casos, esto no es igual.

Por ejemplo, una prenda de vestir tiene unas medidas cuando esta extendido y vestido, pero se puede lograr un paquete mas pequeño al estar doblado.

Otro ejemplo, un celular que sus medidas propias son distintas a comparacion de la caja que lo contiene (que puede contener un cargador, un cable de datos, el manual de uso, etc.).

Y por ultimo, una balsa inflable tiene un tamaño distinto cuando esta empaquetado que cuando esta inflado y extendido.

### Categorizacion del producto
Un producto se le puede asignar varias categorias y asi clasificarlo ordenadamente dentro del catalogo de productos.

Como vimos en la seccion de categorias, existen uno o varios arboles de categoria y al producto *tipicamente* se le asigna una categoria hoja de uno o varios arboles (se le puede asignar una categoria de cualquier nivel).

Si por ejemplo, tenemos estos dos arboles de categorias:

```
Videojuegos
|--Consolas
|----Xbox
|------Accesorios
|------Juegos
|----PlayStation
|------Accesorios
|------Juegos

Festividades
|--Dia del Padre
|----Papa Gamer
|----Papa Lector
|--Dia de la Madre
```

Al producto 'Juego FF20' se le puede asignar dos categorias: `Videojuegos/Consolas/Xbox/Juegos` y `Festividades/Dia del Padre/Papa Gamer`.

Y aqui vienen algunas restricciones.

Si el producto ya tiene estas dos categorias, no se le puede asignar ninguna otra de esas categorias dentro de esas ramas: `Videojuegos` o `Consolas` o `Xbox` o `Festividades` o `Dia del Padre`. Es decir si una categoria esta asignada al producto, entonces ningun padre de esas categorias se puede agregar.

De la misma manera, si en el caso hipotetico el producto se le asigna la categoria `Consolas`, ya no se le podria asignar `Xbox` dado que es una categoria hija dentro de esa rama.

Todo esto es con el fin de que la categorizacion de productos se haga de manera limpia, sin duplicados y sin errores, y ademas promoviendo el uso de categorias hoja lo mas posible.

### Imagenes de Producto
Un producto puede tener dos niveles de imagenes. El primero es a nivel de producto donde las imagenes son consideradas como representativas de todo el producto (aun cuando las variaciones pueden tener imagenes).

Las imagenes a nivel de variacion son para mostrar como se ve esa variacion exactamente, y permiten, por ejemplo, ser usadas como selector de la variacion en la pagina de producto.

Las imagenes (de los dos niveles) tienen las siguientes restricciones/consideraciones:
- Las imagenes deben tener forma cuadrada (ancho y alto igual).
- Las imagenes deben considerar un fondo blanco (recomendado).
- Las imagenes no pueden pesar mas de 1 megabyte.
- Las imagenes deben tener minimo ancho 1000 pixels y minimo alto 1000 pixels.

Cuando las imagenes son agregadas, el sistema automaticamente generará distintos tamaños de la misma imagen para que el sitio web lo pueda utilizar adecuadamente. Por cada imagen se guardara:
- la imagen original
- conversion en tamano grande en 1000x1000px
- conversion en tamano mediana en 500x500px
- conversion en tamano pequeña en 166x166px

Este proceso se ejecuta automaticamente en segundo plano pero puede demorar unos segundos en ejecutarse.

## Definicion de Variación
Una variacion, como ya se dijo, es la existencia del producto en un almacen y lo que finalmente es vendido y entregado al comprador.

Los campos de una variacion son:
- **SKU**: SKU significa en ingles "stock keeping unit" que representa un codigo unico interno por la tienda que contiene el producto. El SKU solo permite estos caracteres [A-Z0-9\-./]. Requerido.
- **UPC**: UPC significa en ingles "Universal Product Code" y es una numeracion universal del producto. Opcional.
- **Nombre de Variación**: El nombre de variacion es automaticamente calculado en base al nombre del producto y los valores de los atributos de la variacion. Si por ejemplo, el producto se llama `Pantalon Denim`, y la variacion tiene `Color:Azul` y `Talla:XS`, el nombre de la variacion seria `Pantalon Denim Azul/XS`. Si tuviera tres atributos, se enumerarian al final separados con un `slash /`.
- **Habilitar la Venta**: Al estar activado, habilita la venta de esta variacion. Desactivar la variacion puede servir mucho para salvaguardar situaciones excepcionales que necesitan detener una venta de la variacion (esto evita el agregado al carrito de compras).
- **Imagenes de Variación**: Las imagenes de variacion sirven para poder mostrar como es la variacion exactamente. Por ejemplo, si un pantalon es vendido en azul y Verde, las imagenes de la variacion deberian mostrar el producto en version azul. Y asi tambien la verde. Se puede agregar solo hasta 6 imagenes por variacion.
- **Precio Base**: Es el precio original de la variacion. Si la variacion tiene asignado el precio urgente, tipicamente este precio es mostrado tachado.
- **Precio Urgente**: Es el precio actual de la variacion y es el que el comprador pagaria.
- **Atributos de Variación**: Son los valores de los atributos de variacion que clasifican las variaciones. La combinacion de todos los valores debe ser unica dentro del producto.

## Publicación de Producto y Variación
Como ya se vio anteriormente, el producto tiene tres atributos que permiten "publicar" el producto en distintas secciones del sitio:
- Habilitar Busqueda
- Habilitar Visualizacion
- Habilitar Venta

Cada uno tiene diferentes condiciones para poder ser habilitado.

Para habilitar la visualizacion, el producto debe:
- Tener una imagen al menos
- Tener una variacion al menos
- Todas las variaciones deben tener un precio base mayor a cero

Para habilitar la busqueda, el producto debe:
- Tener categorias
- Estar marcado para ser visualizado.

Para habilitar la venta, el producto debe:
- Tener una imagen al menos
- Tener una variacion al menos

A nivel de variacion se tiene un solo atributo:
- Habilitar Venta

Para habilitar la venta, la variacion debe:
- Tener el precio base mayor a cero.