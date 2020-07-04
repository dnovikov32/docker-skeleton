# Docker website skeleton

### Docker containers
- PHP 7.4
- Mysql 5.7 
- Nginx 1.13 

### Hot to setup
Create **.env** file:
```bash
$ cp .env.example .env
```

Set docker hosts in **.env** file:
```dotenv
DOCKER_FRONTEND_HOST=skeleton.docker
DOCKER_BACKEND_HOST=admin.skeleton.docker
```

Update **/etc/hosts** file:
```text
127.0.1.1   skeleton.docker
127.0.1.1   admin.skeleton.docker
```

Run command:
```bash
$ make docker-up
```

The following hosts works by default: 
- Frontend http://skeleton.docker
- Backend http://admin.skeleton.docker

### Available command
```bash
$ make docker-up        # Start all docker containers
$ make docker-down      # Stop all docker containers
$ make docker-build     # Build all docker images, for example, when changing the nginx config
$ make docker-rebuild   # Build all docker images from scratch, without cache etc
$ make ssh-php          # PHP container console
```




