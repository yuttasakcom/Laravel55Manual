# Laravel 5.5.\* Manual

## Table of Contents

* [Streamlined Request Validation](#streamlined-request-validation)
* [Fresh Migrations](#fresh-migrations)
* [Frontend Presets](#frontend-presets)
* [Automatic Package Discovery](#automatic-package-discovery)

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
