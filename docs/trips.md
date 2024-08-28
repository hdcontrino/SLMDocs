<p align="center"><a href="https://app.papeleralamilagrosa.com.ar" target="_blank"><img src="https://app.papeleralamilagrosa.com.ar/images/logo.jpg" width="240"></a></p>

<p style="text-align: right;">
  <a href="../README.md">HOME</a>
</p>

## Módulo de Envíos

#### Acciones CRUD
##### Crear registros
Nombre            |Alias                 |Permisos disponibles|Dependencias
--                |-                     |-                   |-
create-new        |Crear nuevo envío     |--x                 |-
create-new-city   |Crear nueva ciudad    |rwx                 |-
create-new-courier|Crear nuevo transporte|rwx                 |-
create-new-driver |Crear nuevo chofer    |rwx                 |-

##### Mostrar registros
Nombre            |Alias          |Permisos disponibles|Dependencias
--                |-              |-                   |-
list-all          |Ver Todos      |r--                 |-
list-cities       |Ver ciudades   |r--                 |-
list-couriers     |Ver transportes|r--                 |-
list-drivers-all  |Ver Coferes    |r--                 |-
list-trip_status-1|Ver Preparados |r--                 |-
list-trip_status-2|Ver En curso   |r--                 |-
list-trip_status-3|Ver Finalizados|r--                 |-

##### Editar registros
Nombre            |Alias                 |Permisos disponibles|Dependencias
--                |-                     |-                   |-
edit-city         |Editar ciudad         |rw-                 |-
edit-courier      |Editar transporte     |rw-                 |-
edit-driver       |Editar chofer         |rw-                 |-
parcial-delivery  |Marcar entrega parcial|-w-                 |orders.note, orders.edit
set-delivery-note |Editar remito         |rw-                 |orders.set-delivery-note

##### Eliminar registros
Nombre        |Alias              |Permisos disponibles|Dependencias
--            |-                  |-                   |-
delete        |Cancelar envío     |-w-                 |-
delete-city   |Eliminar ciudad    |-w-                 |-
delete-courier|Eliminar transporte|-w-                 |-
delete-driver |Eliminar chofer    |-w-                 |-

#### Otras acciones
##### Mostrar resúmenes
Nombre                    |Alias                     |Permisos disponibles|Dependencias
--                        |-                         |-                   |-
show-summary-all          |Ver resumen de Todos      |r--                 |-
show-summary-trip_status-1|Ver resumen de Preparados |r--                 |-
show-summary-trip_status-2|Ver resumen de En curso   |r--                 |-
show-summary-trip_status-3|Ver resumen de Finalizados|r--                 |-

##### Mostrar detalles
Nombre           |Alias                |Permisos disponibles|Dependencias
--               |-                    |-                   |-
show-order-detail|Ver detalle de pedido|r--                 |orders.show-order-extended
show-trip-detail |Ver detalle de Envío |rwx                 |orders.list-all

##### Buscar registros
Nombre     |Alias        |Permisos disponibles|Dependencias
--         |-            |-                   |-
search-all |Buscar envíos|r--                 |orders.search-all

##### Imprimir registros
Nombre       |Alias                |Permisos disponibles|Dependencias
--           |-                    |-                   |-
print-all    |Imprimir Todos       |r-x                 |-
print-setted |Imprimir preparados  |r-x                 |-
print-trip   |Imprimir envío       |r-x                 |-