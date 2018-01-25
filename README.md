# Laravel 5.5.\* Manual

> Full Stack PHP Framework

## Table of Contents

* [การติดตั้ง laravel](#installation)
* [Streamlined Request Validation](#streamlined-request-validation)
* [Fresh Migrations](#fresh-migrations)
* [Frontend Presets](#frontend-presets)
* [Automatic Package Discovery](#automatic-package-discovery)

## Installation

```
# การติดตั้ง Laravel ทำได้หลายวิธี แต่วิธีที่ขอแนะนำคือติดตั้งผ่าน composer
# คำสั่งติดตั้ง Laravel ผ่าน composer
composer create-project --prefer-dist laravel/laravel your-name-prorject
```

## Streamlined Request Validation

```php
...
    $post = request()->validate([
        'title' => 'required',
        'body' => 'required'
    ]);

    \App\Post::forceCreate($post);

    return 'Done';
...
```

## Fresh Migrations

```bash
php artisan migrate:fresh
```

## Frontend Presets

```bash
php artisan preset none|bootstrap|vue|react
```

## Automatic Package Discovery

```json
...
"extra": {
    "laravel": {
        "providers": [
            "App\\Providers\\YourServiceProvider"
        ],
        "alias": {
            "YourAlias": "App\\Facades\\YourFacade"
        }
    }
}
...
```
