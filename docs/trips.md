<p align="center"><a href="https://app.papeleralamilagrosa.com.ar" target="_blank"><img src="https://app.papeleralamilagrosa.com.ar/images/logo.jpg" width="240"></a></p>

<p style="text-align: right;">
  <a href="../README.md">HOME</a>
</p>

## Módulo de Envíos

#### Acciones CRUD
##### Crear registros
Nombre           |Alias             |Permisos disponibles|Dependencias
--               |-                 |-                   |-
create-new       |Crear nuevo envío |--x                 |-
create-new-driver|Crear nuevo chofer|rwx                 |-

##### Mostrar registros
Nombre            |Alias          |Permisos disponibles|Dependencias
--                |-              |-                   |-
list-all          |Ver Todos      |r--                 |-
list-drivers-all  |Ver Coferes    |r--                 |-
list-trip_status-1|Ver Preparados |r--                 |-
list-trip_status-2|Ver En curso   |r--                 |-
list-trip_status-3|Ver Finalizados|r--                 |-

##### Editar registros
Nombre            |Alias          |Permisos disponibles|Dependencias
--                |-              |-                   |-
edit-driver       |Editar chofer  |rw-                 |-

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
