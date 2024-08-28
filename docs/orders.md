<p align="center"><a href="https://app.papeleralamilagrosa.com.ar" target="_blank"><img src="https://app.papeleralamilagrosa.com.ar/images/logo.jpg" width="240"></a></p>

<p style="text-align: right;">
  <a href="../README.md">HOME</a>
</p>

## Módulo de Pedidos

#### Acciones CRUD
##### Crear registros
Nombre       |Alias                   |Permisos disponibles|Dependencias
--           |-                       |-                   |-
create-new   |Crear nuevo pedido      |rwx                 |users.search-all (opc.)
create-queued|Crear nueva reserva fija|rwx                 |orders.create-new

##### Mostrar registros
Nombre             |Alias             |Permisos disponibles|Dependencias
--                 |-                 |-                   |-
list-all           |Ver Todos         |r--                 |-
list-order_status-1|Ver Pendientes    |r--                 |-
list-order_status-2|Ver Actualizados  |r--                 |-
list-order_status-3|Ver Confirmados   |r--                 |-
list-order_status-4|Ver En reparto    |r--                 |-
list-order_status-5|Ver A retirar     |r--                 |-
list-order_status-6|Ver Finalizados   |r--                 |-
list-order_status-7|Ver Cancelados    |r--                 |-
list-order_status-8|Ver Entregados    |r--                 |-
list-queued        |Ver Reservas fijas|r--                 |-

##### Editar registros
Nombre                  |Alias                                        |Permisos disponibles|Dependencias
--                      |-                                            |-                   |-
edit                    |Editar pedido                                |rw-                 |catalog.list-all
edit-queued             |Editar reserva fija                          |-w-                 |orders.list-queued, orders.edit
note                    |Agregar nota al pedido                       |-w-                 |-
set-coil-price          |Agregar el valor de las bobinas              |-w-                 |orders.edit
set-delivery-note       |Agregar el número de remito                  |-w-                 |orders.edit
set-order_status-7      |Marcar orden como cancelada                  |-w-                 |orders.edit, orders.delete
set-weight              |Agregar el peso de las bobinas               |-w-                 |orders.edit
update-addr_status-1    |Actualizar dirección de un pedido pendiente  |-w-                 |orders.list-order_status-1, orders.edit
update-addr_status-2    |Actualizar dirección en un pedido actualizado|-w-                 |orders.list-order_status-2, orders.edit, schedules.update
update-addr_status-3    |Actualizar dirección en un pedido confirmado |-w-                 |orders.list-order_status-3, orders.edit, schedules.update
update-addr_status-4    |Actualizar dirección en un pedido despachado |-w-                 |orders.list-order_status-4, orders.edit, schedules.update,trips.update
update-addr_status-5    |Actualizar dirección en un pedido a retirar  |-w-                 |orders.list-order_status-5, orders.edit, orders.update-order_status-4to5 (opc.)
update-addr_status-6    |Actualizar dirección en un pedido finalizado |-w-                 |orders.list-order_status-6, orders.edit
update-addr_status-7    |Actualizar dirección en un pedido entregado  |-w-                 |orders.list-order_status-7, orders.edit
update-coil-price       |Agregar el valor de las bobinas              |-w-                 |orders.edit
update-order_status-1to2|Actualizar pedido pendiente                  |--x                 |orders.list-order_status-1, orders.edit, schedules.update
update-order_status-2to1|Devolver pedido a pendiente                  |--x                 |orders.list-order_status-2, orders.edit, schedules.update
update-order_status-2to3|Confirmar pedido actualizado                 |--x                 |orders.list-order_status-2, orders.edit, schedules.update
update-order_status-3to2|Cancelar confirmación de pedido              |--x                 |orders.list-order_status-3, orders.edit, schedules.update
update-order_status-3to4|Despachar pedido                             |--x                 |orders.list-order_status-3, orders.edit, schedules.update, trips.create-new, trips.update
update-order_status-3to5|Disponibilizar pedido para retirar           |--x                 |orders.list-order_status-3, orders.edit, schedules.update
update-order_status-4to3|Devolver pedido despachado                   |--x                 |orders.list-order_status-4, orders.edit, schedules.update
update-order_status-4to5|Cambiar pedido a entregar a retirar          |--x                 |orders.list-order_status-4, orders.edit, schedules.update
update-order_status-5to3|Reagendar pedido para retirar                |--x                 |orders.list-order_status-5, orders.edit, schedules.update
update-order_status-5to4|Cambiar pedido para retirar a entrega        |--x                 |orders.list-order_status-5, orders.edit, schedules.update
update-order_status-5to6|Finalizar pedido                             |--x                 |orders.list-order_status-5, orders.edit, trips.update
update-order_status-6to8|Marcar pedido como entregado                 |--x                 |orders.list-order_status-6, orders.edit, trips.update
update-weight           |Actualizar el peso de una bobina             |-w-                 |orders.edit

##### Eliminar registros
Nombre       |Alias                |Permisos disponibles|Dependencias
--           |-                    |-                   |-
delete       |Eliminar pedido      |-w-                 |-
delete-queued|Eliminar reserva fija|-w-                 |-

#### Otras acciones
##### Mostrar resúmenes
Nombre                     |Alias                      |Permisos disponibles|Dependencias
--                         |-                          |-                   |-
show-summary-all           |Ver resumen de Todos       |r--                 |-
show-summary-order_status-1|Ver resumen de Pendientes  |r--                 |-
show-summary-order_status-2|Ver resumen de Actualizados|r--                 |-
show-summary-order_status-3|Ver resumen de Confirmados |r--                 |-
show-summary-order_status-4|Ver resumen de En reparto  |r--                 |-
show-summary-order_status-5|Ver resumen de A retirar   |r--                 |-
show-summary-order_status-6|Ver resumen de Finalizados |r--                 |-
show-summary-order_status-7|Ver resumen de Cancelados  |r--                 |-
show-summary-order_status-8|Ver resumen de Entregados  |r--                 |-
show-summary-queued        |Ver resumen de Reserva Fija|r--                 |-

##### Mostrar detalles
Nombre             |Alias                |Permisos disponibles|Dependencias
--                 |-                    |-                   |-
show-order-detail  |Ver detalle          |rwx                 |-
show-order-extended|Ver detalle extendido|rwx                 |-

##### Buscar registros
Nombre               |Alias                      |Permisos disponibles|Dependencias
--                   |-                          |-                   |-
search-all           |Buscar pedidos             |r-x                 |-
search-order_status-1|Buscar pedidos Pendientes  |r-x                 |-
search-order_status-2|Buscar pedidos Actualizados|r-x                 |-
search-order_status-3|Buscar pedidos Confirmados |r-x                 |-
search-order_status-4|Buscar pedidos En reparto  |r-x                 |-
search-order_status-5|Buscar pedidos A retirar   |r-x                 |-
search-order_status-6|Buscar pedidos Finalizados |r-x                 |-
search-order_status-7|Buscar pedidos Cancelados  |r-x                 |-
search-order_status-8|Buscar pedidos Entregados  |r-x                 |-

##### Imprimir registros
Nombre              |Alias                |Permisos disponibles|Dependencias
--                  |-                    |-                   |-
print-all           |Imprimir Todos       |r-x                 |-
print-order         |Imprimir Orden       |r-x                 |-
print-order_status-1|Imprimir Pendientes  |r-x                 |-
print-order_status-2|Imprimir Actualizados|r-x                 |-
print-order_status-3|Imprimir Confirmados |r-x                 |-
print-order_status-4|Imprimir En reparto  |r-x                 |-
print-order_status-5|Imprimir A retirar   |r-x                 |-
print-order_status-6|Imprimir Finalizados |r-x                 |-
print-order_status-7|Imprimir Cancelados  |r-x                 |-
print-order_status-8|Imprimir Entregados  |r-x                 |-

##### Acciones varias
Nombre     |Alias                               |Permisos disponibles|Dependencias
--         |-                                   |-                   |-
phone-call |LLamar al teléfono del cliente      |--x                 |users.list-rol-2
send-email |Enviar correo al cliente            |--x                 |users.list-rol-2
map-address|Ver dirección del cliente en el mapa|--x                 |users.list-rol-2
