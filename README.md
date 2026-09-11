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
# Tipos de Redes  en Docker
- BBridge: red por defecto, los contenedores se hablan entre sí y salen a internet por NAT.
- Host: usa la red del host directamente, sin aislamiento.
- None: sin red, solo el contenedor consigo mismo.
- Overlay: conecta contenedores en distintas máquinas (Swarm).
- Macvlan: cada contenedor parece un dispositivo físico más en la red, con su propia IP.
- IPvlan: como macvlan, pero comparten la MAC del host.
# Tipo de Volumenes en Docker
- Volumes: gestionados completamente por Docker, se almacenan en /var/lib/docker/volumes/ dentro del host. Es la forma recomendada de persistir datos porque Docker maneja backups, migración y permisos, y funciona bien tanto en Linux como en Windows.
- Bind mounts: montan una carpeta o archivo específico del host, usando su ruta exacta, directamente dentro del contenedor. Dan mayor control sobre la ubicación de los datos, pero dependen de la estructura del sistema host, por lo que son menos portables entre entornos.
- tmpfs mounts: se almacenan solo en la memoria RAM del host, nunca en disco. Al detener el contenedor esos datos se pierden. Son útiles para información sensible o temporal que no debe persistir.
-Named vs anonymous volumes: dentro de los volumes gestionados, los named tienen un nombre definido por el usuario, lo que facilita reutilizarlos en otros contenedores; los anonymous se crean automáticamente con un identificador tipo hash, siendo más difíciles de referenciar después.
# Indicaciones
## Comandos
```bash
docker run                   
docker run -d              
docker run -p 3000:3000           
docker run -e VAR=valor             
docker run --name mi-contenedor     
docker run --rm                     
docker compose up -d
```
## Configuración por entorno
```
MESSAGE=<Piero Cardenas Julian>
```
![Contenedores corriendo y las 3 copias](./img/image.png)
# Creditos
- Cardenas Julian Juan Piero 
- ID: 000115468
# ETC