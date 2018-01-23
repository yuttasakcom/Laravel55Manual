# Laravel 5.5.\* Manual

## Table of Contents

* [Streamlined Request Validation](#streamlined-request-validation)

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
