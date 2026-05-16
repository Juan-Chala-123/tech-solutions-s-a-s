# Jenkins

En esta actividad se realizó la implementación de un entorno de integración continua utilizando Jenkins y Docker, permitiendo automatizar procesos de validación y pruebas de proyectos de software.

Se configuraron Jobs tipo Pipeline para ejecutar verificaciones automáticas sobre un proyecto desarrollado con un framework de desarrollo web, integrando GitHub para la activación automática mediante Webhooks y configurando notificaciones vía correo electrónico y Discord.

### Docker

Esta es una configuracion base de Jenkins, mediante un gestion por docker compose.

#### docker-compose.yml

```yml
services:
    jenkins:
        container_name: jenkins-container
        image: jenkins/jenkins:2.555.1-lts-jdk25
        restart: unless-stopped
        user: root
        ports:
            - 9090:8080
            - 50000:50000
        volumes:
            - jenkins_home:/var/jenkins_home
            - /var/run/docker.sock:/var/run/docker.sock

volumes:
jenkins_home:
```

### Pipeline

```pipeline

```

### Evidencias

#### Instalación de Plugin

![Plugin](public/images/install-plugins.png)

#### Instalacion de Discord Notifier

![Discord Notifier](public/images/discord-notifier.png)

#### Notificacion a un servidor de Discord

![Notificacion Discord](public/images/discord-nitifier1.png)