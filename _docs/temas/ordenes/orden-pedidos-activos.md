---
title: Pedidos activos
subtitle: Pedidos que aún se encuentran en gestión.
tags: [Pedidos activos]
author: Luis Zumaeta
---

Los pedidos activos son todos aquellos que aún se encuentran en proceso de gestión. Principalmente abarcan los estados `pendiente de pago` ,`confirmado`, `listo para despacho`, `en tránsito`, `últimos entregados` y `retenidos`.

Todos los pedidos se muestran en grillas y pueden ser filtrados por estados mediante las pestañas. Al hacer clic en el número del pedido, se podrá ingresar a la sección de mayor detalle del pedido.

## Pedidos activos
Ingresando a la sección **Pedidos activos** podrás encontrar los pedidos que tengan los estados *Pendiente de Pago*, *Confirmado*, *Listo para despacho*, *En tránsito*, *Últimos Entregados* y *Retenidos*, para esto solo deberás hacer click en la pestaña correspondiente.

{% include image.html img="../docs/primeros-pasos/pedidos-activos-1.jpg" alt="Alt for image" caption="Pedidos Activos" %}

También podrás visualizar algunas opciones como **Iniciar descarga**, la cual permite obtener un archivo Excel con todos los registros necesarios de los pedidos y también existe otra opción de **Filtros**, en donde se puede filtrar estos pedidos por: 
 * **Filtro por fecha de creación dado un rango de fechas:** Para obtener todos los pedidos que han sido creados dentro de un rango específico de fechas.
 * **Filtro por fecha máxima de envío dado un rango de fechas:** Para obtener todos los pedidos que han sido o serán entregados dentro de un rango específico de fechas.
 * **Filtro por transportista:** Para obtener todos los pedidos que han sido o serán entregados por un transportista en particular.
 * **Filtro por método de pago:** Para obtener todos los pedidos que han sido pagados con un método de pago correspondiente.
 * **Filtro por un código identificador de un usuario:** Para obtener todos los pedidos que han sido efectuados por un usuario en particular.
 * **Filtro por un correo electrónico:** Para obtener todos los pedidos que estan relacionados en un correo.
 * **Filtro por una tienda:** Para obtener todos los pedidos que estan relacionados a una tienda.
 * **Filtro por un almacén:** Para obtener todos los pedidos que estan relacionados a un almacén.

{% include image.html img="../docs/primeros-pasos/pedidos-activos-filtros-1.jpg" alt="Alt for image" caption="Filtros de Pedidos Activos" %}

## Pedido pendiente de pago
Los pedidos con estado `pendiente de pago` reflejan aquellos pedidos que aun no pasan el filtro o proceso de cobro. Este estado es previo a `confirmado`. Cuando se cambio el estado de `pendiente de pago` a `confirmado` implica **que el pedido ha sido pasado por el proceso de cobro**.

### Edición

Mientras el pedido se encuentre en `pendiente de pago` no se permite modificar ningún campo dentro del pedido.  

## Pedido confirmado

Los pedidos con estado `confirmado` reflejan aquellos pedidos que han pasado el filtro o proceso de cobro para poder asegurar el primer paso de atención.

Este estado es previo a `listo para despacho`. Cambiar el estado de `confirmado` a `listo para despacho` implica **asegurar que el pedido ya se encuentra empacado y etiquetado para su despacho**.

Dependiendo del **rol**, se podrán ejecutar diferentes acciones en el detalle del pedido.

### Edición de cantidad de productos

La edición de cantidad de productos únicamente se puede realizar en el estado confirmado. Esta edición, permite cambiar la cantidad de cada producto en caso `el usuario desista`, `falta de stock`, `retrasos`, `error en precios`, etc.

La cantidad a editar del producto **no puede ser mayor a la cantidad original**. En pocas palabras, no se puede agregar más cantidades al producto.

### Edición de la dirección de entrega

La edición de la dirección de entrega únicamente se puede realizar en el estado confirmado. Esta edición permite modificar la geolocalización de la entrega (Coordenadas).

### Edición de referencias

La edición de las referencias se pueden realizar en el estado `confirmado` y `listo para despacho`. Esta edición permite agregar o modificar una referencia para ubicar con mayor facilidad la dirección de entrega.

### Edición de datos del destinatario

La edición de datos del destinatario permite modificar lo siguiente:

- **Nombre** y **Apellido**: El nombre y apellido de la persona que recibe el pedido.
- **Teléfono**: El número de contacto quien recibe el pedido.
- **Documento de identidad**: El tipo y número de documento de la persona que recibirá el pedido.

## Pedido listo para despacho

Los pedidos en estado `listo para despacho` reflejan aquellos pedidos que se encuentran listos para ser despachados y ser entregados al transportista (entrega a domicilio) o al usuario final (recojo en tienda).

{% include alert.html style="success" text="⚠️ Cabe mencionar que cuando un pedido es movida del estado `Confirmado` al estado `Listo para Despacho` y el subpedido es del tipo `Delivery`, la plataforma se encargara de asignar un transportista automaticamente al subpedido." %}

Este estado es previo a `en tránsito`. Cambiar el estado de `listo para despacho` a `en transito` implica **asegurar que el pedido ya se encuentra en posesión del transportista**.

Dependiendo del **rol**, se podrán ejecutar diferentes acciones en el detalle del pedido.

### Imprimir

Desde el detalle del pedido, se podrán imprimir 2 tipos de documentos:

- **Orden**: Es el resumen del pedido para ser impreso como evidencia de la compra al usuario final.
- **Etiqueta de envío**: Es la etiqueta o guía de transporte que se genera para poder tener el seguimiento correcto del pedido.

### Edición de referencias

La edición de las referencias se pueden realizar en el estado `confirmado` y `listo para despacho`. Esta edición permite agregar o modificar una referencia para ubicar con mayor facilidad la dirección de entrega.

### Edición de datos del destinatario

La edición de datos del destinatario permite modificar lo siguiente:

- **Nombre** y **Apellido**: El nombre y apellido de la persona que recibe el pedido.
- **Teléfono**: El número de contacto quien recibe el pedido.
- **Documento de identidad**: El tipo y número de documento de la persona que recibirá el pedido.

## Pedido en tránsito

Los pedidos en estado `en tránsito` reflejan aquellos pedidos que están en posesión de un transportista.

Este estado es previo a `entregado`. Cambiar el estado de `en tránsito` a `entregado` implica **asegurar que el pedido se encuentra en manos del cliente o ha sido entregado en la dirección de destino**.

## Pedidos entregados

Los pedidos en estado `entregado` reflejan aquellos los pedidos que ya están en manos de los clientes. Este estado es el último por lo que no contiene estados posteriores, pero admite la posibilidad de revertir su estado con uno anterior.

## Cambio de estado
Para cambiar de estado un pedido se deberá ingresar a la sección **Pedidos activos** y seleccionar un subpedido en particular, luego en la parte superior derecha se mostrará un botón para cambiar al estado siguiente de acuerdo a los estado mencionados<a href="#qué-estados-tienen-los-pedidos">previamente</a>.

{% include image.html img="../docs/primeros-pasos/pedidos-activos-cambio-estado.jpg" alt="Alt for image" caption="Cambio de estado de un Pedido" %}

## Revertir estado
Para revertir el estado de un pedido se deberá ingresar a la sección **Pedidos activos** y seleccionar un subpedido en particular, luego en la parte superior central existe un botón de **opciones** el cual posee una opción para revertir el pedido a su estado anterior de acuerdo a los estado mencionados <a href="#qué-estados-tienen-los-pedidos">previamente</a>.

{% include image.html img="../docs/primeros-pasos/pedidos-activos-revertir.jpg" alt="Alt for image" caption="Revertir el estado de un Pedido" %}

## Cancelar pedido
Para cancelar un pedido se deberá ingresar a la sección **Pedidos activos** y seleccionar un subpedido en particular, luego dentro del botón de opciones que se muestran en la parte superior central se muestra una opción para cancelar el pedido.

{% include image.html img="../docs/primeros-pasos/pedidos-activos-cancelar.jpg" alt="Alt for image" caption="Cancelar un Pedido" %}

Al seleccionar esta opción se mostrará un pop up en donde se deberá colocar de manera obligatoria una razón por la cual el subpedido será cancelado.
{% include image.html img="../docs/primeros-pasos/pedidos-activos-cancelar-1.jpg" alt="Alt for image" caption="Opciones de razones para cancelar un Pedido" %}

Una vez seleccionada la razón, el pedido se podrá cancelar y la vista del subpedido se actualizará mostrando la diferencia como negativo debido a que se deberá realizar una devolución al usuario del valor de los productos sin contar el valor del costo de envío.
{% include image.html img="../docs/primeros-pasos/pedidos-activos-cancelar-2.jpg" alt="Alt for image" caption="Pedido cancelado"%}

## Retener pedido
Para retener un pedido se deberá ingresar a la sección **Pedidos activos** y seleccionar un subpedido en particular, luego dentro del botón de opciones que se muestran en la parte superior central se muestra una opción para retener el pedido. 

{% include image.html img="../docs/primeros-pasos/pedidos-activos-retener.jpg" alt="Alt for image" caption="Retener un Pedido" %}

Una vez seleccionada la opción de retener pedido este pedido pasará a una nueva vista en donde se encuentran todos los pedidos retenidos.

{% include image.html img="../docs/primeros-pasos/pedidos-activos-retener-2.jpg" alt="Alt for image" caption="Retener un Pedido" %}

Al retener un pedido no podrá ser procesado dentro del flujo normal de los pedidos, ya que quedará fuera hasta que sea liberado. Para liberar un pedido, se deberá ingresar al subpedido en cuestión y se deberá seleccionar la opción de liberar pedido. Al liberar un pedido este volverá al estado anterior con el que se encontraba antes de ser retenido.
Es decir si un pedido se encontraba con el estado de **Confirmado** antes de ser retenido, luego al retenerlo paso al estado de **Retenido**, pero una vez que se libero pasa nuevamente al estado **Confirmado**.
{% include image.html img="../docs/primeros-pasos/pedidos-activos-retener-1.jpg" alt="Alt for image" caption="Liberar un Pedido" %}