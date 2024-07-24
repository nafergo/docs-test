---
title: Tiendas
subtitle: Una tienda representa principalmente el nombre comercial o la división de diferentes negocios del merchant.
tags: [merchant,crear_tienda]
author: Luis Zumaeta
---

### **Como Site:**

La opción de **tienda** solo se encuentra disponible para sitios **marketplace**.

Un **Merchant/Seller** puede tener múltiples **tiendas** siempre y cuando el dueño del **marketplace** se lo permita. El rol principalmente encargado de realizar las configuraciones necesarias sería **SiteMerchantRep** y/o **SiteSale**.

Las tiendas suelen representar el nombre comercial, diferentes negocios o proyectos para un merchant.

- Un merchant puede llamarse Empresa XYZ; sin embargo, es más conocida como `Techpro Sellers`:

Por ejemplo: 
```
Merchant: Empresa XYZ
Tienda: Techpro Sellers
```

- Un merchant puede poseer la exclusividad de 1 o varias marca(s) y decide abrir una tienda ancla para vender todos los productos de dicha marca:

```
Merchant: Empresa XYZ
Tienda: Apple
Tienda: Samsung
Tienda: Huawei
```
- Un Merchant puede tener 1 o varios tipos de negocio y decide abrir tiendas diferentes para estrategias/productos diferentes.

Por ejemplo: 
```
Merchant: Empresa ABC
Tienda: Comestibles diarios.
Tienda: Muebles finos.
Tienda: Deportes extremos.
```

También se permite como Site crear nuevas tiendas, teniendo las siguientes opciones:
- Crear Tienda: Permite crear Tiendas.
- Iniciar descarga: Reporte en Excel de la Información de todas las Tiendas existentes.
- Buscar: Búsqueda de Tiendas.
- Acciones: Editar información de la Tienda como información básica, logo, categorías, configuración y opciones.

{% include image.html img="../docs/primeros-pasos/tienda.png" alt="Alt for image" caption="Tienda" %}

{% include image.html img="../docs/primeros-pasos/tienda-2.png" alt="Alt for image" caption="Editar tienda" %}

Al editar podemos visualizar el logo de la tienda.
{% include image.html img="../docs/primeros-pasos/tienda-3.png" alt="Alt for image" caption="Editar tienda" %}

Al editar podemos visualizar la categoría de la tienda y el Meta keywords.
{% include image.html img="../docs/primeros-pasos/tienda-4.png" alt="Alt for image" caption="Editar tienda" %}

Al editar podemos colocar el monto mínimo que el usuario debe agregar al carrito para poder comprar los productos de la tienda.
{% include image.html img="../docs/primeros-pasos/tienda-5.png" alt="Alt for image" caption="Editar tienda" %}

Al editar podemos seleccionar si la tienda se va visualizar en la plataforma, el porcentaje de Comisión por venta, el Boost (Mayor prioridad asignada a la tienda para destacarla del resto) y el Asesor comercial.
{% include image.html img="../docs/primeros-pasos/tienda-6.png" alt="Alt for image" caption="Editar tienda" %}

## Crear tienda

En sitios **marketplace**, la tienda es habilitada desde la pantalla **Tiendas** en el menú lateral izquierdo. Para ello, debemos estar en la pantalla indicada y hacer clic en "Crear tienda".

{% include image.html img="../docs/primeros-pasos/tienda-crear.png" alt="Alt for image" caption="Crear tienda" %}

Cada **tienda** tiene que estar vinculada con un **merchant**.

El **SiteOwner (dueño del marketplace)**, debe ingresar los siguientes datos en consenso con el Merchant:

### Nombre de la tienda

El nombre de la **tienda** no podrá ser editado posteriormente y se verá reflejado como nombre en la web.

### Categorías de la tienda

Son las categorías a las cuales una tienda puede estar vinculada (Máximo 5).

### Comisión por venta

Es la comisión impuesta por el **Siteowner** sobre todos los productos que el **merchant** logre vender.

### Asesor comercial

Es la persona responsable o ejecutivo de cuenta **(Sitesale)** que estableció o gestionará la relación comercial con el **merchant**. 