---
title: Tarifas
subtitle: Las sección de tarifas nos permite editar el precio de envío hacia los usuarios finales.
tags: [envios,cobertura]
author: Luis Zumaeta
---

## Tarifas
La plataforma permite configurar 2 tarifas por cada cobertura.

Las tarifas están conformadas por un número ilimitado de rutas tarifarias.

## Rutas tarifarias
Son todas las combinaciones posibles que se realizan entre zonas.

Las rutas tarifarias permiten realizar todas las combinaciones entre zonas para crear las condiciones necesarias del precio de envío.

Cada ruta tarifaria puede contener infinitas condiciones especiales con la finalidad de ser altamente estratégico.

### Editar tarifa
Para poder editar una tarifa, iremos al boton en la columna Acciones y vamos a **Editar tarifa**.
{% include image.html img="../docs/temas/logistica/coberturas_tarifas/editar-tarifa-1.png" alt="Alt for image" caption="prueba" %}

#### Crear ruta tarifaria
Si queremos crear una **Ruta tarifaria**, daremos click al boton Ruta tarifaria
{% include image.html img="../docs/temas/logistica/coberturas_tarifas/editar-tarifa-2.png" alt="Alt for image" caption="prueba" %}
Seleccionamos la ruta de origen y destino, al igual que el plazo de entrega en horas.
{% include image.html img="../docs/temas/logistica/coberturas_tarifas/editar-tarifa-3.png" alt="Alt for image" caption="prueba" %}

#### Editar ruta tarifaria
Una vez creada la ruta tarifaria, veremos los datos de la ruta creada, con un apartado donde podremos cambiar la zona de origin y destino, al igual que su plazo de entrega en horas.
{% include image.html img="../docs/temas/logistica/coberturas_tarifas/editar-tarifa-4.png" alt="Alt for image" caption="prueba" %}

### Condiciones especiales
Las condiciones especiales están sujetas por:

- Tamaño de envío.
- Monto del ticket de la orden.

Con esta flexibilidad se pueden crear varios precios de envíos, por ejemplo:

Imaginemos que queremos segmentar nuestros precios según tamaños:

| N° | Tamaño | Subtotal desde | Subtotal Hasta | Precio |
|---|---|---|---|---|
| 1 | XXS, XS | - | - | $10 |
| 2 | S | - | - | $20 |
| 3 | M, L | - | - | $30 |
| 4 | XL, XXL | - | - | $40 |

Tal vez querramos segmentar por tamaños y por ticket de compra:

|Tamaño | Subtotal desde | Subtotal Hasta | Precio |
|---|---|---|---|
| XXS, XS | 0 | 150 | $20 |
| XXS, XS | 150 | - | $0 |
| S | 0 | 350 | $15 |
| S | 350 | - | $10 |
| M, L | 0 | 150 | $20 |
| M, L | 150 | 350 | $15 |
| M, L | 350 | - | $5 |
| XL, XXL | - | - | $ |

Tal vez querramos que nuestros precios sean flat:

|Tamaño | Subtotal desde | Subtotal Hasta | Precio |
|---|---|---|---|
| - | - | - | $15 |

Ó

|Tamaño | Subtotal desde | Subtotal Hasta | Precio |
|---|---|---|---|
| XXS, XS, S, M, L, XL, XXL | - | - | $15 |

Con estos ejemplos, es claro que podemos crear varias condiciones de precios de envío entre 2 zonas.

#### Crear condiciones especiales
Para crear una condicion especial en una ruta tarifaria, nos dirigiremos a "Agregar mas condiciones".
{% include image.html img="../docs/temas/logistica/coberturas_tarifas/editar-tarifa-5.png" alt="Alt for image" caption="prueba" %}


Por último, es muy importante recalcar que cualquier cambio para que se vea reflejado en la web, es necesario **"Pubicar coberturas"**

Esta acción la podemos realizar desde la sección de "Coberturas y tarifas" en el botón de acciones.

El estado de publicación, siempre nos informará si el método de envío está actualizado con el estado **Publicada** o si se encuentra **Pendiente**.