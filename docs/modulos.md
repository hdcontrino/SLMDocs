<p align="center"><a href="https://app.papeleralamilagrosa.com.ar" target="_blank"><img src="https://app.papeleralamilagrosa.com.ar/images/logo.jpg" width="240"></a></p>

<p style="text-align: right;">
  <a href="../README.md">HOME</a>
</p>

## Módulos de Usuario (panels)
El SLM poseé una única interfaz privada donde, dependiendo del rol del usuario, se visualizan distintos módulos o paneles.
Dependiendo el o los módulos que se muestren la interfaz puede dividirse en dos secciones, una vista principal y una lateral (derecha) que muestra información detallada sobre elementos de la vista principal.
En los casos en que un usuaro pueda ver más de un módulo, se habilita un menú lateral (izq.) para navegar cada uno de los módulos disponibles.

##### Módulos disponibles actualmente (panels)
ID|Nombre   | Alias   | Descripción                    | Icono
--|-        |-        |-                               |-
1 |orders   |Pedidos  |Panel de pedidos de clientes    |fa-clipboard-list
2 |schedules|Agenda   |Agenda de pedidos de clientes   |fa-calendar-days
3 |trips    |Envíos   |Panel de envíos de pedidos      |fa-truck-fast
4 |catalogs |Listas   |Panel de listas de precios      |fa-file-invoice-dollar
5 |products |Productos|Panel de productos              |fa-boxes-stacked
6 |users    |Usuarios |Panel de usuarios               |fa-users
7 |reports  |Informes |Panel de informes y estadísticas|fa-chart-line

###### Otros módulos 
Nombre   |Alias | Descripción                                  | Icono
--       |-     |-                                             |-
trip-form|QRs   |Vista pública para reportar cierres de pedidos|--

##### Acciones
Cada módulo tiene asociadas distintas acciones que permiten que los usuarios con acceso puedan interactuar con los datos que ofrece el módulo. En ocaciones, algunos módulos muestran acciones que pertenecen a otros. Para poder ejecutar esas acciones, el usuario siempre necesitará los permisos del módulo de la acción, con tener sólo los permisos del módulo que la muestra no será suficiente para ejecutarla.

- [Acciones del módulo Pedidos](orders.md#acciones)
- [Acciones del módulo Agenda](schedules.md#acciones)
- [Acciones del módulo Envíos](trips.md#acciones)
- [Acciones del módulo Listas](catalogs.md#acciones)
- [Acciones del módulo Productos](products.md#acciones)
- [Acciones del módulo Usuarios](users.md#acciones)
- [Acciones del módulo Informes](reports.md#acciones)
