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

### **Como Merchant:**
* Creación masiva de productos
* Creación masiva completa de productos
* Actualización masiva completa de productos
* Actualización masiva de productos
* Actualización masiva de imágenes
* Actualización masiva de stocks
* Actualización masiva de precios bases
* Actualización masiva de precios promocionales
* Activación y desactivación masiva de productos
* Actualización masiva de imágenes externas de variaciones
* Activación y desactivación masiva de variaciones
* Actualización de boost

En la siguiente pantalla podemos ver un ejemplo de los estados de operaciones masivas como **merchant**:
{% include image.html img="../docs/temas/estado-de-operaciones-masivas-1.jpg" alt="Alt for image" caption="Estado de operaciones masivas como merchant" %}

Al hacer click en la **lupa** visualizaremos una ventana como esta, donde se muestra el detalle de los **errores**:
{% include image.html img="../docs/temas/estado-de-operaciones-masivas-2.jpg" alt="Alt for image" caption="Detalle de la operación procesada" %}

En cada detalle se pueden agrupar si un error tiene la misma línea clave (**ID**, **Nombre** o **SKU del producto procesado**), en este error se puede visualizar exactamente cual es la línea en donde se encuentra y las posibles celdas en donde podría haberse cometido dicho error
{% include image.html img="../docs/temas/estado-de-operaciones-masivas-4.jpg" alt="Alt for image" caption="Detalle de la operación procesada" %}