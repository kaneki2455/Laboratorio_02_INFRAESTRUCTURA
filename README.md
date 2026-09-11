# Laboratorio 02
Hoy utilizaremos docker compose para poder desplegar su trabajo. Servicio web y una
base de datos
## Stack
API
- Minimal API
- Debe retornar un mensaje incluyendo mi nombre
- Lista Dockers
- -  docker run -d --rm -p 3000:3000 nmatsui/hello-world-api. 44035c3c38c8  - vigorous_banach
- - docker run -d --rm -p 3001:3000 nmatsui/hello-world-api. e43f29cf57b3 - distracted_wilbur
- - docker run -d --rm -p 3002:3000 nmatsui/hello-world-api. 907bc961e055 - determined_jeps
BD
- PostgreSQL
- $ docker run --name Lab_2 -e POSTGRES_PASSWORD=123 -d postgres  
- Volumenes
- db_data:/var/lib/postgresql/data
- db_data - nombre de volumen 
- /var/lib/postgresql/data - ruta dentro del contenedor de Postgres
# Indicaciones
## Comandos
```bash
docker compose up -d
```
## Configuración por entorno
```
MESSAGE=<Piero Cardenas>
```
# Creditos
- Cardenas Julian Juan Piero 
- ID: 000115468
# ETC