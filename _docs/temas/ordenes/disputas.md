---
title: Disputas
subtitle: Devoluciones para los pedidos entregados
tags: [disputas]
author: Oscar Cabrera
---

### Crear disputas

Las **disputas** es un módulo *nuevo* y separado de los pedidos, que permite el seguimiento de *tickets* o *casos* sobre reclamos de pedidos ya entregados con la finalidad de generar algún reembolso o revisión. 

Este módulo presenta dos estados generales:
* Disputas activas: Las disputas que estan actualmente activas.
* Disputas cerradas: Las disputas que están finalizadas o abandonadas.

{% include image.html img="../docs/primeros-pasos/disputas.jpg" alt="Alt for image" caption="Disputas" %}

Para crear una disputa el pedido debe tener un estado de entregado, el principal medio para crear una disputa puede ser Servicio de Atención al Cliente, pero también se puede integrar la opción para solicitar una devolución dentro de un Singleplace/Marketplace. Además es importante destacar que cualquier disputa solo puede ser creada dentro de los 15 días después de entregar el pedido, de solicitar una devolución pasado ese tiempo la garantía de la tienda debería verse incluida.

{% include image.html img="../docs/primeros-pasos/disputas-1.jpg" alt="Alt for image" caption="Disputas" %}

Es necesario colocar una categoría y un motivo para crear una disputa, ya que esta determinará el problema exacto que presenta el cliente que solicita la devolución. También se deberá colocar el monto exacto que solicita el cliente y sus datos de contacto.

{% include image.html img="../docs/primeros-pasos/disputas-2.jpg" alt="Alt for image" caption="Disputas" %}

Las **disputas** presentan 4 estados:

* Creada: Cuando se crea la disputa a un pedido que ya ha sido entregado.
* Iniciada: Cuando la disputa ha sido iniciada
* En progreso: Cuando la disputa esta en proceso a ser resuelta.
* Finalizada: Cuando la disputa ha finalizado.
* Abandonada: Este estado puede colocarse en caso el cliente deje de lado el seguimiento de su devolución o también cuando al cabo de 30 días no se ha realizado ninguna cambio con respecto a la disputa se colocará como abandonada automáticamente.

Para iniciar con el proceso de disputa se debe seleccionar el botón de iniciar para comenzar con la resolución de la disputa. También en este punto antes de iniciarse se le debe asignar un representante para dar el seguimiento del caso.

{% include image.html img="../docs/primeros-pasos/disputas-3.jpg" alt="Alt for image" caption="Inicio de una disputa" %}

Al finalizar una devolución se muestra el recorrido de todos los estados por los que ha pasado la disputa.

{% include image.html img="../docs/primeros-pasos/disputas-5.jpg" alt="Alt for image" caption="Historial de estados de una disputa" %}