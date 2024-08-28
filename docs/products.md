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
Nombre               |Alias              |Permisos disponibles|Dependencias
--                   |-                  |-                   |-
list-all             |Ver Todos          |r--                 |-
list-product_type-1  |Ver Artículos      |r--                 |-
list-product_type-2  |Ver Bolsones       |r--                 |-

##### Editar registros
Nombre               |Alias                        |Permisos disponibles|Dependencias
--                   |-                            |-                   |-
edit                 |Editar producto              |rw-                 |
import-all           |Importar precios de productos|-wx                 |products.edit
import-product_type-1|Importar precios de artículos|-wx                 |products.edit
import-product_type-2|Importar precios de bolsones |-wx                 |products.edit
set-fixed-price      |Fijar precio de producto     |rw-                 |products.edit
set-product-prices   |Modificar precios en lote    |rw-                 |products.edit

##### Eliminar registros
Nombre     |Alias                        |Permisos disponibles|Dependencias
--         |-                            |-                   |-
delete     |Eliminar producto            |-w-                 |-

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

##### Acciones varias
Nombre               |Alias              |Permisos disponibles|Dependencias
export-all           |Exportar Productos |r--                 |-
export-product_type-1|Exportar Artículos |r--                 |-
export-product_type-2|Exportar Bolsones  |r--                 |-
hide-product         |Desactivar producto|-w-                 |products.edit
show-product         |Activar producto   |-w-                 |products.edit
