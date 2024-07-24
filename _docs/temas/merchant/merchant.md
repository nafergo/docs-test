---
title: Merchants
subtitle: Un merchant representa la empresa autorizada de vender los productos que aparecen en el catalogo.
tags: [merchant]
author: katlimruiz
---

Un merchant representa la empresa autorizada de vender los productos que aparecen en el catálogo. Asímismo, cuando el sitio es **marketplace**, es una entidad importante en la plataforma puesto que algunas funcionalidades estan diseñadas para que el merchant tenga cierta autonomia en varios de los procesos de negocio, por lo que si es importante que este bien configurado.

## Según tipo de sitio
En sitios **singleplace**, el dueño del sitio y el merchant son la misma empresa y tiene el mismo equipo (el del sitio). En este nivel, no existe equipo de merchant y los roles del merchant tampoco son visibles.

En sitios **marketplace**, el merchant se registra como vendedor dentro del marketplace y es dueño de una o más tiendas que contienen productos que son vendidos a través del marketplace.

Un merchant tiene un equipo de trabajo (al que se le pueden asignar distintos roles dentro del merchant) y se encarga del control y mantenimiento de una o varias tiendas y de todos sus productos y almacenes.

## Definicion
Un merchant tiene los siguientes campos:
- **Nombre**: Este debe ser el **nombre legal** del merchant. No puede repetirse dentro del mismo país.
- **Identificador legal**: El identificador legal del merchant dentro del pais de origen. Recordar que aún cuando la empresa fuera una transnacional, cada pais cuenta con una oficina comercial dentro de cada pais al menos para poder importar y/o distribuir y/o vender sus productos. No puede repetirse dentro del mismo país.
- **Codigo Externo**: Este es un codigo externo opcional que se le puede asignar al merchant. Utilizado principalmente como dato que se necesita para ciertas integraciones.
- **Nombre de Persona de Ventas**: Nombre completo de la persona encargada o representante principal de ventas del merchant dentro del marketplace o dentro del sitio (para singleplace).
- **Correo electronico de Persona de Ventas**: correo electronico de la persona de ventas.
- **Telefono de Persona de Ventas**: teléfono fijo o celular de la persona de ventas.
- **Nombre de Persona de Operaciones**: Nombre completo de la persona encargada o representante principal de operaciones (envios y post-venta principalmente) del merchant dentro del marketplace o dentro del sitio (para singleplace).
- **Correo electronico de Persona de Operaciones**: correo electronico de la persona de operaciones.
- **Telefono de Persona de Operaciones**: telefono fijo o celular de la persona de operaciones.

Esta sección permite como Site crear nuevos Merchants, teniendo las siguientes opciones:
- Crear Merchant: Permite crear Merchant.
- Iniciar descarga: Reporte en Excel de la Información de todas los Merchants existentes.
- Buscar: Búsqueda de Merchants.
- Acciones: Editar información del Merchant como información básica, logo, categorías, configuración y opciones.

{% include image.html img="../docs/primeros-pasos/merchant.png" alt="Alt for image" caption="Merchant" %}

{% include image.html img="../docs/primeros-pasos/editar-merchant.png" alt="Alt for image" caption="Editar Merchant" %}

Por último, los **merchants** suelen tener entidades importantes como las **tiendas** y **almacenes** que permiten su total funcionamiento. Por ejemplo:

- `1 Merchant - 1 tienda - N Almacenes`
- `1 Merchant - N tiendas - 1 Almacén`
- `1 Merchant - N Tiendas - N Almacenes`
