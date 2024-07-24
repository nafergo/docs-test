---
title: Equipo
subtitle: 
tags: [crear_usuario]
author: ivan
---

Antes de pasar a la explicacion de como crear un usuario y sus respectivos roles que tendra, explicaremos cada rol.
## Roles:

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

## Crear usuario
Para crear un nuevo usuario, vamos a la opción de **Equipo** y luego **Crear usuario**
{% include image.html img="../docs/temas/usuarios/equipo/crear-equipo-merchant-1.png" alt="Alt for image" caption="prueba" %}
Aqui debemos ingresar los datos del nuevo usuario como *Nombres*, *Apellidos*, *Roles*, *Correo electrónico* y *Contraseña*.
{% include image.html img="../docs/temas/usuarios/equipo/crear-equipo-merchant-2.png" alt="Alt for image" caption="prueba" %}

## Editar usuario
Una vez que el usuario se encuentra creado, tendremos la opción de editarlo, como se muestra en la imágen.
{% include image.html img="../docs/temas/usuarios/equipo/editar-equipo-merchant-1.png" alt="Alt for image" caption="prueba" %}
Nos dirige a la sección **General**, aqui aparecera la información actualmente del usuario asi como sus roles.
{% include image.html img="../docs/temas/usuarios/equipo/editar-equipo-merchant-2.png" alt="Alt for image" caption="prueba" %}
Cuando vayamos a la sección **Roles**, aqui aparecera todos los roles que puede tener el usuario 
ademas de poder añadir o quitar roles al usuario con tan solo dar click a la casilla. Si sale 
seleccionada la casilla quiere decir que el usuario posee ese rol y sino aparece seleccionado quiere 
decir que no posee ese rol.
{% include image.html img="../docs/temas/usuarios/equipo/editar-equipo-merchant-3.png" alt="Alt for image" caption="prueba" %}

## Eliminar usuario
Para eliminar un usuario haremos los mismos pasos para editar usuario y cuando vemos la informacion del usuario, nos saldra un boton para eliminar al usuario.
{% include image.html img="../docs/temas/usuarios/equipo/eliminar-equipo-merchant.png" alt="Alt for image" caption="prueba" %}

## Buscar usuario
Si queremos buscar un usuario podemos hacerlo por su **Correo Electrónico** o su **ID legal**.
{% include image.html img="../docs/temas/usuarios/equipo/buscar-equipo-1.png" alt="Alt for image" caption="prueba" %}

## Descargar usuarios
Si queremos descargar todos los usuarios, en formato Excel, tenemos una opcion **Iniciar descarga**.
{% include image.html img="../docs/temas/usuarios/equipo/descarga-equipo-1.png" alt="Alt for image" caption="prueba" %}

