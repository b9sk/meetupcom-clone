# A Laravel 9 app with Sail

## Services in the template
- php 8.2
- mysql 8.0
- redis
- minio

## Installation

### Step 1
Clone the repository 

### Step 2 (optional)
Update Docker ports if needed in .env file:
- APP_PORT
- VITE_PORT
- FORWARD_DB_PORT

### Step 3
Sail doesn't exist yet, install Composer dependencies to install Sail:
- `composer install --ignore-platform-reqs`

Probably you faced the error: `Script @php artisan package:discover --ansi handling the post-autoload-dump event returned with error code 1`. It will be gone later.

### Step 4
Set up Docker:
- `./vendor/bin/sail up --build -d`

Also you may call `docker compose` directly.

### Step 5
Ensure the error from Step 3 is gone:
- `./vendor/bin/sail composer install`

## Essential Sail commands
- `./vendor/bin/sail` list available Sail commands
- `./vendor/bin/sail artisan` artisan
- `./vendor/bin/sail composer` composer
- `./vendor/bin/sail node` node
- `./vendor/bin/sail test` an alias of `php artisan test`
- `./vendor/bin/sail tinker` an alias of `php artisan tinker`

Optionally, in Linux you may create a Sail shortcut:  `ln -s ./vendor/bin/sail sail`.

## Futher reading

### Laravel 9 Sail reference 
https://laravel.com/docs/9.x/sail
