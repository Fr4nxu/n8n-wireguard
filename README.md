# n8n con WireGuard en Docker

En un entorno de TI moderno, la capacidad de automatizar flujos de trabajo y gestionar procesos de manera eficiente es crucial. n8n, una herramienta de automatización de código abierto, se destaca como una solución flexible y potente que permite integrar diversas APIs y servicios en flujos de trabajo personalizados. Combinado con una VPN WireGuard, n8n se convierte en una herramienta accesible y segura desde cualquier ubicación, lo que maximiza su utilidad en entornos distribuidos o remotos.

## Características

- **n8n**: Plataforma de automatización de flujos de trabajo de código abierto que permite conectar diversas aplicaciones y servicios para automatizar tareas repetitivas.
- **WireGuard**: WireGuard es una solución de VPN moderna, conocida por su simplicidad, velocidad y alto nivel de seguridad.
- **Acceso Remoto Seguro**: Permite acceder a tu instancia de n8n desde cualquier lugar del mundo de manera segura, protegiendo tus datos y flujos de trabajo

## Requisitos

Antes de comenzar, asegúrate de tener instaladas las siguientes herramientas en tu sistema Linux:

- **[Docker](https://docs.docker.com/engine/install/)**: Plataforma para ejecutar contenedores.
- **[Docker Compose](https://docs.docker.com/compose/install/)**: Herramienta para definir y ejecutar aplicaciones Docker con múltiples contenedores.

Puedes instalar Docker y Docker Compose usando estos comandos:

```bash
# Instalar Docker
sudo apt-get update
sudo apt-get install -y docker.io docker-compose

```bash
#añadir el usuario actual al grupo docker
sudo usermod -aG docker ${USER}
#aplicar cambios sin reiniciar
su - ${USER}
#comprobar que el usuario se ha añadido correctamente al grupo DOCKER
id -nG

```bash
# Iniciar y habilitar Docker
sudo systemctl start docker
sudo systemctl enable docker

### Configurar variables de entorno
Modifica el .env.example adapatandolo a tus necesidades

```bash
# Levantar los servicios
docker-compose up -d
#Verificar estado de los servicios
docker-compose ps 

### Acceder a n8n
http://localhost:5678

### Conectar un cliente VPN



