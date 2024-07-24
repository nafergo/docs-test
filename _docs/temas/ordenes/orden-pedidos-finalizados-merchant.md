---
title: Pedidos finalizados
subtitle: Pedidos que se encuentran en un estado final.
tags: [Pedidos_finalizados]
author: Luis Zumaeta
---

Los pedidos finalizados son todos aquellos que han llegado a un estado final y no poseen un estado posterior. Principalmente abarcan los estados `entregados` y `cancelados`.

Todos los pedidos que se muestran son relacionados a la **tienda** en donde se efectúa el pedido y pueden ser filtrados por estados mediante las pestañas. Al hacer clic en el número del pedido, se podrá ingresar a la sección de mayor detalle del pedido.

## Pedidos finalizados
Ingresando a la sección **Pedidos finalizados** podrás encontrar los pedidos que tengan los estados *Entregados* y *Cancelados*, para esto solo deberás hacer click en la pestaña correspondiente.

{% include image.html img="../docs/primeros-pasos/pedidos-finalizados.png" alt="Alt for image" caption="Pedidos Finalizados" %}

También podrás visualizar algunas opciones como **Iniciar descarga**, la cual permite obtener un archivo Excel con todos los registros necesarios de los pedidos y también existe otra opción de **Filtros**, en donde se puede filtrar estos pedidos por: 
 * **Filtro por fecha de creación dado un rango de fechas:** Para obtener todos los pedidos que han sido creados dentro de un rango específico de fechas.
 * **Filtro por fecha máxima de envío dado un rango de fechas:** Para obtener todos los pedidos que han sido o serán entregados dentro de un rango específico de fechas.
 * **Filtro por transportista:** Para obtener todos los pedidos que han sido o serán entregados por un transportista en particular.
 * **Filtro por método de pago:** Para obtener todos los pedidos que han sido pagados con un método de pago correspondiente.
 * **Filtro por un código identificador de un usuario:** Para obtener todos los pedidos que han sido efectuados por un usuario en particular.
 * **Filtro por un correo electrónico:** Para obtener todos los pedidos que estan relacionados en un correo.
 * **Filtro por una tienda:** Para obtener todos los pedidos que estan relacionados a una tienda.
 * **Filtro por un almacén:** Para obtener todos los pedidos que estan relacionados a un almacén.

## Pedido cancelados

Los pedidos en estado `cancelados`, no pueden ser modificados debido a que es un estado **final**.

***Se tiene que estar completamente seguro para cancelar un pedido***.

{% include image.html img="../docs/primeros-pasos/pedidos-finalizados-1.png" alt="Alt for image" caption="Pedidos Cancelados" %}

## Pedido entregados

Los pedidos en estado `entregados` reflejan aquellos pedidos que se encuentran en el destino del usuario final o después de que el usuario recoja el producto.

Cambiar el estado de `en tránsito` a `entregados` implica **asegurar que el pedido se encuentra en manos del cliente o ha sido entregado en la dirección de destino**..

Dependiendo del **rol**, se podrán ejecutar diferentes acciones en el detalle del pedido.

{% include image.html img="../docs/primeros-pasos/pedidos-finalizados-2.png" alt="Alt for image" caption="Pedidos Entregados" %}