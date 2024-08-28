<p align="center"><a href="https://app.papeleralamilagrosa.com.ar" target="_blank"><img src="https://app.papeleralamilagrosa.com.ar/images/logo.jpg" width="240"></a></p>

<p style="text-align: right;">
  <a href="../README.md">HOME</a>
</p>

## Módulo de Carrito

#### Acciones CRUD
##### Crear registros
Nombre    |Alias              |Permisos disponibles|Dependencias
--        |-                  |-                   |-
create-new|Crear nuevo carrito|rwx                 |catalogs.list

##### Mostrar registros
Nombre      |Alias            |Permisos disponibles|Dependencias
--          |-                |-                   |-
show-cart   |Mostrar carrito  |r--                 |-
show-catalog|Mostrar lista    |r--                 |catalogs.list
show-history|Mostrar historial|r--                 |orders.list

##### Editar registros
Nombre    |Alias                         |Permisos disponibles|Dependencias
--        |-                             |-                   |-
add-item  |Agregar un producto al carrito|rw-                 |-
del-item  |Quitar un producto del carrito|-w-                 |-
edit      |Editar carrito                |rw-                 |
set-delay |Programar pedido              |-w-                 |orders.edit-queued

##### Acciones varias
Nombre        |Alias                    |Permisos disponibles|Dependencias
--            |-                        |-                   |-
export-catalog|Exportar lista de precios|r-x                 |cart.show-catalog
