---
title: Marcas de Producto
subtitle: La marca del producto es el nombre o seudonimo comercial de la empresa productora del mismo.
tags: [catalogo, tema_marca_producto]
author: katlimruiz
---

La marca del producto es el nombre o seudonimo comercial de la empresa productora del mismo.

## Segun tipo de sitio
En general, el equipo del sitio es dueño de las marcas de producto y se encarga de crearlas, modificarlas y eliminarlas. De esta manera, el sitio mantiene un catalogo de marcas consistente.

En sitios **singleplace**, es el mismo equipo del sitio quien asignará estas marcas a los productos.

Sin embargo, para sitios **marketplace**, la asignacion de las marcas a los productos se espera que sea hecha por los merchants.

IMPORTANTE: Es responsabilidad del vendedor del producto de tener los permisos necesarios para la comercializacion de las marcas en su catalogo. La plataforma solo se encarga de dar el servicio de catalogo de marcas para su asignacion a los productos del vendedor.

## Definicion
Una marca tiene los siguientes campos:
- **Nombre**: Este es el nombre de la marca. Permite estos caracteres [A-z0-9Á-ú&\-@' ] y hasta maximo 50 caracteres. No puede repetirse.
- **Habilitar para busqueda**: Este campo permite marcar una marca para que pueda ser buscada o no. Este campo NO significa que si esta desactivado, todos los productos relacionados se oculten de la busqueda. Esto se utiliza solamente cuando la interface de usuario del sitio ha habilitado la busqueda de nombres de marca en su barra de busqueda (este es uno de sus tipicos usos).
- **Alias**: Una marca se le puede asignar un maximo de cinco alias que en el uso cotidiano son sinonimos de la marca. Por ejemplo: Coca Cola y Coke o HP y Hewlett-Packard. No pueden repetirse ni dentro de la misma marca, ni a traves de todas las marcas registradas. Un alias no puede ser tampoco igual al nombre de la marca. Un alias puede tener estos caracteres [A-z0-9Á-ú&\-@' ].

## Asignacion a productos
La marca se asigna al producto en el momento de la creacion del producto. Una vez que el producto es creado, la marca ya no se puede cambiar.

## Crear marca
En SiteCentral, para crear una marca se debe utilizar el boton `Crear Marca` y se debe asignar el nombre de la nueva marca.

Cuando la marca se crea, los siguientes campos son automaticamente asignados:
- Habilitar para busqueda: no

Si se desea que estos campos tengan otros valores, se utiliza la opcion de modificar la marca.

**Roles permitidos**: `sitecatalog`, `sitesale`, `sitecms`

## Modificar marca
En SiteCentral, para modificar una marca, el primer paso es buscarla a traves del nombre. Una vez ubicada, utilizar el boton de `Modificar Marca`.

El nombre de la marca no se pueden modificar.

Los siguientes campos si se pueden modificar:
- Habilitar para busqueda
- Alias

**Roles permitidos**: `sitecatalog`, `sitesale`, `sitecms`

## Eliminar marca (aun por implementarse)
En SiteCentral, para eliminar una marca, el primer paso es buscarla a traves del nombre. Una vez ubicada, utilizar el boton de `Modificar Marca`. Dentro de esta pantalla, utilizar el boton `Eliminar Marca`.

Para poder eliminar una marca, las siguientes condiciones deben cumplirse:
- La marca no debe estar asociada a ningun producto, sin importar si esta activo o no.
- La marca debe estar deshabilitada para la busqueda.

**Roles permitidos**: `sitecatalogadmin`