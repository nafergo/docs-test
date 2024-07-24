---
title: Operaciones masivas
subtitle: Crea y actualiza múltiples campos relacionados a un productos de forma masiva.
tags: [Cargas_masivas,Operaciones_masivas]
author: Luis Zumaeta
---
### **Como Merchant:**

La plataforma permite realizar **operaciones masivas** con cargas de excel para crear y actualizar múltiples productos en un breve periodo de tiempo.

Las operaciones masivas disponibles son:

- Creación masiva de productos.
- Creación masiva completa de productos.
- Actualización masiva completa de productos.
- Actualización masiva de productos.
- Actualización masiva de imágenes.
- Actualización masiva de stocks.
- Actualización masiva de precios bases.
- Actualización masiva de precios promocionales.
- Activación y desactivación masiva de productos.
- Actualización masiva de imágenes externas de variaciones.
- Activación y desactivación masiva de variaciones.

Cada opción permite la descarga de una plantilla excel que sirve como modelo para completar la información requerida y para realizar la carga masiva.

{% include image.html img="../docs/primeros-pasos/operaciones-masivas-2.png" alt="Alt for image" caption="Operaciones masivas para merchant" %}

***Recomendaciones generales para las operaciones masivas:***

- Siempre descarga la última versión de la plantilla.
- No modifiques el nombre de las cabeceras de las columnas.
- No modifiques el nombre de las pestañas
- No agregues pestañas, ni columnas adicionales.
- Revisa el glosario de cada plantilla para respetar las reglas y condiciones de cada campo.
- Revisa este manual (Siempre actualizaremos la información).

## Descripción de campos

Los campos mayoritariamente utilizados están mencionados en la sección de producto. Para entender los campos en la plantilla de excel, es necesario revisar la documentación mencionada.

## Creación masiva de productos

La **creación masiva de productos** permite crear muchos productos o variaciones de producto desde un archivo excel. Esta plantilla solo permite la creación de productos y/o variaciones, UPC, marca, precio, categorias, información del producto y dimensiones.

Para crear productos masivamente, es necesario completar los campos obligatorios.

### Crear productos con una sola variación:

Para crear productos con una sola variación es necesario dejar en blanco el campo **variaciones** y completar todos los campos obligatorios.

### Crear productos con múltiples variaciones:

Para crear 1 producto con muchas variaciones, se deben seguir los siguientes pasos:

- Las variaciones son representadas en varias filas.
- Todas las variaciones deben utilizar el mismo nombre del producto.
- Todas las variaciones deben tener la misma marca.
- Todas las variaciones deben tener el mismo código de categoría.
- Todas las variaciones deben tener diferentes SKU's.
- El campo variaciones debe contener y respetar los valores: Color, Capacidad, Talla y Estilo.

Ejemplo:

El producto sería `Pantalon XYZ` y las variaciones serían:

- `Pantalon XYZ Color Rojo Talla S`
- `Pantalon XYZ Color Rojo Talla M`
- `Pantalon XYZ Color Rojo Talla L`
- `Pantalon XYZ Color Azul Talla S`
- `Pantalon XYZ Color Azul Talla M`
- `Pantalon XYZ Color Azul Talla L`

## Creación masiva completa de productos

La **creación masiva completa de productos** permite crear muchos productos o variaciones de producto de manera mas completa desde un archivo excel. Esta plantilla permite la creación de productos y/o variaciones, marca, precio, categorias, información del producto, dimensiones del producto, UPC, boost de la tienda, imágenes de productos y/o variaciones, permisos del producto, precio promocional, stock y almacén.

Para crear productos masivamente, es necesario completar los campos obligatorios.

### Crear productos con una sola variación:

Para crear productos con una sola variación es necesario dejar en blanco el campo **variaciones** y completar todos los campos obligatorios.

### Crear productos con múltiples variaciones:

Para crear 1 producto con muchas variaciones, se deben seguir los siguientes pasos:

- Las variaciones son representadas en varias filas.
- Todas las variaciones deben utilizar el mismo nombre del producto.
- Todas las variaciones deben tener la misma marca.
- Todas las variaciones deben tener el mismo código de categoría.
- Todas las variaciones deben tener diferentes SKU's.
- El campo variaciones debe contener y respetar los valores: Color, Capacidad, Talla y Estilo.

## Actualización masiva de productos

La **actualización masiva de productos** permite actualizar múltiples productos desde un archivo excel. Esta plantilla utiliza principalmente el campo **ProductId** para realizar la actualización.

La **actualización** puede ser utilizada de manera parcial. Esto significa que solo las celdas que se ingrese información serán actualizadas.

Por ejemplo:

`Si el campo "Nombre del producto" se ingresa un nuevo valor y el campo "Descripción del producto" se encuentra vacío`
`Entonces solo se actualizará el campo "Nombre el producto"`

## Actualización masiva completa de productos

La **actualización masiva de productos** permite actualizar múltiples productos desde un archivo excel de manera mas completa, podrás actualizar las imagenes del producto y sus variaciones, precio base y promocionales, información del producto, permisos del producto, especificaciones, almacén y stock. Esta plantilla utiliza principalmente el campo **ProductId** para realizar la actualización.

## Actualización masiva de imágenes

La **Actualización masiva de imágenes** permite actualizar imágenes de productos y/o variaciones en un formato Zip de manera masiva. A continuación seguir las recomendaciones de como colocar los nombres de cada imagen:

- El nombre de la imagen puede contener el ProductID. Ejm: d28ab390699d11ecbd679b538e2fb9be
- Como tambien el ProductID y luego el SKU de la variación separados por un guión bajo. Ejm: d28ab390699d11ecbd679b538e2fb9be_SKU123
- En caso de colocar solo el ProductID la imagen subida se asociará con la imagen del producto. Por otro lado, en caso de colocar tanto el ProductID como el SKU la imagen se asociará a una variación específica.
- Verificar que los ProductIDs y los SKUs ingresados sean los mismos que están registrados en la plataforma, ya que deberá colocarse exactamente igual para la actualización de imágenes.
- Tener en cuenta que guardar el archivo con otro nombre afectará las imágenes que deseas actualizar.

## Actualización masiva de stocks

La **actualización masiva de stocks** permite actualizar el stock de varios productos de varios **almacenes** desde un archivo excel. Esta plantilla utiliza principalmente el campo **SKU** y **Código de almacén** para realizar la actualización.

***El stock a actualizar, reemplazará al stock existente***

Por ejemplo:

`Si 1 producto tiene un stock de 250 y se realiza una carga masiva con el mismo producto con stock 10`
**`El stock final será 10`**

## Actualización masiva de precios bases

La **actualización masiva de precios base** permite actualizar el precio de muchas variaciones desde un archivo excel. Esta plantilla utiliza principalmente el campo **SKU** para realizar la actualización.

La **actualización** solo realiza la actualización del precio base siempre y cuando sea **mayor** al precio especial final.

## Actualización masiva de precios promocionales

La **actualización masiva de precios promocionales** permite actualizar el precio promocional de muchas variaciones desde un archivo excel y como requisito colocar la fecha de inicio promocional y la fecha de expiración del precio promocional. Esta plantilla utiliza principalmente el campo **SKU** y **precio base** para realizar la actualización.

La **actualización** solo realiza la actualización del precio promocional siempre y cuando sea **menor** al precio base.

## Activación y desactivación masiva de productos.

La **activación y desactivación masiva de productos** permite actualizar la visualización, búsqueda y venta de varios productos desde un archivo excel. Esta plantilla utiliza principalmente el campo **ProductId** para realizar la actualización.

La **actualización** puede ser utilizada de manera parcial. Esto significa que solo las celdas que se ingrese información serán actualizadas; sin embargo, la `Habilitación de la búsqueda` está condicionada a la `habilitación de la visualización`.

Por ejemplo:

`Si el campo "Habilitar venta" se ingresa un nuevo valor y el campo "Habilitar búsqueda" se encuentra vacío`
`Entonces solo se actualizará el campo "Habilitar venta"`

## Actualización masiva de imagenes externas de variaciones

La **actualización masiva de imagenes externas de variaciones** permite actualizar la imagen de la variación y la acción de poder agregar o reemplazar. Esta plantilla utiliza principalmente el campo **SKU** para realizar la actualización.

## Actualización y desactivación masiva de variaciones

La **actualización y desactivación masiva de variacioness** permite actualizar las variaciones para  habilitar para la venta. Esta plantilla utiliza principalmente el campo **SKU** para realizar la actualización.
