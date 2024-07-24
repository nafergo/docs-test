---
title: Asignacion de Transportista a la Suborden
tags: [envios,transportista]
author: katlimruiz
---



Este algoritmo tiene muchisimo potencial y mucho camino por recorrer. La idea eventualmente es lograr un algoritmo "vivo" que tome una decision acerca del mejor transportista para una suborden en base a su historial, carga de trabajo, velocidad, bajo costo, etc. Sin embargo, a Julio 2021, tenemos un algoritmo mas pequeno reducido que luego se puede ir incrementando en su capacidad.

### Algunos Conceptos
Antes de detallar el algoritmo actual, es necesario mencionar algunos terminos primero:
- Suborden: Es la representacion de una orden de venta (que tambien es una orden de envio) que define el punto inicial (almacen del merchant donde esta fisicamente localizado el listado de productos vendidos) y el punto final de envio (direccion del comprador). Se asume que una suborden puede contener varios productos de una misma tienda (un celular, un cargador, una bateria extra, un protector de pantalla) y que todos los productos deben ser enviados al mismo tiempo al comprador. Una suborden siempre pertenece a una sola tienda y un merchant.
- Tipo de Suborden: Hay dos tipos de suborden: Delivery y Store Pickup. El primero es el usual donde se debe enviar el producto hacia la direccion ingresada por el comprador. El segundo es donde el comprador se acerca a un punto fisico donde el producto ya debe estar ubicado.
- Tamaño de envio: Para la suborden dada que contiene uno o mas productos se calcula un tamaño de envio (ver como se calcula TODO: link a tamano de paquete) que debe asumirse como un todo indivisible.
- Metodo de Envio: es la velocidad de envio seleccionado a nivel de suborden. Actualmente Julio 2021, la plataforma solo soporta realmente el metodo `Regular` (que permite envios a 24h o mas). En el futuro cercano, se espera poder soportar tambien `Express`, `Same Day` y `Next Day`.
- Tipo de Flota: A nivel de cada tienda, se puede escoger el tipo de flota que la tienda utilizara: `Flota Sitio` o `Flota Tienda`.

La `Flota Sitio` significa que el sitio se encarga del envio y la tienda solamente se encarga de empaquetar y entregar el paquete al transportista.

La `Flota Tienda` significa que la tienda hace sus propios envios y el sitio no interviene.

Para sitios `marketplace`, la tienda puede escoger una de las dos `Flota Sitio` o `Flota Tienda`.

Para sitios `singleplace`, solo existira `Flota Sitio`.

En ambos casos, para que las flotas funcionen, el equipo encargado (sea el del sitio o de la tienda) debe registrar la cobertura de envio y tarifas correspondientes para los territorios donde se aceptara hacer los envios.

Desde Julio 2021, la `Flota Tienda` aun no esta habilitada.

## Algoritmo
En el momento que la suborden es movida del estado `Confirmado` a `Listo para Despacho`, la plataforma intentara asignar el transportista a la suborden. A continuacion, el algoritmo que se ejecuta:

1. Verificar que la suborden sea Delivery. Si no lo es, el campo transportista a nivel de suborden queda vacio.
2. Cuando es un sitio `singleplace` o la tienda de la suborden de un marketplace tiene configurado `Flota Tienda`, el texto `S/F` (store fleet) es asignado como nombre de transportista dentro de la suborden.
3. Si la tienda de la suborden de un marketplace tiene configurado `Flota Site` y el transportista aun no ha sido asignado (ver asignacion manual), entonces se procede a continuar con calcular y asignar el transportista.
4. Finalmente, utilizando el almacen de origen y metodo de envio de la suborden, la plataforma intentara asignar a algun transportista configurado dentro del almacen como transportista preferido (segun el metodo de envio).
5. Si no hay ningun transportista que encaje, entonces la suborden no podra ser movida de estado.

Para solucionar este impase, hay varias soluciones:
1. Configurar un transportista preferido a nivel de almacen con el mismo metodo de envio de la suborden.
2. En el futuro cercano, en SiteCentral se podra asignar manualmente un transportista a una suborden. Ver seccion separada para mas detalle.

## Asignacion Manual
En el futuro cercano, el equipo del sitio podra asignar manualmente un transportista a una suborden. Para este caso, la asignacion y validacion que el transportista puede ejecutar el envio es potestad completa del equipo del sitio. De esta manera, se puede, por ejemplo, coordinar con un transportista atipico para que haga algun envio especial.

La asignacion manual se espera que se haga cuando la suborden esta en el estado `Confirmado`. Y como se menciona antes, si ya se asigno manualmente el transportista, entonces la plataforma no tratara de asignarlo segun el algoritmo anterior.

Roles: `sitelogistic`
