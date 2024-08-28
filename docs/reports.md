<p align="center"><a href="https://app.papeleralamilagrosa.com.ar" target="_blank"><img src="https://app.papeleralamilagrosa.com.ar/images/logo.jpg" width="240"></a></p>

<p style="text-align: right;">
  <a href="../README.md">HOME</a>
</p>

## Módulo de Informes

#### Acciones CRUD
##### Crear registros
Nombre    |Alias              |Permisos disponibles|Dependencias
--        |-                  |-                   |-
create-new|Crear nuevo informe|rwx                 |orders.search-order_status-1, orders.search-order_status-8, products.search-all, users.search-rol-2

##### Mostrar registros
Nombre        |Alias                |Permisos disponibles|Dependencias
--            |-                    |-                   |-
list-saved    |Ver Guardados        |r--                 |-

#### Otras acciones
##### Mostrar resúmenes
Nombre            |Alias                   |Permisos disponibles|Dependencias
--                |-                       |-                   |-
show-summary-saved|Ver resumen de Guardados|r--                 |-

##### Mostrar detalles
Nombre            |Alias                  |Permisos disponibles|Dependencias
--                |-                      |-                   |-
show-report-detail|Ver detalles de Informe|r--                 |orders.list-all, users.list-rol-2

##### Buscar registros
Nombre     |Alias          |Permisos disponibles|Dependencias
--         |-              |-                   |-
search-all |Buscar informes|r--                 |-

##### Imprimir registros
Nombre       |Alias                |Permisos disponibles|Dependencias
--           |-                    |-                   |-
print-current|Imprimir mes en curso|r-x                 |-
print-report |Imprimir reporte     |r-x                 |-

##### Acciones varias
Nombre        |Alias                |Permisos disponibles|Dependencias
--            |-                    |-                   |-
export-current|Exportar mes en curso|rw-                 |reports.list-saved
export-report |Exportar reporte     |rw-                 |reports.list-saved
