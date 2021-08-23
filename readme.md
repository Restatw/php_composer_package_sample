## 建立 Packages 專案



```sh
composer init
```

```json
## add to main composer.json
    "autoload-dev": {
        "psr-4": {
            "Tests\\": "tests/",
            "GameBackend\\Contact\\": "packages/contact/src"
        }
    }
```

```php
## add to config/app.php
    return [
    # ...
        'providers' => [
            # ...
            GameBackend\Contact\ContactServiceProvider::class,
            # ...
        ]
    # ...
    ];
```
