<p align="center"><a href="https://app.papeleralamilagrosa.com.ar" target="_blank"><img src="https://app.papeleralamilagrosa.com.ar/images/logo.jpg" width="240"></a></p>

<p style="text-align: right;">
  <a href="../README.md">HOME</a>
</p>

## Módulo de Usuarios

#### Acciones CRUD
##### Crear registros
Nombre    |Alias              |Permisos disponibles|Dependencias
--        |-                  |-                   |-
create-new|Crear nuevo usuario|rwx                 |-

##### Mostrar registros
Nombre            |Alias                                  |Permisos disponibles|Dependencias
--                |-                                      |-                   |-
list-all          |Ver Todos                              |r--                 |-
list-rol-1        |Ver Administradores Generales          |r--                 |-
list-rol-2        |Ver Clientes                           |r--                 |-
list-rol-3        |Ver de Cta. Cte. y Facturación         |r--                 |-
list-rol-4        |Ver de Control Final                   |r--                 |-
list-rol-5        |Ver de Administración de Ventas        |r--                 |-
list-rol-6        |Ver de Depóstio y Logística de Despacho|r--                 |-

##### Editar registros
Nombre            |Alias                        |Permisos disponibles|Dependencias
--                |-                            |-                   |-
edit              |Editar usuario               |rw-                 |
edit-customer     |Editar variables de cliente  |rw-                 |users.edit
send-pwd-recovery |Enviar recuperación de clave |rwx                 |users.edit
set-address       |Añador dirección de cliente  |rw-                 |users.edit-customer
set-catalog       |Definir lista de precios     |rw-                 |users.edit-customer, catalogs.list-all

##### Eliminar registros
Nombre         |Alias           |Permisos disponibles|Dependencias
--             |-               |-                   |-
delete         |Eliminar usuario|-w-                 |-
delete-customer|Eliminar cliente|-w-                 |users.edit

#### Otras acciones
##### Mostrar resúmenes
Nombre            |Alias                                             |Permisos disponibles|Dependencias
--                |-                                                 |-                   |-
show-summary-all  |Ver resumen de Todos                              |r--                 |-
show-summary-rol-1|Ver resumen de Administradores Generales          |r--                 |-
show-summary-rol-2|Ver resumen de Clientes                           |r--                 |-
show-summary-rol-3|Ver resumen de de Cta. Cte. y Facturación         |r--                 |-
show-summary-rol-4|Ver resumen de de Control Final                   |r--                 |-
show-summary-rol-5|Ver resumen de de Administración de Ventas        |r--                 |-
show-summary-rol-6|Ver resumen de de Depóstio y Logística de Despacho|r--                 |-

##### Mostrar detalles
Nombre          |Alias                    |Permisos disponibles|Dependencias
--              |-                        |-                   |-
show-profile    |Ver el perfil del usuario|rw-                 |-
show-user-detail|Ver detalles del usuario |rw-                 |-

##### Buscar registros
Nombre      |Alias                                              |Permisos disponibles|Dependencias
--          |-                                                  |-                   |-
search-all  |Buscar usuarios                                    |r--                 |-
search-rol-1|Buscar usuarios Administradores Generales          |r--                 |-
search-rol-2|Buscar usuarios Clientes                           |r--                 |-
search-rol-3|Buscar usuarios de Cta. Cte. y Facturación         |r--                 |-
search-rol-4|Buscar usuarios de Control Final                   |r--                 |-
search-rol-5|Buscar usuarios de Administración de Ventas        |r--                 |-
search-rol-6|Buscar usuarios de Depóstio y Logística de Despacho|r--                 |-

##### Acciones varias
Nombre            |Alias                            |Permisos disponibles|Dependencias
hide-user         |Desactivar usuario               |r--                 |users.edit
share-pwd-recovery|Ver link de recuperación de clave|rwx                 |users.edit
show-user         |Activar usuario                  |r--                 |users.edit
