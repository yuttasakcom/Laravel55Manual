# Laravel 5.5.\* Manual

## Table of Contents

* [Streamlined Request Validation](#streamlined-request-validation)
* [Fresh Migrations](#fresh-migrations)

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

> Dropped all tables

```bash
php artisan migrate:fresh
```
