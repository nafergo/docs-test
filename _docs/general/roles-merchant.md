---
title: Roles merchant
subtitle: Permisos y funcionalidades por rol.
tags: [general, Roles_merchant]
author: Luis Zumaeta
---
Esta sección tiene como propósito la descripción de los roles ya que son clave para que tengamos una plataforma segura y predecible. Los roles Merchant solo están disponibles para sitios **marketplace**.

Gestionar todo el flujo de catálogo, contenido y distribución puede requerir más de un perfil. Es por ello que se brindan los siguientes roles según la necesidad de permisos.

Todos los roles disponibles responden a una jerarquía. El Rol *MerchantAdmin* responde a una jerarquía superior frente a todos los demas roles merchant, por ende hereda todos los permisos de sus roles inferiores. Los demás roles merchant se encuentran a un mismo nivel pero con permisos diferentes.

## Roles disponibles como Merchant/Seller:

### **MerchantAdmin:** 
Es el dueño o administrador responsable de la empresa o negocio Merchant/Seller.

Este usuario posee todos los permisos para la configuración de una tienda. Puede realizar todas las funcionalidades de los otros roles. 

Las funcionalidades **únicas** a diferencia de otros roles son:
- Creación, edición y eliminación de usuarios para el equipo.
- Configuración de notificaciones a los correos destinatarios.
- Gestión de integraciones.

### **MerchantSale:** 
Persona responsable de la venta o marketing de productos. Puede ser responsable de la atención de la venta como un cajero, un ejecutivo comercial o un analista en marketing.

Las principales funciones que posee son:
- Visualizar el dashboard de ventas.
- Encender o apagar la tienda que tiene a cargo.
- Gestionar pedidos.

### **MerchantCatalog:** 
Persona responsable del catálogo de producto. Principalmente cuida que el detalle de producto esté actualizado para no infringir normas o incluso ser más estratégico en la venta.

Las principales funciones que posee son:
- Modificar configuraciones de la tienda.
- Crear, editar o eliminar cualquier característica del producto del catálogo.
- Gestionar el stock de productos.

### **MerchantCMS:** 
Persona a cargo del contenido de la página del Merchant. Puede ser un diseñador

Las principales funciones que posee son:
- Gestionar el contenido de la página principal de la tienda.

### **MerchantLogistic:** 
Persona a cargo de la preparación, distribución y del inventario del producto. Puede ser un almacenero.

Las principales funciones que posee son:
- Encender o apagar la tienda que tiene a cargo.
- Modificar el stock de cada producto del catálogo.
- Gestionar pedidos.

## Combinación de roles

Los roles pueden ser sleecionados en `combo`, eso quiere decir que un usuario puede tener muchos roles asignados.

Por ejemplo:
- `Un usuario puede tener los roles MerchantSale y MerchantCatalog`
- `Un usuario puede tener los roles MerchantSale, MerchantCatalog y MerchantLogistic`
- `Un usuario puede tener los roles MerchantCMS y MerchantCatalog`

Esto permite que las características principales de cada rol puedan ser asignadas a un mismo usuario para distribuir la carga o responsabilidades.
