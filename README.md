# n8n con WireGuard en Docker

Este proyecto proporciona un entorno de automatización con [n8n](https://n8n.io/) junto con una VPN [WireGuard](https://www.wireguard.com/) utilizando Docker. n8n es una herramienta de automatización de flujos de trabajo y WireGuard es una solución VPN moderna y rápida.

## Características

- **n8n**: Plataforma de automatización de flujos de trabajo de código abierto.
- **WireGuard**: Solución de VPN rápida y segura.
- **Docker Compose**: Orquesta la configuración y ejecución de los contenedores.

## Requisitos

Antes de comenzar, asegúrate de tener instaladas las siguientes herramientas en tu sistema Linux:

- **[Docker](https://docs.docker.com/engine/install/)**: Plataforma para ejecutar contenedores.
- **[Docker Compose](https://docs.docker.com/compose/install/)**: Herramienta para definir y ejecutar aplicaciones Docker con múltiples contenedores.

Puedes instalar Docker y Docker Compose usando estos comandos:

```bash
# Instalar Docker
sudo apt-get update
sudo apt-get install -y docker.io

# Iniciar y habilitar Docker
sudo systemctl start docker
sudo systemctl enable docker

# Instalar Docker Compose
sudo curl -L "https://github.com/docker/compose/releases/download/$(curl -s https://api.github.com/repos/docker/compose/releases/latest | grep tag_name | cut -d '\"' -f 4)/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose

# Dar permisos de ejecución a Docker Compose
sudo chmod +x /usr/local/bin/docker-compose
