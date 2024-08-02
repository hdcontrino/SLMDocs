<p align="center"><a href="https://app.papeleralamilagrosa.com.ar" target="_blank"><img src="https://app.papeleralamilagrosa.com.ar/images/logo.jpg" width="240"></a></p>

## Roles y Permisos
El SLM trabaja los permisos de los usuarios por medio del acceso que sus roles les dan a cada uno de los espacios disponibles.
La base de los permisos se administra de acuerdo a tres instancias:
- r (read): permite ver el contenido del espacio.
- w (write): permite guardar o modificar información que el espacio muestra.
- x (execute): permite ejecutar tareas o funciones específicas.

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
Nombre   |Módulo      |Permisos
--       |-           |-
admin    |orders      |rw
admin    |schedules   |rw
