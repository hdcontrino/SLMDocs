<p align="center"><a href="https://app.papeleralamilagrosa.com.ar" target="_blank"><img src="https://app.papeleralamilagrosa.com.ar/images/logo.jpg" width="240"></a></p>

## Interfaces y Vistas
El SLM poseé actualmente dos interfaces, una pública y otra privada, a las cuales se puede acceder a través de internet.

##### Intefaz pública `resources/views/layouts/public.blade.php`
- **QRs:**
Se accede a través del link embebido en los códigos QR que se obtienen al imprimir un envío. La interfaz está compuesta de un pequeño diálogo que lista los pedidos que componen ese envío. Cada uno de los elementos de esta lista poseé un formulario que permite informar sobre la entrega del pedido que representa. El usuario que accede (generalmente un chofer que tiene el QR) puede subir una imagen del remito de entrega junto a su número y marcar el pedido como entregado.

##### Interfaz privada `resources/views/layouts/app.blade.php`
Todos los usuarios registrados en el sistema pueden acceder a esta interfaz a través de la vista [dashboard](#dashboard), según el rol asignado podrán ver uno o varios módulos que le permitirán interactuar con la plataforma según sus permisos. [Ver Roles y Permisos](docs/permisos.md)

## Vistas
Las vistas están compuestas de secciones generales que comprenden subsecciones y componentes, que se detallan a continuación.

#### Login 
`resources/views/auth/login.blade.php`
Si bien esta vista es de acceso público, está diseñada para otorgar acceso a la vista privada a aquellos usuarios registrados que posean un rol habilitado. Cuando un usuario accede a esta [Ver Autenticación y Accesos](docs/autenticacion.md)

#### Dashboard
`resources/views/layouts/dashboard.blade.php`
El Dashboard

##### Secciones

##### Componentes
Dentro de la interfaz privada existen varios componentes generales habilitados según el rol del usuario. Algunos de ellos sufren cambios visuales o funcionales dependiendo el rol del usuario que los accede.
- Barra de Búsqueda `App\View\Components\SearchBar::class`
- Campo de selección `App\View\Components\SelectControl::class`
- Campo tipo switch `App\View\Components\SwitchControl::class`
- Diálogo `App\View\Components\Dialog::class`
- Espera por carga `App\View\Components\Loading::class`
- Menú de usuario `App\View\Components\UserMenu::class`
- Panel Derecho `App\View\Components\RightPanel::class`
- Panel Izquierdo `App\View\Components\LeftPanel::class`
- Pie de Página `App\View\Components\Footer::class`
