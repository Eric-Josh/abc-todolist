## abc todoList

## Build
Built with Laravel 8, PHP 8.x, Vue 3

## Installation
* Clone Repository `git clone https://github.com/Eric-Josh/abc-todolist`
* Move into project path `cd abc-todolist`
* Install all dependencies `composer install or composer update` & `npm install or npm update`
* Create DB
* Copy .env.example to .env `cp .env.example .env`
* Generate APP_KEY `php artisan key:generate`
* Add DB details in .env
* Run Migration `php artisan migrate`
* Run app `php artisan serve` & `npm run hot`

## CRUD Endpoints
```
GET: /api/items

POST: /api/item

PUT: /api/item/:id

DELETE: /api/item/:id
```
