---
title: Opciones de pago
subtitle: Las opciones de pagos son las posibilidades brindadas al usuario para concretar la venta.
tags: [opciones,pagos]
author: Luis Zumaeta
---

Cada vez que un cliente se dispone a pagar por su compra, este seleccionará algún metodo de pago (Tarjeta de crédito, Pago con transferencia, Pago en efectivo, Confirmación de código, etc), aqui veremos como realizar esa configuración.

## Crear nueva opción de pago
Para crear una nueva opción de pago solo debemos seleccionar la opción **Opciones de pago**, a continuación **Crear opción de pago** y seguir los siguientes pasos:

### Obligatorios
- **Nombre de la opción de pago:** Este será el nombre reflejado en las opciones del cliente.
- **Número de orden:** Es el ordenamiento preferido de las opciones de pago habilitadas.
- **Método de pago:** Es el tipo de método de pago utilizado en la **creación del proveedor de pago** (Este campo **no podrá ser editado a futuro**).
- **Operación de pago por defecto:** Es la operación designada según el método de pago.
- **Proveedores de pago:** Es la lista disponible de los proveedores a utilizar para la opción de pago.

### Opcionales
- **Descripción:** Es un texto de hasta 1000 caracteres que hace referencia a la explicación de la opción de pago para guiar al usuario.
- **Instrucciones:** Es un texto de hasta 1000 caracteres que hace referencia a las instrucciones a guiar al usuario para completar el pago.

Todas las opciones de pago nuevas se crean **Inhabilitadas**.

## Editar opción de pago

Al editar una opción de pago se podrán editar todos los campos **excepto** el método de pago.

Adicionalmente se tienen las opciones:
- **Habilitar**: Opción que permite Habilitar o Deshabilitar temporalmente una opción de pago.
- **Eliminar**: Opción que permite la eliminación del registro de la opción de pago (Esta opción **no puede ser revertida**).
