Laravel 5.6 test template with AdminLTE package
-----------------------------------------------
Laravel AdminLTE manual installation
Follow the typical Laravel package installation steps:

composer create-project --prefer-dist laravel/laravel template
config your .env file
php artisan make:auth
php artisan migrate


1) Add admin-lte Laravel package with:
composer require "acacha/admin-lte-template-laravel:4.*"

2) To register the Service Provider edit config/app.php file and add to providers array:
/*
 * Acacha AdminLTE template provider
 */
Acacha\AdminLTETemplateLaravel\Providers\AdminLTETemplateServiceProvider::class,

3) To Register Alias edit config/app.php file and add to alias array:
/*
 * Acacha AdminLTE template alias
 */
'AdminLTE' => Acacha\AdminLTETemplateLaravel\Facades\AdminLTE::class,

4) Publish files with:
php artisan vendor:publish --tag=adminlte --force
