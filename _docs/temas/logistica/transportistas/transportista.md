---
title: Transportistas
subtitle: Un transportista representa una empresa que se asocia con el sitio para otorgar el servicio de envio de los productos vendidos.
tags: [envios,tema_transportista]
author: katlimruiz
---

Un transportista representa una empresa que se asocia con el sitio para otorgar el servicio de envio de los productos vendidos.

Su uso empieza cuando la suborden pasa del estado `Confirmado` a `Listo para Despacho`.

Si la suborden es del tipo de envio Delivery, la plataforma intentara emparejar a la suborden con algun transportista apto para llevar esos productos desde el almacen del merchant hacia el destino ingresado por el comprador.

Para lograr esto, la plataforma cuenta con un algoritmo propio que se puede leer mas a detalle aqui (TODO: link a algoritmo de seleccion de transportista).

Una vez el transportista es asignado a la suborden y la suborden pasa a estado `Listo para Despacho`, el proceso de envio empieza a ejecutarse (TODO: link a proceso de envio).

## Definicion
Un transportista tiene estos campos:
- **Nombre**: Nombre del transportista que puede ser llenado distinto que el nombre legal del transportista. No se puede repetir.
- **Identificador Legal**: Numero del identificador legal del transportista.
- **Nombre Legal**: Nombre legal de la empresa transportista.
- **Nombre de Persona de Operaciones**: Nombre completo de la persona contacto de las operaciones del transportista. Este deberia ser el contacto principal a quien se puede acudir si hay retrasos, cambios o etc.
- **Telefono de Persona de Operaciones**: Telefono fijo o celular de la persona contacto de las operaciones del transportista.
- **Correo electronico de Persona de Operaciones**: Correo electronico de la persona contacto de las operaciones del transportista.
- **Nombre de Persona de Comercial**: Nombre completo de la persona contacto del transportista para ver temas de tarifario. Este deberia ser el contacto principal a quien se puede acudir si hay negociacion en el tarifario de costos de envio.
- **Telefono de Persona de Comercial**: Telefono fijo o celular de la persona contacto del transportista para ver temas de tarifario.
- **Correo electronico de Persona de Comercial**: Correo electronico de la persona contacto del transportista para ver temas de tarifario.
- **Notas**: Notas internas que se le puede agregar al transportistas y que son solo visibles por el equipo del sitio.

## Crear transportista
En SiteCentral, ingresar a la opcion de Transportistas, y utilizar el boton **Crear Transportista**.
{% include image.html img="../docs/temas/logistica/transportistas/crear-transportista-1.png" alt="Alt for image" caption="prueba" %}
Aqui debemos ingresar los datos del nuevo transportista como *Nombre*, *Identificador legar*, *Nombre legal*, *Contacto de operaciones*, *Contacto comercial* y *Notas*.
{% include image.html img="../docs/temas/logistica/transportistas/crear-transportista-2.png" alt="Alt for image" caption="prueba" %}

## Editar transportista
En SiteCentral, ingresar a la opcion de Transportistas, y buscar el transportista por su nombre. Una vez encontrado, utilizar el boton en la columna Acciones.
{% include image.html img="../docs/temas/logistica/transportistas/editar-transportista-1.png" alt="Alt for image" caption="prueba" %}
Luego nos mostrara toda la informacion del transportista.
{% include image.html img="../docs/temas/logistica/transportistas/editar-transportista-2.png" alt="Alt for image" caption="prueba" %}
{% include image.html img="../docs/temas/logistica/transportistas/editar-transportista-3.png" alt="Alt for image" caption="prueba" %}
{% include image.html img="../docs/temas/logistica/transportistas/editar-transportista-4.png" alt="Alt for image" caption="prueba" %}

## Eliminar transportista
En SiteCentral, ingresar a la opcion de Transportistas, y buscar el transportista por su nombre. Una vez encontrado, utilizar el boton en la columna Acciones. Una vez dentro, seleccionar el boton **Eliminar**.