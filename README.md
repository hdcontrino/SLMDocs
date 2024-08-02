<p align="center"><a href="https://app.papeleralamilagrosa.com.ar" target="_blank"><img src="https://app.papeleralamilagrosa.com.ar/images/logo.jpg" width="240"></a></p>

## Sistema La Milagrosa – SLM v1.17.0
Sistema de gestión de operación de Papelera La Milagrosa. Laravel Framework based.

Document Version: 1.0.0
Laravel Version: 8.83.27
PHP Version: 7.4.33

- [INTERFACES Y VISTAS](docs/interfaces.md)
- [USUARIOS Y ROLES](docs/usuarios.md)
- [AUTENTICACIÓN Y ACCESOS](docs/autenticacion.md)
- [MÓDULOS DE USUARIO](docs/modulos.md)
- [ROLES Y PERMISOS](docs/permisos.md)

NOTA: Actualmente el SLM se encuentra optimizado únicamente para utilizarlo a través de Google Chrome.


##### Roles de usuario existentes actualmente (roles)
```
[
    {
        "id": 1,
        "name": "admin",
        "singular": "Administración General",
        "plural": "Administradores Generales",
        "description": "Administración General",
        "defpanel": "orders",
        "panels": {
            "orders": 2,
            "schedules": 2,
            "trips": 2,
            "catalogs": 2,
            "products": 2,
            "users": 2,
            "reports": 2
        }
    },
    {
        "id":2,
        "name": "customer",
        "singular": "Cliente",
        "plural": "Clientes",
        "description": "Usuario de tipo Cliente",
        "defpanel": "catalogs",
        "panels": {
            "orders": 0,
            "schedules": 0,
            "trips": 0,
            "catalogs": 2,
            "products": 0,
            "users": 0,
            "reports": 0
        }
    },
    {
        "id": 3,
        "name": "collector",
        "singular": "Cta. Cte. y Facturación",
        "plural": "de Cta. Cte. y Facturación",
        "description": "Usuarios del sector de Cta. Cte. y Facturación",
        "defpanel": "orders",
        "panels": {
            "orders": 2,
            "schedules": 1,
            "trips": 2,
            "catalogs": 2,
            "products": 2,
            "users": 0,
            "reports": 0
        }
    },
    {
        "id": 4,
        "name": "control",
        "singular": "Control Final",
        "plural": "de Control Final",
        "description": "Usuario del sector de Control Final",
        "defpanel": "schedules",
        "panels": {
            "orders": 0,
            "schedules": 1,
            "trips": 2,
            "catalogs": 0,
            "products": 0,
            "users": 0,
            "reports": 0
        }
    },
    {
        "id": 5,
        "name": "sales",
        "singular": "Administración de Ventas",
        "plural": "de Administración de Ventas",
        "description": "Usuario del sector de Administración de Ventas",
        "defpanel": "orders",
        "panels": {
            "orders": 2,
            "schedules": 2,
            "trips": 1,
            "catalogs": 2,
            "products": 2,
            "users": 2,
            "reports": 0
        }
    },
    {
        "id": 6,
        "name": "depot",
        "singular": "Depóstio y Logística de Despacho",
        "plural": "de Depóstio y Logística de Despacho",
        "description": "Usuario del sector de Depóstio y Logística de Despacho",
        "defpanel": "schedules",
        "panels": {
            "orders": 0,
            "schedules": 2,
            "trips": 2,
            "catalogs": 0,
            "products": 0,
            "users": 0,
            "reports": 0
        }
    }
]
```
##### Códigos de permisos de roles de usuario (permission)
```
{
    0: "No tiene acceso al panel",
    1: "Puede ver el panel",
    2: "Puede ver el panel y las opciones de edición"
}
```

##### Equipo de desarrollo
CDT Coheda Development Team
**[COHEDA LTD](https://coheda.com?ref=U0xNIFBhcGVsZXJhIGxhIG1pbGFncm9zYSAoRG9jdW1lbnRhY2nzbik=)**

##### Project Manager
- **Name:** Daniel Contrino
- **GitHub:** [hdcontrino](https://github.com/hdcontrino)

### License

The Laravel framework is open-sourced software licensed under the [MIT license](https://opensource.org/licenses/MIT).
