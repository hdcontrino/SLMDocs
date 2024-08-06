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
Nombre         |Alias                       |Permisos disponibles|Dependencias
--             |-                           |-                   |-
assignment     |Añadir grupo por asignar    |rw-                 |-
driver         |Añadir chofer a la agenda   |rw-                 |trips.list-drivers-all
edit-driver    |Editar datos del chofer     |rw-                 |trips.edit-driver

#### Otras acciones
##### Mostrar detalles
Nombre           |Alias       |Permisos disponibles|Dependencias
--               |-           |-                   |-
show-drivers     |Ver choferes|r--                 |trips.list-drivers-all
show-order-detail|Ver detalle |r--                 |orders.show-order-extended

##### Buscar registros
Nombre    |Alias           |Permisos disponibles|Dependencias
--        |-               |-                   |-
search-all|Buscar en agenda|r-x                 |orders.search-all

##### Imprimir registros
Nombre   |Alias                  |Permisos disponibles|Dependencias
--       |-                      |-                   |-
print    |Imprimir agenda del día|r-x                 |orders.list-all
