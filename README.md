```
.
├── nginx/
│   ├── docker-compose.yml    # Configuración principal
│   └── conf.d/               # Configs de todos los proyectos
└── proyectoX/                # Carpeta independiente por proyecto
    └── nginx.conf            # Config específica del proyecto
```


Agregar un nuevo servidor de aplicacion usando el template.
Primero crear el archivo solo con la parte http del template.
Posteriormente (despues de generar los certificados) agregar la parte https del template.

```bash
docker-compose run --rm certbot certonly --webroot --webroot-path /var/www/certbot/ --dry-run -d [domain-name]
```


```bash
docker-compose run --rm certbot certonly --webroot --webroot-path /var/www/certbot/ -d [domain-name]
```
