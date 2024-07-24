---
title: Nuevo pedido
subtitle: 
tags: [nuevo_pedido]
author: ivan
---
## ¿Qué estados tienen los pedidos?
> **Nuevo**: Es el primer estado con el que la orden es creada.
> 
> **Pendiente de pago**: Después de que la orden se crea pasa a ser pendiente de pago, hasta que se efectue el pago.
> 
> **Rechazado**: En caso de que suceda algún problema al momento de efectuarse el pago, el pedido obtiene este estado.
> 
> **Confirmado**: Si el pago fue satisfactorio, el pedido termina confirmándose.
> 
> **Listo para despacho**: Al empezar a ser procesado por el merchant, se puede colocar a listo para despacho en caso de que ya se tenga preparado el pedido para despecharse.
> 
> **En tránsito**: Cuando el pedido se encuentra en camino a ser entregado por el transportista.
> 
> **Entregado**: Al ser entregado el pedido hasta el cliente final.
> 
> **Cancelado**: Este estado puede darse en cualquier momento dentro del flujo de pedidos excepto cuando un pedido tiene el estado de **Entregado**.
> 
> **Retenido**: De igual manera este estado puede darse en cualquier momento dentro del flujo normal de pedidos excepto cuando un pedido tiene el estado de **Entregado**.

## Pedidos
Ingresando a la opción **Pedidos** podrás encontrar todos los pedidos que se han realizado las últimas 24 horas. También podrás visualizar algunas opciones como **Iniciar descarga**, la cual permite obtener un archivo Excel con todos los registros necesarios de los pedidos y también existe otra opción de **Filtros**, en donde se puede filtrar estos pedidos por: 
 * **Filtro dado un rango de fechas:** Para obtener todos los pedidos que han sido efectuados dentro de un rango específico de fechas.
 * **Filtro por un código identificador de un usuario:** Para obtener todos los pedidos que han sido efectuados por un usuario en particular.
 * **Filtro por un correo electrónico:** Para obtener todos los pedidos que estan relacionados en un correo.
 * **Filtro por una campaña:** Para obtener todos los pedidos a los que se le ha aplicado una campaña.
 * **Filtro por cupón:** Para obtener todos los pedidos a los que se le ha aplicado un cupón.
 * **Filtro por estados:** Para obtener todos los pedidos de acuerdo a uno o más estados.

{% include image.html img="../docs/primeros-pasos/pedidos.jpg" alt="Alt for image" caption="Pedidos" %}

## Sincronizar Orden
Dentro de un pedido se podrá visualizar una vista como la que se mostrará a continuación, en donde se puede sincronizar una orden en caso de que se tenga una integración con una pasarela de pagos de terceros.

{% include image.html img="../docs/primeros-pasos/pedidos-sincronizar.jpg" alt="Alt for image" caption="Sincronizar Orden" %}

## ¿Cómo se agrupan los pedidos?
Cada pedido puede tener uno o más subpedidos, los cuales son agrupados de acuerdo al almacén desde donde se recolectan los productos. Es decir si se tiene un pedido con 2 productos diferentes, el producto A1 se obtiene desde el almacén B1 y el producto A2 se obtiene desde el almacén B2, entonces se creará un pedido con 2 subpedidos. Caso contrario de que ambos productos se encuentren en el mismo almacén entonces solo se crearía un subpedido que contendría estos 2 productos.

Existen 2 tipos de subpedidos: Entrega a domicilio y Retiro en tienda. El primero es el usual donde se debe enviar el producto hacia la direccion ingresada por el comprador y el segundo es donde el comprador se acerca a un punto fisico donde el producto ya debe estar ubicado.

{% include image.html img="../docs/primeros-pasos/pedidos-agrupamiento.jpg" alt="Alt for image" caption="Pedidos Agrupamiento" %}