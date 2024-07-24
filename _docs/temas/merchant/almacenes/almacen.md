---
title: Almacenes
subtitle: El almacén es la representación virtual de una tienda o un almacén físico.
tags: [merchant,almacen]
author: Luis Zumaeta
---

La plataforma permite la creación de múltiples **almacenes** conforme sean necesarios para la distribución de diferentes productos y la atención de órdenes.

Las características principales de un **almacén** son:

- Stock de productos.
- Ubicación del almacén.
- Tiempo de preparación (Lead time).
- Horario de corte.
- Tipo de entrega (A domicilio o recojo en tienda)

Hoy en día la omnicanalidad es algo que toma mucha presencia en el mundo digital y es por ello que el **almacén** representa una tienda o almacén físico debido a que es el reflejo de lo que ocurre en la realidad. Esto significa que una tienda/local/almacén/darkstore, etc, puede recibir pedidos para ser distribuidos desde ese punto.

## Segun tipo de sitio
En sitios **singleplace**, el **Sitelogistic** está encargado de la creación y gestión del **almacén** de manera directa.

En sitios **marketplace**, el **MerchantoLogistic** está encargado de la creación y gestión del **almacén** de manera directa.

Esta distinción es debido a que en un sitio **singleplace** el almacenero es dueño del proceso de despacho mientras que en un **marketplace** el responsable del despacho es almacenero del **merchant**.

## Características del almacén

### Definición de campos generales
- **Nombre de almacén**: Es el nombre comercial que se le atribuye al almacén (Este campo no podrá ser editado posteriormente).
- **Código de almacén**: Es un código que se le asigna al almacén para identificarlo de manera interna (Este campo no podrá ser editado posteriormente).
- **ID externo de almacén**: Este campo es utilizado para realizar integraciones a nivel de stock con otros sistemas.
- **Persona encargada**: Son los datos de contacto de la persona responsable del almacén.

### Stock de productos
El stock puede ser ingresado desde el catálogo de productos o desde operaciones masivas para una actualización de varios productos.

La plataforma permite descargar un reporte general del stock de todos los productos.

***La falta de stock no bloquea la visualización del producto***

### Ubicación del almacén
El **almacén** a diferencia de la **tienda** tiene una ubicación física con la finalidad de ser el punto de recojo de productos. Esta característica permite que los productos puedan ser distribuidos desde diferentes ubicaciones.

La ubicación puede ser editada posteriormente en caso la ubicación haya sido ingresada erróneamente.

La ubicación del almacén se geolocaliza con la finalidad de obtener mayor precición. Se puede agregar refrencias como campo opcional.

### Tiempo de preparación
Es el tiempo que un almacén suele demorar en preparar productos en general.

### Horario de corte
Es la hora en la cuál el **almacén** cierra su proceso de recepción de pedidos para no afectar su compromiso de entrega. Esto no significa que se detengan la generación de pedidos, sino que los pedidos aumentan un día adicional para su entrega. Por ejemplo:

Si un almacén puede atender todos los pedidos que ingresen hasta las 17:00 para dejarlos listos en 24 horas, significa que los pedidos que ingresen a las 17:05 serán considerados para el siguiente turno de atención. Con ello evitando prometer fechas de entrega que no podrán cumplir.

### Tipo de entrega

#### A domicilio
Es la opción de habilitar la entrega mediante un transportista que puede ser proporcionado por el Siteowner o por flota propia (**marketplace**).

#### Recojo en tienda
Es la opción de habilitar el recojo en la tienda de manera presencial.


## Crear almacén
Para crear un almacen debemos ir a la seccion de **Almacenes** y dando click en  "Crear almacen".
{% include image.html img="../docs/temas/merchant/almacenes/crear-almacen-1.png" alt="Alt for image" caption="prueba" %}

Luego ingresaremos toda la informacion del almacen como *Nombre*, *Codigo*, *ID externo*, *Contacto del almacenero* y *Ubicación del almacen*.
{% include image.html img="../docs/temas/merchant/almacenes/crear-almacen-2.png" alt="Alt for image" caption="prueba" %}

## Editar almacén
Para editar un almacén debemos dar click al siguiente boton.
{% include image.html img="../docs/temas/merchant/almacenes/editar-almacen-1.png" alt="Alt for image" caption="prueba" %}

Nos dirigira al apartdo de *Informacion* donde se mostrara la informacion actual del almacen para poder editarla.
{% include image.html img="../docs/temas/merchant/almacenes/editar-almacen-2.png" alt="Alt for image" caption="prueba" %}

Tambien un poco mas abajo encontraremos un boton de *"Configurar dias de no despacho o festivos"*, donde se podra escoger los dias en los cuales el almacen no hara despachos.
{% include image.html img="../docs/temas/merchant/almacenes/editar-almacen-3.png" alt="Alt for image" caption="prueba" %}
Podremos escoger los dias de no despacho dandole click a los dias.
{% include image.html img="../docs/temas/merchant/almacenes/editar-almacen-4.png" alt="Alt for image" caption="prueba" %}

Luego se vamos al apartado de *Metodos de entrega* donde se podra hacer configuraciones tanto para la "Entrega a domicilio" asi como para "Retiro en tienda".

Esta seria la configuracion para el metodo "Entrega a domicilio".
{% include image.html img="../docs/temas/merchant/almacenes/editar-almacen-5.png" alt="Alt for image" caption="prueba" %}
Esta seria la configuracion para el metodo "Retiro en tienda".
{% include image.html img="../docs/temas/merchant/almacenes/editar-almacen-6.png" alt="Alt for image" caption="prueba" %}

## Buscar almacén
Para poder buscar un almacen lo podemos hacer por su *Nombre y/o Codigo*.
{% include image.html img="../docs/temas/merchant/almacenes/buscar-almacen.png" alt="Alt for image" caption="prueba" %}

## Stock del almacén
Para poder ver el stock de los productos que tiene el almacen, damos click al siguiente boton.
{% include image.html img="../docs/temas/merchant/almacenes/stock-1.png" alt="Alt for image" caption="prueba" %}
Nos mostrara el SKU de los productos con su respectivo stock ademas de poder filtrarlos por si tiene variaciones o no y tambien un boton "Iniciar descarga" para descargar todo el stock del almacen en formato excel.
{% include image.html img="../docs/temas/merchant/almacenes/stock-2.png" alt="Alt for image" caption="prueba" %}




