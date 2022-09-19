# Docker Environment
` Docker Enviourment for run mutliple enviourment instance in same machine`

# Installation
- [Install Docker](https://www.docker.com/)
    - [Installation Guideline](https://www.digitalocean.com/community/tutorials/how-to-install-and-use-docker-on-ubuntu-18-04)
- [docker-compose](https://docs.docker.com/compose/) 
    ```
    sudo apt install docker-compose
    ```
#### Run commands after clone project for each service (such as commonService, php8apps, php7apps etc)

*To build and run docker image*
```
docker-compose up --build
```

*If already builed then just run
```
docker-compose up -d (run in background)
```

# How to run a project

```
syntax: docker-compose run -rm -pDockerport:ExternalPort service-name bash
```

```
example: docker-compose run --rm -p8700:8000 php8apps bash 
```
*then go to the directory what you want to run
```
cd example
```

*then run the project
```
php artisan serve --host=0.0.0.0 (for laravel project)
```

*then hit to browser with port
```
http://0.0.0.0:8700
```
