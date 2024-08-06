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

