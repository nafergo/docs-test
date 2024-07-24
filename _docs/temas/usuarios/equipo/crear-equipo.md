---
title: Equipo
subtitle: 
tags: [crear_usuario]
author: ivan
---

Antes de pasar a la explicacion de como crear un usuario y sus respectivos roles que tendra, explicaremos cada rol.
## Roles:

### **SiteAdmin:**
Generalmente los responsables principales del Site.

Este usuario posee todos los permisos para la configuración del site. Puede realizar todas las funcionalidades de los otros roles. 

Las funcionalidades **únicas** a diferencia de otros roles son:
- Creación, edición y eliminación de usuarios para el equipo.
- Configuración de notificaciones a los correos destinatarios.
- Gestión de integraciones.

### **SiteCMS.**
Persona responsable del contenido de la web. Suele ser un diseñador o responsbale del marketing.

Las principales funciones que posee son:
- Gestionar el contenido de la página principal del site.
- Gestionar la data jerarquica del site.
- Gestionar las plantillas de notificaciones a los clientes.

### **SiteCMSAdmin.**
Persona jerarquicamente por encima del rol SiteCMS.

Las principales funciones **adicionales** que posee son:
- Eliminar el contenido de la página principal del site.
- Eliminar la data jerarquica del site.
- Habilitar las plantillas de correos.

### **SiteCatalog.**
Persona responsable en administrar la información del catálogo dependiendo del sitio.

Las principales funciones que posee, en sitios **Singleplace** son:
- Crear las marcas y categorías.
- Crear, editar o eliminar cualquier característica del producto del catálogo.
- Gestionar el stock de productos.
- Gestionar el boost de los productos en el catálogo

Las principales funciones que posee, en sitios **Marketplace** son:
- Crear las marcas y categorías para los merchants.
- Gestionar el boost de los productos en el catálogo.

### **SiteCatalogAdmin.**
Persona jerarquicamente por encima del rol SiteCatalog.

Las principales funciones **adicionales** que posee son:
- Eliminar productos del catálogo.
- Eliminar marcas y categorías.

### **SiteSale.** 
Persona responsable de la gestión comercial en la plataforma dependiendo del sitio.

Las principales funciones que posee, en sitios **Singleplace** son:
- Gestión de pedidos.
- Visualización del dashboard de ventas y métricas generales.
- Creación de cupones.
- Gestión de herramientas de métricas para la web.

Las principales funciones que posee, en sitios **Marketplace** son:
- Gestión y mantenimiento de Merchants.
- Gestión de pedidos.
- Editar la comisión de venta de cada Seller/Merchant.
- Editar información de los pedidos.
- Visualización del dashboard de ventas y métricas generales de todo el marketplace.
- Creación de cupones.
- Gestión de herramientas de métricas para la web.

### **SiteSaleAdmin.**
Persona jerarquicamente por encima del rol SiteSale.

Las principales funciones **adicionales** que posee son:
- Cancelar órdenes.
- Asignar asesores comerciales `SiteSales` a los sellers/merchants respectivos.

### **SiteFinance.** 
Persona en finanzas responsable de monitorear posibles intentos de fraude, bloqueo de clientes y cancelación de órdenes.

Las principales funciones que posee son:
- Retener un pedido por indicios de fraude.
- Cancelar pedidos ante evidencia de fraude.
- Bloquear usuarios potencialmente peligrosos en fraude.
- Crear y/o registrar proveedores y opciones de pago.

### **SiteFinanceAdmin.** 
Persona jerarquicamente por encima del rol SiteFinance.

Las principales funciones **adicionales** que posee son:
- Habilitar y editar las opciones de pago.
- Eliminar proveedores y opciones de pago.

### **SiteLogistic.** 
Persona encargada de la cobertura, distribución, almacenes y otras funcionalidades dependiendo del sitio.

Las principales funciones que posee, en sitios **Singleplace** son:
- Gestión propia de la logística de pedidos.
- Definir coberturas, tamaños y precios de envío.
- Crear y gestionar transportistas para la distribución.
- Gestionar almacenes y asignación de transportistas.

Las principales funciones que posee, en sitios **Marketplace** son:
- Supervisión de la logística de pedidos.
- Definir coberturas, tamaños y precios de envío.
- Habilitar métodos de envíos.
- Crear y gestionar transportistas para la distribución.
- Revisión de almacenes de los merchants.
- Asignación de transportistas.

### **SiteLogisticAdmin.** 
Persona jerarquicamente por encima del rol SiteLogistic.

Las principales funciones **adicionales** que posee son:
- Habilitar/Deshabilitar métodos de envío.
- Habilitar flota propia del merchant.
- Habilitar/Deshabilitar métodos de envío.


### **SiteEndUserRep.**
Persona encargada de ayudar a los usuarios finales ante cualquier consulta o inquietud.

- Revisión de información de pedidos.
- Modificar información de pedidos.
- Gestión de clientes.
- Gestión de disputas (Post-Venta).
- Revisar información de pagos.

### **SiteEndUserRepAdmin.**
Persona jerarquicamente por encima del rol SiteEndUserRepAdmin.

Las principales funciones **adicionales** que posee son:
- Descargar BD clientes.
- Cancelar pedidos.
- Retener órdenes.

### **SiteMerchantRep.**
Persona encargada en guiar a los merchants en su proceso de adecuación de la plataforma. Este rol solo se encuentra habilitado en los sitios **Marketplace**.

Las principales funciones que posee son:
- Todos los permisos y vistas que un MerchantAdmin.
- Modificación de datos de la tienda.
- Modificación de datos del merchant.

### **SiteMerchantRepAdmin.**
Persona jerarquicamente por encima del rol SiteMerchantRepAdmin.

Las principales funciones **adicionales** que posee son:
- Descargar BD clientes.
- Descargar BD Merchants.
- Descargar BD Tiendas.

## Combinación de roles

Los roles pueden ser sleecionados en `combo`, eso quiere decir que un usuario puede tener muchos roles asignados.

Por ejemplo:
- `Un usuario puede tener los roles SitetSale y SiteCatalog`
- `Un usuario puede tener los roles SiteSaleAdmin, SiteCatalog y SiteCMSAdmin`
- `Un usuario puede tener los roles SiteCMS, SiteFinanceAdmin y SiteEndUserRep`

Esto permite que las características principales de cada rol puedan ser asignadas a un mismo usuario para distribuir la carga o responsabilidades.


## Crear usuario
Para crear un nuevo usuario, vamos a la opción de **Equipo** y luego **Crear usuario**
{% include image.html img="../docs/temas/usuarios/equipo/crear-equipo-1.png" alt="Alt for image" caption="prueba" %}
Aqui debemos ingresar los datos del nuevo usuario como *Nombres*, *Apellidos*, *Roles*, *Correo electrónico* y *Contraseña*.
{% include image.html img="../docs/temas/usuarios/equipo/crear-equipo-2.jpg" alt="Alt for image" caption="prueba" %}

A

## Editar usuario
Una vez que el usuario se encuentra creado, tendremos la opción de editarlo, como se muestra en la imágen.
{% include image.html img="../docs/temas/usuarios/equipo/editar-equipo-1.png" alt="Alt for image" caption="prueba" %}
Nos dirige a la sección **General**, aqui aparecera la información actualmente del usuario asi como sus roles.
{% include image.html img="../docs/temas/usuarios/equipo/editar-equipo-2.jpeg" alt="Alt for image" caption="prueba" %}
Cuando vayamos a la sección **Roles**, aqui aparecera todos los roles que puede tener el usuario 
ademas de poder añadir o quitar roles al usuario con tan solo dar click a la casilla. Si sale 
seleccionada la casilla quiere decir que el usuario posee ese rol y sino aparece seleccionado quiere 
decir que no posee ese rol.
{% include image.html img="../docs/temas/usuarios/equipo/editar-equipo-3.png" alt="Alt for image" caption="prueba" %}

## Eliminar usuario
Para eliminar un usuario haremos los mismos pasos para editar usuario y cuando vemos la informacion del usuario, nos saldra un boton para eliminar al usuario.
{% include image.html img="../docs/temas/usuarios/equipo/eliminar-equipo.png" alt="Alt for image" caption="prueba" %}


## Buscar usuario
Si queremos buscar un usuario podemos hacerlo por su **Correo Electrónico** o su **ID legal**.
{% include image.html img="../docs/temas/usuarios/equipo/buscar-equipo-1.png" alt="Alt for image" caption="prueba" %}

## Descargar usuarios
Si queremos descargar todos los usuarios, en formato Excel, tenemos una opcion **Iniciar descarga**.
{% include image.html img="../docs/temas/usuarios/equipo/descarga-equipo-1.png" alt="Alt for image" caption="prueba" %}

