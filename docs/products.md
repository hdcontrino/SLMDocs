<p align="center"><a href="https://app.papeleralamilagrosa.com.ar" target="_blank"><img src="https://app.papeleralamilagrosa.com.ar/images/logo.jpg" width="240"></a></p>

<p style="text-align: right;">
  <a href="../README.md">HOME</a>
</p>

## Módulo de Productos

#### Acciones CRUD
##### Crear registros
Nombre    |Alias               |Permisos disponibles|Dependencias
--        |-                   |-                   |-
create-new|Crear nuevo producto|rwx                 |product.search-all

##### Mostrar registros
Nombre             |Alias           |Permisos disponibles|Dependencias
--                 |-               |-                   |-
list-all           |Ver Todos       |r--                 |-
list-product_type-1|Ver Artículos   |r--                 |-
list-product_type-2|Ver Bolsones    |r--                 |-

#### Otras acciones
##### Mostrar resúmenes
Nombre                     |Alias                   |Permisos disponibles|Dependencias
--                         |-                       |-                   |-
show-summary-all           |Ver resumen de Todos    |r--                 |-
show-summary-product_type-1|Ver resumen de Artículos|r--                 |-
show-summary-product_type-2|Ver resumen de Bolsones |r--                 |-

##### Mostrar detalles
Nombre             |Alias                    |Permisos disponibles|Dependencias
--                 |-                        |-                   |-
show-product-detail|Ver detalles del producto|rw-                 |-

##### Buscar registros
Nombre     |Alias           |Permisos disponibles|Dependencias
--         |-               |-                   |-
search-all |Buscar productos|r--                 |-
