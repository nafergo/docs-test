---
title: Tamaños de envios
subtitle: Todos los paquetes que se envian a los compradores son clasificados segun sus dimensiones y peso en una escala configurable de tamaños para que de esta manera se pueda homogeneizar los precios de envio.
tags: [envios,transportista]
author: joaquin
---

Los tamaños de envio representan una escala configurable que permite clasificar los paquetes que son enviados a los compradores de manera homogenia y asi facilitar la configuracion y calculo de los precios de envio.

Los tamaños de envio disponibles en la plataforma son:
- XXS
- XS
- S
- M
- L
- XL
- XXL

Esta lista no se puede añadir ni reducir (creemos que con siete posibles medidas es suficiente), pero lo que si se puede configurar a nivel de sitio son las medidas maximas de cada tamaño y si alguna esta habilitada o no.

## Algoritmo
Primero, la plataforma asume que el paquete a ser enviado al comprador contiene todos los items de una suborden: si la suborden contiene 3 pantalones, 4 camisas y dos correas, entonces todo eso se asume como un solo paquete y un solo envio.

NOTA: en el checkout es donde se separa las subordenes en base a la cercania de los almacenes y stocks. Este algoritmo de tamaños de envio se circunscribe a lo que ya contiene la suborden. Si la suborden debio ser agrupada de manera distinta, no esta dentro del alcance de este algoritmo.

Asumiendo que la suborden es asi:

| Item | Cantidad | Pq Largo Cms | Pq Ancho Cms | Pq Alto Cms | Pq Peso Kg |
|---|---|---|---|---|---|
| Pantalon | 3 | 30 | 30 | 30 | 0.3 |
| Camisa | 4 | 30 | 30 | 30 | 0.3 |
| Correa | 2 | 30 | 30 | 30 | 0.3 |

El peso total de todo esto seria `SUM(Item.PqPesoKg * Item.Cantidad)` = `2.7kg`.

El volumen total seria `SUM(Item.PqLargoCms * Item.PqAnchoCms * Item.PqAltoCms * Item.Cantidad)` = `81,000 + 108,000 + 54,000 = 243,000cm3`.

Y los tamaños podrian estar configurados asi:
![Tamaños de envio](../tamano-envio1.png)

Entonces, la plataforma verificará desde el primer tamaño habilitado (`XXS`, `XS`...):
- Condición 1: si es que el volumen total y el peso maximo estan dentro de los maximos de ese nivel.
- Condición 2: ninguna dimensión del paquete sea mayor a ninguna dimension del tamaño. Es decir: `30<100, 30<100, 30<100`. NOTA: dado que el alto, ancho o largo son relativos al punto de vista, en la realidad, la validacion se hace todas las medidas del paquete contra todas las medidas maximas.

Si las dos condiciones se cumplen entonces ese tamaño se asigna al paquete. Si no es asi, entonces se pasa al siguiente tamaño.

Si ninguno encaja, entonces se le asigna el ultimo tamaño habilitado (dado que se considera que siempre es el mas grande de todos). De esta manera, un paquete siempre tendra un tamaño asignado.

## Definicion
Un tamaño de envio tiene los siguientes campos:
- **Tamaño**: Codigo que representa el tamaño. La plataforma sigue el formato "t-shirt size" o "tamaño de camiseta". Desde XXS a XXL.
- **Altura Maxima**: Valor en centimetros de la altura maxima permitida del paquete.
- **Ancho Maximo**: Valor en centimetros del ancho maximo permitido del paquete.
- **Largo Maximo**: Valor en centimetros de largo maximo permitido del paquete.
- **Peso Maximo**: Valor en kilogramos de peso maximo permitido del paquete.
- **Habilitado**: Este campo representa si el tamaño esta habilitado o no. Esto sirve en caso el sitio escoge no utilizar tantas escalas (por ejemplo, podria querer usar solamente S, M, L si sabe que los productos en el catalogo pueden manejarse de esa manera o peor aun hasta podrian manejar un solo tamaño que tambien es posible).

## Crear tamaños de envio
Cuando el sitio es creado, como parte del proceso de onboarding o de configuracion inicial, es responsabilidad del equipo del sitio crear los tamaños de envio. Para hacerlo, en SiteCentral, se ingresa a la opcion de `Tamaños de Envio`, donde si es que no hay ningun tamaño registrado, solo aparecerá el boton de `Crear Tamaños`. Al presionar el boton, la plataforma creará los siete tamaños con medidas por defecto. A partir de ahi, el equipo del sitio, decidira si cambia o no las medidas de cada tamaño.

## Editar tamaño de envio
En SiteCentral, en la opcion `Tamaños de Envio`, se mostraran los tamaños registrados y para modificar uno de ellos, se debe presionar el boton que esta en la columna Acciones. Al presionarlo, aparece una ventana donde se puede modificar los campos ya mencionados antes.
{% include image.html img="../docs/temas/logistica/tamanios_envios/envio.png" alt="Alt for image" caption="prueba" %}

Dado que los tamaños siguen un orden ascendente y este orden no se puede cambiar, entonces las medidas maximas y peso maximo de un nivel siempre deben ser menores a la del nivel siguiente y mayores a la del nivel anterior.
{% include image.html img="../docs/temas/logistica/tamanios_envios/editar-envio-1.png" alt="Alt for image" caption="prueba" %}

## Habilitacion de un tamaño de envio
Cuando los tamaños de envio son creados, todos inician como habilitados.

Si es que el equipo del sitio decide que hay demasiados tamaños y desean reducir esto (de repente su catalogo es mas homogeneo en tamaño), el equipo puede decidir deshabilitar los tamanos de envio solo aquellos que estan al extremo de la lista.

Es decir, si inicialmente se tiene `XXS` a `XXL` y se quiere reducir la lista, solo se podra hacerlo en los dos extremos.
```
XXS << puedes deshabilitar
XS
S
M
L
XL
XXL << puedes deshabilitar
```

Esto resulta en que la lista se reduce a:
```
XS
S
M
L
XL
```

Si es que se quiere lograr tener solamente `S` y `M`, la deshabilitacion se tendria que hacer en orden:
```
XS << deshabilitar 1
S
M
L  << deshabilitar 3
XL  << deshabilitar 2
```

Cuando un tamaño es deshabilitado, como se menciono arriba, el ultimo tamaño habilitado entonces se convierte en el valor por defecto automaticamente. En el caso de arriba, originalmente era `XL`, ahora es `M`.

De manera similar, pero en el sentido contrario, para habilitar un tamaño antes deshabilitado, se tiene que hacer en orden siempre empezando por los extremos:

```
XS << habilitar 1
S
M
L  << habilitar 2
XL  << habilitar 3
```

Esto aumentaria la lista de `S, M` a `XS, S, M, L, XL`.

Como regla de la plataforma, siempre de haber al menos un tamaño habilitado, y en el caso haya uno, ese seria entonces el valor por defecto.
{% include image.html img="../docs/temas/logistica/tamanios_envios/editar-envio-2.png" alt="Alt for image" caption="prueba" %}

