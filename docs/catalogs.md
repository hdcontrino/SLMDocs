<p align="center"><a href="https://app.papeleralamilagrosa.com.ar" target="_blank"><img src="https://app.papeleralamilagrosa.com.ar/images/logo.jpg" width="240"></a></p>

<p style="text-align: right;">
  <a href="../README.md">HOME</a>
</p>

## Módulo de Listas

#### Acciones CRUD
##### Crear registros
Nombre               |Alias                        |Permisos disponibles|Dependencias
--                   |-                            |-                   |-
create-new           |Crear nueva lista            |rwx                 |products.search-all
import-all-prices    |Importar precios de listas   |rwx                 |catalogs.edit
import-catalog-prices|Importar precios de una lista|rwx                 |catalogs.edit

##### Mostrar registros
Nombre   |Alias         |Permisos disponibles|Dependencias
--       |-             |-                   |-
list     |Ver una lista |r--                 |products.list
list-all |Ver Todos     |r--                 |products.list

##### Editar registros
Nombre         |Alias                        |Permisos disponibles|Dependencias
--             |-                            |-                   |-
edit           |Editar lista                 |rw-                 |
edit-level     |Editar porcentual de la lista|rw-                 |catalogs.edit
set-fixed-price|Fijar precio de producto     |rw-                 |catalogs.edit
set-product    |Añadir producto a la lista   |rw-                 |catalogs.edit

##### Eliminar registros
Nombre     |Alias                        |Permisos disponibles|Dependencias
--         |-                            |-                   |-
delete     |Eliminar lista               |-w-                 |-
del-product|Eliminar producto de la lista|rw-                 |catalogs.edit

#### Otras acciones
##### Mostrar resúmenes
Nombre          |Alias               |Permisos disponibles|Dependencias
--              |-                   |-                   |-
show-summary-all|Ver resumen de Todos|r--                 |-

##### Mostrar detalles
Nombre             |Alias                    |Permisos disponibles|Dependencias
--                 |-                        |-                   |-
show-product       |Ver productos de la lista|rw-                 |products.list-all
show-product-detail|Ver detalle del producto |rw-                 |products.show-detail

##### Buscar registros
Nombre     |Alias        |Permisos disponibles|Dependencias
--         |-            |-                   |-
search-all |Buscar listas|r--                 |products.search-all

##### Acciones varias
Nombre        |Alias            |Permisos disponibles|Dependencias
--            |-                |-                   |-
export-all    |Exportar Todos   |r--                 |catalogs.list-all
export-catalog|Exportar lista   |r--                 |catalogs.list-all
hide-catalog  |Desactivar lista |r--                 |catalogs.edit
show-catalog  |Activar lista    |r--                 |catalogs.edit