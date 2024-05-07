#instalacion de template ma crwacion de proyecto

    comandos create-project laravel/laravel SURE

#config .env

    php artisan key:generate

    php artisan migrate


#install template and config

    composer require jeroennoten/laravel-adminlte

    php artisan adminlte:install

    composer require laravel/ui
    php artisan ui bootstrap --auth
    php artisan adminlte:install --only=auth_views

#en resources/home.blade.php

    @extends('adminlte::page')

    @section('title', 'Dashboard')

    @section('content_header')
        <h1>Dashboard</h1>
    @stop

    @section('content')
        <p>Welcome to this beautiful admin panel.</p>
    @stop

    @section('css')
        {{-- Add here extra stylesheets --}}
        {{-- <link rel="stylesheet" href="/css/admin_custom.css"> --}}
    @stop

    @section('js')
        <script> console.log("Hi, I'm using the Laravel-AdminLTE package!"); </script>
    @stop

