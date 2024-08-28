<p align="center"><a href="https://app.papeleralamilagrosa.com.ar" target="_blank"><img src="https://app.papeleralamilagrosa.com.ar/images/logo.jpg" width="240"></a></p>

<p style="text-align: right;">
  <a href="../README.md">HOME</a>
</p>

## Módulo de Agenda

#### Acciones CRUD
##### Crear registros
Nombre    |Alias             |Permisos disponibles|Dependencias
--        |-                 |-                   |-
create-new|Crear nuevo día   |rwx                 |-

##### Mostrar registros
Nombre         |Alias          |Permisos disponibles|Dependencias
--             |-              |-                   |-
list-assigned  |Ver Asignados  |r--                 |-
list-compact   |Ver Calendario |r--                 |-
list-history   |Ver Anteriores |r--                 |-
list-unassigned|Ver Sin asignar|r--                 |-

##### Editar registros
Nombre          |Alias                    |Permisos disponibles|Dependencias
--              |-                        |-                   |-
assign          |Añadir pedido            |-w-                 |schedules.update
assign-to-trip  |Añadir pedido a un envío |-w-                 |schedules.assing
assignment      |Añadir grupo por asignar |-w-                 |-
driver          |Añadir chofer a la agenda|-w-                 |trips.list-drivers-all
edit-driver     |Editar datos del chofer  |rw-                 |trips.edit-driver
move-order      |Mover un pedido          |-w-                 |schedules.update, orders.edit
move-trip       |Mover un envío           |-w-                 |schedules.update, trips.edit
remove-from-trip|Preparar un envío        |-w-                 |schedules.update, trips.edit
remove-trip     |Cancelar un envío        |-w-                 |schedules.update, trips.delete
set-trip        |Preparar un envío        |-w-                 |trips.create-new
send-trip       |Despachar un envío       |-w-                 |schedules.update, trips.edit
unassign        |Desasignar un pedido     |-w-                 |schedules.update
update          |Actualizar elemento      |-w-                 |

#### Otras acciones
##### Mostrar detalles
Nombre           |Alias                |Permisos disponibles|Dependencias
--               |-                    |-                   |-
show-drivers     |Ver choferes         |r--                 |trips.list-drivers-all
show-order-detail|Ver detalle de pedido|r--                 |orders.show-order-extended
show-trip-detail |Ver detalle de envío |r--                 |orders.show-order-extended

##### Buscar registros
Nombre    |Alias           |Permisos disponibles|Dependencias
--        |-               |-                   |-
search-all|Buscar en agenda|r-x                 |orders.search-all, trips.search-all

##### Imprimir registros
Nombre   |Alias                  |Permisos disponibles|Dependencias
--       |-                      |-                   |-
print    |Imprimir agenda del día|r-x                 |orders.list-all

##### Acciones varias
Nombre     |Alias                        |Permisos disponibles|Dependencias
--         |-                            |-                   |-
phone-call |LLamar al teléfono del chofer|--x                 |users.list-rol-2
