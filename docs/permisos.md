<p align="center"><a href="https://app.papeleralamilagrosa.com.ar" target="_blank"><img src="https://app.papeleralamilagrosa.com.ar/images/logo.jpg" width="240"></a></p>

<p style="text-align: right;">
  <a href="../README.md">HOME</a>
</p>

## Roles y Permisos
El SLM trabaja los permisos de los usuarios por medio del acceso que sus roles les dan a cada uno de los espacios disponibles.
La base de los permisos se administra de acuerdo a tres instancias:
- \- (none): el usuario no tiene ningún tipo de acceso.
- r (read): permite ver el contenido del espacio.
- w (write): permite guardar o modificar información que el espacio muestra.
- x (execute): permite ejecutar tareas o funciones específicas.

En la base de datos se guardarán estos permisos bajo representación octal. Cada uno de los permisos se representa numéricamente:

- Lectura (r) tiene un valor de 4.
- Escritura (w) tiene un valor de 2.
- Ejecución (x) tiene un valor de 1.

Los valores para cada categoría se suman para obtener un número octal:

- r-- (lectura solamente) = 4
- rw- (lectura y escritura) = 4 + 2 = 6
- rwx (lectura, escritura y ejecución) = 4 + 2 + 1 = 7

Cada rol de usuario dentro del SLM puede tener acceso de lectura (r) o de escritura (w) a distintos módulos a través de las vistas que tienen asignados. A su vez, cada elemento dentro del módulo podrá requerir, también, los mismos permisos, como así también permiso de ejecución (x).


#### Roles
##### Módulos predeterminados
Cada rol tiene una vista y un módulo predeterminado que se mostrará al ingresar a la interfaz. Esta característica es personalizable para la aplicación aunque la versión actual del SLM no poseé aún una vista de configuración de usuario donde pueda controlarse este comportamiento.

Nombre   |Layout |Módulo   |Vista
--       |-      |-        |-
admin    |private|orders   |`resources/views/panels/orders.blade.php`
collector|private|orders   |`resources/views/panels/orders.blade.php`
control  |private|schedules|`resources/views/panels/schedules.blade.php`
customer |private|catalogs |`resources/views/panels/catalog-customer.blade.php`
depot    |private|schedules|`resources/views/panels/schedules.blade.php`
public   |public |login    |`resources/views/auth/login.blade.php`
sales    |private|orders   |`resources/views/panels/orders.blade.php`

##### Permisos de módulos
Cada rol tiene configurado el acceso a los módulos a través del modelo `app/Models/PanelRole.php`. En la siguiente tabla se detallan los permisos configurados actualmente.

Nombre   |Módulo   |Permisos
--       |-        |-
admin    |orders   |rw-
admin    |schedules|rw-
admin    |trips    |rw-
admin    |catalogs |rw-
admin    |products |rw-
admin    |users    |rw-
admin    |reports  |rw-
customer |orders   |---
customer |schedules|---
customer |trips    |---
customer |catalogs |rw-
customer |products |---
customer |users    |---
customer |reports  |---
collector|orders   |rw-
collector|schedules|r--
collector|trips    |rw-
collector|catalogs |rw-
collector|products |rw-
collector|users    |---
collector|reports  |---
control  |orders   |rw-
control  |schedules|r--
control  |trips    |rw-
control  |catalogs |---
control  |products |---
control  |users    |---
control  |reports  |---
sales    |orders   |rw-
sales    |schedules|rw-
sales    |trips    |r--
sales    |catalogs |rw-
sales    |products |rw-
sales    |users    |rw-
sales    |reports  |---
schedules|orders   |---
schedules|schedules|rw-
schedules|trips    |rw-
schedules|catalogs |---
schedules|products |---
schedules|users    |---
schedules|reports  |---

#### Permisos de escritura y ejecución
[Agenda](schedules.md)|[Carrito](cart.md)|[Envíos](trips.md)        |[Informes](reports.md)
--                    |-                 |-                         |-
assign                |add-item          |create-new                |create-new
assign-to-trip        |create-new        |create-new-city           |export-current
assignment            |del-item          |create-new-courier        |export-report 
create-new            |edit              |create-new-driver         |list-saved
driver                |export-catalog    |delete                    |print-current
edit-driver           |set-delay         |delete-city               |print-report 
list-assigned         |show-cart         |delete-courier            |search-all
list-compact          |show-catalog      |delete-driver             |show-report-detail
list-history          |show-history      |edit-city                 |show-summary-saved
list-unassigned       |                  |edit-courier              |
move-order            |                  |edit-driver               |
move-trip             |                  |list-all                  |
phone-call            |                  |list-cities               |
print                 |                  |list-couriers             |
remove-from-trip      |                  |list-drivers-all          |
remove-trip           |                  |list-trip_status-1        |
search-all            |                  |list-trip_status-2        |
send-trip             |                  |list-trip_status-3        |
set-trip              |                  |parcial-delivery          |
show-drivers          |                  |print-all                 |
show-order-detail     |                  |print-setted              |
show-trip-detail      |                  |print-trip                |
unassign              |                  |search-all                |
update                |                  |set-delivery-note         |
|                     |                  |show-summary-all          |
|                     |                  |show-summary-trip_status-1|
|                     |                  |show-summary-trip_status-2|
|                     |                  |show-summary-trip_status-3|
|                     |                  |show-order-detail         |
|                     |                  |show-trip-detail          |

[Listas](catalogs.md)|[Pedidos](orders.md)       |[Productos](products.md)   |[Usuarios](users.md)
--                   |-                          |-                          |-
create-new           |create-new                 |create-new                 |create-new
delete               |create-queued              |delete                     |delete         
del-product          |delete                     |edit                       |delete-customer
edit                 |delete-queued              |export-all                 |edit         
edit-level           |edit                       |export-product_type-1      |edit-customer
export-all           |edit-queued                |export-product_type-2      |hide-user 
export-catalog       |list-all                   |hide-product               |list-all  
hide-catalog         |list-order_status-1        |import-all                 |list-rol-1
import-all-prices    |list-order_status-2        |import-product_type-1      |list-rol-2
import-catalog-prices|list-order_status-3        |import-product_type-2      |list-rol-3
list                 |list-order_status-4        |list-all                   |list-rol-4
list-all             |list-order_status-5        |list-product_type-1        |list-rol-5
search-all           |list-order_status-6        |list-product_type-2        |list-rol-6
set-fixed-price      |list-order_status-7        |search-all                 |search-all  
set-product          |list-order_status-8        |set-fixed-price            |search-rol-1
show-catalog         |list-queued                |set-product-prices         |search-rol-2
show-product         |map-address                |show-product               |search-rol-3
show-product-detail  |note                       |show-product-detail        |search-rol-4
show-summary-all     |phone-call                 |show-summary-all           |search-rol-5
|                    |print-all                  |show-summary-product_type-1|search-rol-6
|                    |print-order                |show-summary-product_type-2|send-pwd-recovery
|                    |print-order_status-1       |                           |set-address      
|                    |print-order_status-2       |                           |set-catalog      
|                    |print-order_status-3       |                           |share-pwd-recovery
|                    |print-order_status-4       |                           |show-profile
|                    |print-order_status-5       |                           |show-summary-all  
|                    |print-order_status-6       |                           |show-summary-rol-1
|                    |print-order_status-7       |                           |show-summary-rol-2
|                    |print-order_status-8       |                           |show-summary-rol-3
|                    |search-all                 |                           |show-summary-rol-4
|                    |search-order_status-1      |                           |show-summary-rol-5
|                    |search-order_status-2      |                           |show-summary-rol-6
|                    |search-order_status-3      |                           |show-user
|                    |search-order_status-4      |                           |show-user-detail
|                    |search-order_status-5      |                           |
|                    |search-order_status-6      |                           |
|                    |search-order_status-7      |                           |
|                    |search-order_status-8      |                           |
|                    |send-email                 |                           |
|                    |set-coil-price             |                           |
|                    |set-delivery-note          |                           |
|                    |set-order_status-7         |                           |
|                    |set-weight                 |                           |
|                    |show-order-detail          |                           |
|                    |show-order-extended        |                           |
|                    |show-summary-all           |                           |
|                    |show-summary-order_status-1|                           |
|                    |show-summary-order_status-2|                           |
|                    |show-summary-order_status-3|                           |
|                    |show-summary-order_status-4|                           |
|                    |show-summary-order_status-5|                           |
|                    |show-summary-order_status-6|                           |
|                    |show-summary-order_status-7|                           |
|                    |show-summary-order_status-8|                           |
|                    |show-summary-queued        |                           |
|                    |update-addr_status-1       |                           |
|                    |update-addr_status-2       |                           |
|                    |update-addr_status-3       |                           |
|                    |update-addr_status-4       |                           |
|                    |update-addr_status-5       |                           |
|                    |update-order_status-4to5   |                           |
|                    |update-addr_status-6       |                           |
|                    |update-addr_status-7       |                           |
|                    |update-coil-price          |                           |
|                    |update-order_status-1to2   |                           |
|                    |update-order_status-2to1   |                           |
|                    |update-order_status-2to3   |                           |
|                    |update-order_status-3to2   |                           |
|                    |update-order_status-3to4   |                           |
|                    |update-order_status-3to5   |                           |
|                    |update-order_status-4to3   |                           |
|                    |update-order_status-4to5   |                           |
|                    |update-order_status-5to3   |                           |
|                    |update-order_status-5to4   |                           |
|                    |update-order_status-5to6   |                           |
|                    |update-order_status-6to8   |                           |
|                    |update-weight              |                           |
