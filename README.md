# Laravel 6.0 TCPDF
<p align="center">
<a href="https://travis-ci.org/villca/numeros-en-letras"><img src="https://travis-ci.org/villca/tcpdf-laravel.svg" alt="Build Status"></a>
<a href="https://packagist.org/packages/villca/numeros-en-letras"><img src="https://poser.pugx.org/villca/tcpdf-laravel/v/stable.svg" alt="Latest Stable Version"></a>
<a href="https://packagist.org/packages/villca/numeros-en-letras"><img src="https://poser.pugx.org/villca/tcpdf-laravel/d/total.svg" alt="Total Downloads"></a>
<a href="https://packagist.org/packages/villca/numeros-en-letras"><img src="https://poser.pugx.org/villca/tcpdf-laravel/license.svg" alt="License"></a>
</p>

## PHP Framework

<p align="center">
<img src="https://laravel.com/assets/img/components/logo-laravel.svg">
</p>

## Descripción
Generador de documentos PDF.

## Instalación

Laravel TCPDF es un servicio que puede ser instalado via [composer](http://getcomposer.org) mediante el siguiente comando:
```json
  composer require villca/tcpdf-laravel
```
# Laravel 6.*
Para Laravel 6.* tienen que agregar en el archivo `composer.json`.

```json
{
    "require": {
        "villca/tcpdf-laravel": "6.0.*"
    }
}
```

# Laravel 5.*
Para Laravel 5.* tienen que agregar en el archivo `composer.json`.

```json
{
    "require": {
        "villca/tcpdf-laravel": "2.0.*"
    }
}
```
## Configuración 
Agregar en provider y alias en `config/app.php`.

```php
'providers' => [
    //...
    Villca\TCPDF\ServiceProvider::class,
]

//...

'aliases' => [
    //...
    'PDF' => Villca\TCPDF\Facades\TCPDF::class
]
```
Crea el archivo `tcpdf.php`
```json
  php artisan vendor:publish
```
ahora accede `config/tcpdf.php` para modificarlo.

!!eso es todo ahora a generar PDF's.

## Ejemplo

```php
<?php

namespace App\Http\Controllers;

use PDF;

class ReportesController extends Controller
{
    public function index()
    {
              PDF::SetTitle('Hola Mundo');
              PDF::AddPage();
              PDF::Write(0, 'Bienvenido a TCPDF-Laravel');
              PDF::Output('hola_mundo.pdf');
    }
}
```
Para mayor información acerca de las funciones de TCPDF en: [TCPDF Documentación](http://www.tcpdf.org/doc/code/classTCPDF.html)

## Importante

Los archivos de ejemplos estan en`vendor/tecnickcom/tcpdf/examples`.


## Créditos

Basado en [tecnickcom/tcpdf](https://github.com/tecnickcom/tcpdf)

## Contactos

 [Facebook](https://www.facebook.com/JhessuVillca)
