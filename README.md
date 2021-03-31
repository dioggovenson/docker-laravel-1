## Simple CRUD service built with Docker
### Pre-requisites
* Docker running on the host machine.
* Docker compose running on the host machine.
* Docker version 20.10.5
* docker-compose version 1.27.4
## Installation
### To get started, the following steps needs to be taken:
* Clone the repo.
* git clone https://github.com/elijahhada/docker-laravel.git into a folder of your choice
* cd docker-laravel/ to the project directory.
* run command:
* sudo docker run --rm -v ${PWD}:/app composer install
* run command:
* sudo docker-compose build --no-cache
* after successful built run command:
* sudo docker-compose up -d
* copy from .env.example to .env:
* cp .env.example .env to use env config file
* run commands to migrate and seed db:
* sudo docker-compose exec app php artisan migrate
* sudo docker-compose exec app php artisan db:seed
* Visit http://localhost:8100 to see Laravel application.
## usage:
* docker-compose up -d to start all containers
* docker-compose down to stop all containers
* to test application you can use Postman, available urls and actions:
* GET http://localhost:8100/api/users
* POST http://localhost:8100/api/users
* GET http://localhost:8100/api/users/id
* PUT http://localhost:8100/api/users/id
* DELETE http://localhost:8100/api/users/id
