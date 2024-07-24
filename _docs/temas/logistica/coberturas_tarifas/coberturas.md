---
title: Coberturas
subtitle: Las coberturas definen el rango de distribución por cada método de envío.
tags: [envios,cobertura]
author: Luis Zumaeta
---

Las coberturas son independientes por cada método de envío con la finalidad de atender los rangos de distribución según los recursos que se tengan disponibles.

Para entender el funcionamiento de las coberturas es necesario entender los siguientes conceptos:
- Metodos de envío (Revisar la sección de "Metodos de envío")
- Zonas
- Polígonos

## Zonas
Una zona es el conjunto de 1 o varios polígonos. Las zonas pueden ser personalizadas por el nombre y por el color.

Las zonas permiten agrupar varios polígonos para una gestión más sencilla de edición de coberturas. Es como trabajar por capas.

Una zona como mínimo debe contener 1 polígono y puede tener ilimitados polígonos.

Una vez creada la zona, es posible:
- Editar el nombre.
- Agregar más polígonos.
- Eliminar la zona (Incluye todos los polígonos)

Ejemplo de como usar **Zonas** con varios polígonos:

`Digamos que nuestra cobertura son zonas Urbanas cuya posición geográfica son polos opuestos.`
`Podríamos poner un polígono en el extremos A y otro polígono en el extremo B.`
`De esta manera representan 1 misma zona apesar de estar separados por 2 polígonos.`

## Polígonos
Es la unidad más pequeña de edición de una cobertura. Los polígonos no pueden ser nombrados y adaptan el color de la zona a la que pertenece.

Los polígonos permiten una flexibilidad muy grande para poder definir claramente los límites de cada posición geográfica.

Los polígonos pueden sobreponerse/traslaparse entre ellos sin ningún inconveniente, siempre y cuando, sean polígonos diferentes.

Una vez creado el polígono, es posible:

- Editar el polígono.
- Eliminar el polígono.

***Un polígono no puede traslaparse a sí mismo debido a que puede generar conflicto.***

Una vez entendido los *Metodos de envío*, *Coberturas*, *zonas* y *Poligonos*, pasaremos
a hablar de las funcionalidades en esta sección de **Coberturas y tarifas**.

## Crear cobertura
Todos los métodos de envío poseen coberturas diferentes, esto permite una personalización correcta considerando tiempos, tarifas y coberturas geolocalizadas. Para crear una cobertura nos dirigimos a **Coberturas y tarifas**, presionamos el boton **Crear cobertura** y escogemos un **Metodo de envio**.
{% include image.html img="../docs/temas/logistica/coberturas_tarifas/cobertura-tarifa-1.png" alt="Alt for image" caption="prueba" %}
Nos saldra un recuadro donde escogeremos el metodo de envio para la cobertura.
{% include alert.html style="success" text="⚠️ Cabe mencionar que cuando no se pueden crear dos cobertuas con el mismo metodo de envio." %}
{% include image.html img="../docs/temas/logistica/coberturas_tarifas/cobertura-tarifa-2.png" alt="Alt for image" caption="prueba" %}

Cuando creamos una cobertura, el sistema le tambien las tarifas que son 2 lladas "tarifa 1" y "tarifa 2" ademas el sistema le asigna a la cobertura recien creada, la tarifa 1 como su tarifa actual. La tarifa actual puede cambiar yendo a la opcion de **Seleccionar tarifa** que se explicara mas adelante.

Ahora pasaremos a ver todas las acciones que podemos hacer para una cobertura y para eso le damos click al boton de la columna Acciones.
{% include alert.html style="success" text="⚠️ Cabe mencionar que cuando entremos al apartado de Coberturas en una campaña solo se podran ver las opciones de Publicar cobertura, Editar cobertura y Configuracion." %}
{% include image.html img="../docs/temas/logistica/coberturas_tarifas/cobertura-tarifa-3.png" alt="Alt for image" caption="prueba" %}


## Editar cobertura
Para poder editar una cobertura, iremos al boton en la columna Acciones y vamos a **Editar cobertura**.
{% include image.html img="../docs/temas/logistica/coberturas_tarifas/editar-cobertura-1.png" alt="Alt for image" caption="prueba" %}
En esta sección crearemos "Zonas y polígonos" que determinarán la geolocalización de recojo y entrega.
{% include image.html img="../docs/temas/logistica/coberturas_tarifas/editar-cobertura-2.png" alt="Alt for image" caption="prueba" %}

### Crear zona
Para crear una zona debemos presionar el boton de **Crear zona**.
{% include alert.html style="success" text="⚠️ Cabe mencionar que cuando entremos al apartado de Coberturas en una campaña y vamos a Editar cobertura, solo se podra crear una zona por cobertura." %}
{% include image.html img="../docs/temas/logistica/coberturas_tarifas/editar-cobertura-3.png" alt="Alt for image" caption="prueba" %}
Nos muestra un recuadro para que coloques el nombre de la zona, que debe ser unico por cobertura, y escogemos el color del poligono de la zona. 
{% include image.html img="../docs/temas/logistica/coberturas_tarifas/editar-cobertura-4.png" alt="Alt for image" caption="prueba" %}

Luego se creara un poligono en un mapa, donde podras editar la forma del poligono dandole click a alguna de los puntos que sale en los lados del poligono, y finalmente le debes dar a **Guardar cambios** para guardar el poligono de la zona.
{% include image.html img="../docs/temas/logistica/coberturas_tarifas/editar-cobertura-5.png" alt="Alt for image" caption="prueba" %}

### Editar zona
Para poder editar la zona, nos vamos boton con sus opciones.
{% include image.html img="../docs/temas/logistica/coberturas_tarifas/editar-cobertura-6.png" alt="Alt for image" caption="prueba" %}

## Editar tarifas
En esta sección crearemos "Tarifas y tiempos de envío" entre las zonas habilitadas como coberturas.

Para mayor información puedes revisar la sección de "Tarifas".

## Seleccionar tarifa
Para poder seleccionar una tarifa, primero la tarifa que se quiere seleccionar debe tener como minimo una ruta tarifaria y dicha ruta tarifaria debe tener como minimo una condicion especial.

Para mayor información puedes revisar la sección de "Tarifas".

Para poder seleccionar una tarifa, iremos al boton en la columna Acciones y vamos a **Seleccionar tarifa**.
{% include image.html img="../docs/temas/logistica/coberturas_tarifas/seleccionar-tarifa-1.png" alt="Alt for image" caption="prueba" %}
Nos mostrara las tarifas disponibles para que sean seleccionadas ademas de decirme cual es la tarifa actual, que sea la que esta ya seleccionada.
{% include image.html img="../docs/temas/logistica/coberturas_tarifas/seleccionar-tarifa-2.png" alt="Alt for image" caption="prueba" %}
Finalmente nos mostrara un recuadro donde pedira la confirmacion del paciente con respecto al nombre de a tarifa.
{% include image.html img="../docs/temas/logistica/coberturas_tarifas/seleccionar-tarifa-3.png" alt="Alt for image" caption="prueba" %}

## Configuración
Para poder configurar el metodo de envio de la cobertura, iremos al boton en la columna Acciones y vamos a **Configuracion**.
{% include alert.html style="success" text="⚠️ Cabe mencionar que cuando estemos en el apartado de Coberturas de una campaña, esta opcion de Configuracion solo se podra ver cuando se haya creado una zona." %}
{% include image.html img="../docs/temas/logistica/coberturas_tarifas/configuracion-1.png" alt="Alt for image" caption="prueba" %}

Para mayor informacion puedes revisar la seccion de "Metodos de envío".

## Publicar cobertura
Para poder publicar una cobertura, la tarifa actual debe tener como minimo una ruta tarifaria y dicha ruta tarifaria debe tener como minimo una condicion especial, en caso contrario el boton de **Publicar cobertura** no aparecera.

{% include alert.html style="success" text="⚠️ Cabe mencionar que cuando estemos en el apartado de Coberturas de una campaña, esta opcion de Publicar cobertura solo se podra ver cuando se haya creado una zona." %}
Iremos al boton de la columna Acciones y vamos a **Publicar cobertura**. 
{% include image.html img="../docs/temas/logistica/coberturas_tarifas/publicar-cobertura.png" alt="Alt for image" caption="prueba" %}

Cuando edito una cobertura y dicha cobertura esta publicada, su estado de publicacion cambiara a pendiente. Esto solo pasara cuando edito una cobertura.

Por último, es muy importante recalcar que cualquier cambio para que se vea reflejado en la web es necesario **"Pubicar coberturas"**

El estado de publicación, siempre nos informará si la cobertura está actualizado con el estado **Publicada** o si se encuentra **Pendiente**.