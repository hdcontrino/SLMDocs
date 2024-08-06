<p align="center"><a href="https://app.papeleralamilagrosa.com.ar" target="_blank"><img src="https://app.papeleralamilagrosa.com.ar/images/logo.jpg" width="240"></a></p>

<p style="text-align: right;">
  <a href="../README.md">HOME</a>
</p>

## Módulo de Pedidos

#### Acciones CRUD
##### Crear registros
Nombre    |Alias             |Permisos disponibles|Dependencias
--        |-                 |-                   |-
create-new|Crear nuevo pedido|rwx                 |users.search-all (opc.)

##### Mostrar registros
Nombre             |Alias           |Permisos disponibles|Dependencias
--                 |-               |-                   |-
list-all           |Ver Todos       |r--                 |-
list-order_status-1|Ver Pendientes  |r--                 |-
list-order_status-2|Ver Actualizados|r--                 |-
list-order_status-3|Ver Confirmados |r--                 |-
list-order_status-4|Ver En reparto  |r--                 |-
list-order_status-5|Ver A retirar   |r--                 |-
list-order_status-6|Ver Finalizados |r--                 |-
list-order_status-7|Ver Entregados  |r--                 |-

##### Editar registros
Nombre                  |Alias                                |Permisos disponibles|Dependencias
--                      |-                                    |-                   |-
edit                    |Editar pedido                        |rw-                 |catalog.list-all
note                    |Agregar nota al pedido               |-w-                 |-
update-order_status-1to2|Actualizar pedido pendiente          |--x                 |schedules.update
update-order_status-2to1|Devolver pedido a pendiente          |--x                 |schedules.update
update-order_status-2to3|Confirmar pedido actualizado         |--x                 |schedules.update
update-order_status-3to2|Cancelar confirmación de pedido      |--x                 |schedules.update
update-order_status-3to4|Despachar pedido                     |--x                 |schedules.update, trips.create-new, trips.update
update-order_status-3to5|Disponibilizar pedido para retirar   |--x                 |schedules.update
update-order_status-4to3|Devolver pedido despachado           |--x                 |schedules.update
update-order_status-4to5|Cambiar pedido a entregar a retirar  |--x                 |schedules.update
update-order_status-5to3|Reagendar pedido para retirar        |--x                 |schedules.update
update-order_status-5to4|Cambiar pedido para retirar a entrega|--x                 |schedules.update
update-order_status-5to6|Finalizar pedido                     |--x                 |trips.update

##### Eliminar registros
Nombre|Alias          |Permisos disponibles|Dependencias
--    |-              |-                   |-
delete|Eliminar pedido|-w-                 |-

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
show-summary-order_status-7|Ver resumen de Entregados  |r--                 |-

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
search-order_status-7|Buscar pedidos Entregados  |r-x                 |-

##### Imprimir registros
Nombre              |Alias                |Permisos disponibles|Dependencias
--                  |-                    |-                   |-
print               |Imprimir Orden       |r-x                 |-
print-all           |Imprimir Todos       |r-x                 |-
print-order_status-1|Imprimir Pendientes  |r-x                 |-
print-order_status-2|Imprimir Actualizados|r-x                 |-
print-order_status-3|Imprimir Confirmados |r-x                 |-
print-order_status-4|Imprimir En reparto  |r-x                 |-
print-order_status-5|Imprimir A retirar   |r-x                 |-
print-order_status-6|Imprimir Finalizados |r-x                 |-
print-order_status-7|Imprimir Entregados  |r-x                 |-
