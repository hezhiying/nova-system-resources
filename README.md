# A Laravel Nova tool to show system resources

This [Nova](https://nova.laravel.com) tool gives you a live overview of your RAM and CPU usage.

![screenshot of the backup tool](screenshot.png)

## Requirements

You must use either Linux or MacOS.

## Installation

You can install the nova tool in to a Laravel app that uses [Nova](https://nova.laravel.com) via composer:

```bash
composer require gijsg/nova-system-resources
```

Next up, you must register the tool with Nova. This is typically done in the `tools` method of the `NovaServiceProvider`.


```php
// in app/Providers/NovaServiceProvder.php

// ...

public function tools()
{
    return [
        // ...
        new \GijsG\SystemResources\SystemResources('ram'),
        new \GijsG\SystemResources\SystemResources('cpu'),
    ];
}
```

The MIT License (MIT). Please see [License File](LICENSE.md) for more information.