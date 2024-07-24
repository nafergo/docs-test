---
title: Categorias de Producto
subtitle: Una categoria de producto es una agrupación de productos con caracteristicas y/o beneficios similares.
tags: [catalogo, tema_categoria_producto]
author: katlimruiz
---

Una categoria de producto es una agrupación de productos con caracteristicas y/o beneficios similares. Algunos ejemplos: Moda Hombres, Zapatos, Zapatillas, Electrodomesticos, Videojuegos, etc.

Las categorias de producto pueden ser organizadas en una estructura jerarquica (llamado arbol de categorias) donde una categoria padre puede contener muchas categorias hijas.

Un ejemplo de un arbol de categorias seria:
```
Videojuegos
|--Consolas
|----Xbox
|------Accesorios
|------Juegos
|----PlayStation
|------Accesorios
|------Juegos
```
## Segun tipo de sitio
En general, el equipo del sitio es dueño de las categorias de producto y se encarga de crearlas, modificarlas y eliminarlas. De esta manera, el sitio mantiene una taxonomia consistente.

En sitios **singleplace**, es el mismo equipo del sitio quien asignará estas categorias a los productos.

Sin embargo, para sitios **marketplace**, la asignacion de las categorias a los productos se espera que sea hecha por los merchants.

En caso, el merchant desea crear una nueva categoria es potestad del equipo del sitio aceptarlo o no.

## Definicion
Una categoria tiene los siguientes campos:
- **Codigo**: Este es el codigo de categoria asignado por el equipo del sitio (ver seccion separada). Debe ser unico dentro del sitio.
- **Nombre**: Este es el nombre de la categoria. Permite estos caracteres [A-z0-9ÑñÁ-Úá-ú\-&,$% *] y hasta maximo 100 caracteres. Puede repetirse.
- **Nivel**: Este es el nivel asignado automaticamente a la categoria segun la altura en el arbol en la que esta ubicada. El nivel 0 es para las raiz del arbol. Este campo es interno, pero si es necesario mencionarlo.
- **Tiene contenido para adultos**: Este campo permite clasificar los productos relacionados como solo para adultos. En algunos paises esto se utiliza para enmascarar las imagenes o pedir una confirmacion previa de mayoria de edad para el usuario que esta viendo el sitio. Es responsabilidad de la interface de usuario del sitio utilizar este campo cuando sea necesario.
- **Habilitar para busqueda**: Este campo permite marcar una categoria para que pueda ser buscada o no. Este campo NO significa que si esta desactivado, todos los productos relacionados se oculten de la busqueda. Esto se utiliza solamente cuando la interface de usuario del sitio ha habilitado la busqueda de nombres de categoria en su barra de busqueda (este es uno de sus tipicos usos).
- **Ruta de la Categoria**: La ruta de la categoria es una cadena de texto que muestra, desde la raiz hasta la misma categoria, los nombres de las categorias separadas por un `slash /`. Por ejemplo: `Videojuegos/Consolas/Xbox/Juegos`.

### Codigo de categoria
El codigo de la categoria es asignado por el equipo del sitio cumpliendo las siguientes condiciones:
- Maximo 30 caracteres
- Solo permite caracteres alfanumericos (A-z 0-9)

La estructura y la forma del codigo de categoria es decidido por el mismo equipo del sitio en base a sus propias necesidades.

Sin embargo, sí se recomienda que los codigos de categoria tengan un formato uniforme y que connote una jerarquizacion para su facil utilizacion.

Una posible forma es asumir que si mi arbol de categorias tiene 4 niveles y tipicamente no hay mas alla de 100 categorias por nivel, entonces el codigo podria ser tener un esquema de 8 caracteres como 00112233.

Si, por ejemplo, tuvieras este arbol de categorias, estos podrian ser los codigos asignados a cada categoria.
```
Videojuegos 01
|--Consolas 0101
|----Xbox 010101
|------Accesorios 01010101
|------Juegos 01010102
|----PlayStation 010102
|------Accesorios 01010201
|------Juegos 01010202
```

Otra posible forma podria ser simplemente hacerlo autonumerico segun se vayan creando las categorias 00000001, 00000002, 00000003, ...

Pero reiteramos que es decisión del equipo del sitio seleccionar el mejor esquema que se adapte a su propia situacion.

## Estructura Jerarquica
Las categorias de productos se organizan en una estructura jerarquica llamada arbol de categorias. El arbol de categorias siempre empieza con una `categoria raiz`.

Las categorias que estan en el ultimo nivel del arbol se les dice `categoria hoja`.

A las categorias raiz se le asigna siempre el nivel 0 (cero). Cuando se agrega una `categoria hija` dentro una categoria raiz, la categoria hija se le asignara el nivel 1.

Si se agrega una categoria hija a esta ultima categoria hija (osea una categoria nieta de la raiz), se le asignara el nivel 2. Y asi hasta el nivel 3.

La plataforma solo permite hasta 4 niveles de categorias (0..3).

La plataforma permite tener varias categorias raiz, de esta manera entonces, se pueden tener varios arboles de categoria registrados.

## Asignacion a productos
Un producto puede tener varias categorias asignadas pero siempre de distintos arboles. Para mayor detalle, ver la pagina de producto (TODO: crear link a producto).

## Crear categoria
En SiteCentral, para crear una categoria raiz se debe utilizar el boton `Añadir Ruta` y se debe asignar el codigo y nombre de la nueva categoria.

Si es que deseas crear una categoria hija (sea nivel 1, 2 o 3), debes ubicar la categoria padre inmediata y utilizar el boton de `Añadir Categoria`. De igual manera que una categoria raiz, se debe asignar el codigo y nombre.

{% include alert.html style="warning" text="**IMPORTANTE**: El codigo y nombre de la categoria NO SE PUEDE CAMBIAR. Si necesitas cambiarlo, el procedimiento es crear una nueva categoria y reasignar los productos. Esto es una situacion temporal." %}

Cuando la categoria se crea, los siguientes campos son automaticamente asignados:
- Nivel: nivel del padre + 1
- Ruta: ruta del padre + / + nombre
- Habilitar para busqueda: no
- Contenido para adultos: no

Si se desea que estos campos tengan otros valores, se utiliza la opcion de modificar la categoria.

**Roles permitidos**: `sitecatalog`.

## Modificar categoria
En SiteCentral, para modificar una categoria, el primer paso es buscarla a traves del codigo o del nombre. Una vez ubicada, utilizar el boton de `Modificar Categoria`.

El codigo y el nombre no se pueden modificar.

Los siguientes campos si se pueden modificar:
- Habilitar para busqueda
- Contenido para adultos

**Roles permitidos**: `sitecatalog`.

## Eliminar categoria (aun por implementarse)
En SiteCentral, para eliminar una categoria, el primer paso es buscarla a traves del codigo o del nombre. Una vez ubicada, utilizar el boton de `Modificar Categoria`. Dentro de esta pantalla, utilizar el boton `Eliminar Categoria`.

Para poder eliminar una categoria, las siguientes condiciones deben cumplirse:
- Solo se puede eliminar categorias hoja. Si se quiere eliminar una categoria raiz o una categoria que este en los niveles intermedios, entonces se debe primero eliminar las categorias hoja y asi ir subiendo de nivel.
- La categoria no debe estar asociada a ningun producto, sin importar si esta activo o no.
- La categoria debe estar deshabilitada para la busqueda.

**Roles permitidos**: `sitecatalogadmin`.
