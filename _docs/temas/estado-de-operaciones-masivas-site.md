---
title: Estado de operaciones
subtitle: Verifica el estado en tiempo real de la operación realizada.
tags: [Cargas_masivas,Operaciones_masivas,estado_de_operaciones_masivas]
author: Oscar Cabrera
---

## Resumen
Aqui podrás visualizar tanto el estado de las operaciones que están en curso, asi como aquellas que ya fueron realizadas.
Cada operación subida se maneja con porcentaje en donde se puede visualizar el progreso de la operación que se está ejecutando. 

También cuenta con una fecha de inicio y finalización para poder conocer en que momento se ejecuto una operación. Igualmente cuenta con el archivo que se proceso para que este puede ser consultado en todo momento.

Para cada operación manejamos 5 tipos de estados: 
* **Iniciando:** Es el primer estado y se da apenas la operación comienza.
* **En progreso:** Cuando se esta procesando la operación.
* **Finalizado:** Al finalizar satisfactoriamente la operación procesada.
* **Finalizado con error:** En caso de que existan errores al momento de procesarse cualquier operación, se generará con este estado, cabe destacar que se puede visualizará el error a detalle para que de esta manera pueda ser corregido.
* **Error:** Es un estado poco común pero se da cuando existe algún problema que impide que la operación comience.
  
## ¿Que operaciones soporta?

### **Como Site:**
* Exportación de merchants
* Exportación de tiendas
* Exportación de equipo
* Exportación de clientes
* Exportación de marcas
* Exportación de categorías
* Exportación de pedidos con filtros: 
    * `Filtro dado un rango de fechas`: Para obtener todos los pedidos que han sido efectuados dentro de un rango específico de fechas.
    * `Filtro por un código identificador de un usuario`: Para obtener todos los pedidos que han sido efectuados por un usuario en particular.
    * `Filtro por un correo electrónico`: Para obtener todos los pedidos que estan relacionados en un correo.
    * `Filtro por una campaña`: Para obtener todos los pedidos a los que se le ha aplicado una campaña.
    * `Filtro por cupón`: Para obtener todos los pedidos a los que se le ha aplicado un cupón.
    * `Filtro por estados`: Para obtener todos los pedidos de acuerdo a uno o más estados.
* Cambio masivo de estado de pedidos
* Actualización masiva de boost

En la siguiente pantalla podemos ver un ejemplo de los estados de operaciones masivas como **site**:
{% include image.html img="../docs/temas/estado-de-operaciones-masivas-3.png" alt="Alt for image" caption="Estado de operaciones masivas como site" %}

Al hacer click en la **lupa** visualizaremos una ventana como esta, donde se muestra el detalle de los **errores**:
{% include image.html img="../docs/temas/estado-de-operaciones-masivas-2.jpg" alt="Alt for image" caption="Detalle de la operación procesada" %}

En cada detalle se pueden agrupar si un error tiene la misma línea clave (**ID**, **Nombre** o **SKU del producto procesado**), en este error se puede visualizar exactamente cual es la línea en donde se encuentra y las posibles celdas en donde podría haberse cometido dicho error
{% include image.html img="../docs/temas/estado-de-operaciones-masivas-4.jpg" alt="Alt for image" caption="Detalle de la operación procesada" %}