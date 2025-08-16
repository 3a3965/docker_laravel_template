# DSLE-11 

Docker Start Laravel Environment for 11 version of Laravel. Includes:
- PHP 8.2
- MySQL
- Redis
- PhpMyAdmin

## Installation

Clone repo and use local.sh to start. On Windows use Git Bash:

```bash
./local.sh start
```

If containers are okay, go inside container:
```bash
./local.sh ssh
```

And inside container:
```bash
composer create-project laravel/laravel:^11.0 .
```

After Laravel installation:
Copy<br>
   <b>APP_NAME</b><br>
and<br>
   <b>DB_CONNECTION=mysql<br>
   DB_HOST=database<br>
   DB_PORT=3306<br>
   DB_DATABASE=easyapp<br>
   DB_USERNAME=user<br>
   DB_PASSWORD=password<br></b>
sections from .env to src/.env and run inside container:
```bash
php artisan migrate:fresh
```

Congrats! You have Laravel and all the stuff runing!
