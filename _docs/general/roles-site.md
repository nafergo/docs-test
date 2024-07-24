---
title: Roles site
subtitle: Permisos y funcionalidades por rol.
tags: [general, Roles_site]
author: Luis Zumaeta
---
Esta sección tiene como propósito la descripción de los roles ya que son clave para que tengamos una plataforma segura y predecible. Los roles Site están disponibles para sitios **Singleplace** y **Marketplace**.

Gestionar todo en un marketplace puede ser un poco caótico. Es por ello que se brindan los siguientes roles según la necesidad de permisos para delegar correctamente las responsabilidades.

Todos los roles disponibles responden a una jerarquía. El Rol *SiteAdmin* responde a una jerarquía superior frente a todos los demas roles *Sites* y *Merchants*. A diferencia de los `roles merchant`, los `roles site` poseen una jerarquía adicional para diferenciar tener un mayor control por cada rol.

Por ejemplo:
- `Un rol SiteCMSAdmin tendrá una jerarquía superior al SiteCMS`
- `Un rol SiteSaleAdmin tendrá una jerarquía superior al SiteSale`
- `Un rol SitFinanceAdmin tendrá una jerarquía superior al SiteFinance`

Los roles que posean una jerarquía superior a otro rol, obtendrá los permisos del rol inferior pero no viceversa. Esto permite una correcta distribución de responsabilidades a lo largo de las funcionalidades de la plataforma. El rol *SiteAdmin* es el rol de más alta jerarquía, por ende heredará los permisos de todos los demás roles Sites.

## Roles disponibles como SiteOwner:

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
