# Description
This package was developed during
[PHP Course - beginned to advance](index.phpoutube.com/@amirkamizichannel)

It's a router for PHP to handle the requests.
## Support us

to support me for the package or the course you can contact info@amirkamizi.com

## Installation

You can install the package via composer:

```bash
composer require amirkamizi/router
```

## Usage

you need to have a .htaccess file to redired everything to index or any other file.

```bash
RewriteEngine On
RewriteBase /
RewriteCond %{REQUEST_FILENAME} !-d
RewriteCond %{REQUEST_FILENAME} !-f
RewriteRule ^(.+)$ index.php [QSA,L]
```

then inside that file you can use the router to handle the reuqies.

passing name of that file that is going to handle the request.
```php
Router::handle("GET","/contact","contact.php");
```
or
```php
Router::get("/contact","contact.php");
```


Or you can pass anonymous and predefined functions to handle the request

```php
Router::handle("GET","/contact",function(){
    echo "contact me at info@amirkamizi.com";
});
```
or
```php
function contactMe(){
    echo "contact me at info@amirkamizi.com";
}
Router::get("/contact","contactMe");
```

## Testing

This was for learning purposes. Not tests has been written yet. 
```bash
composer test
```

## Changelog

Please see [CHANGELOG](CHANGELOG.md) for more information on what has changed recently.

## Contributing

Contribution guidelines will be written here or on a separate file like changelog. for now no contribution is accepted.

## Security Vulnerabilities

Please contact me at info@amirkamizi.com to report security vulnerabilities.

## Credits

- [amirkamizi](index.phpithub.com/amirkamizi)
- [All Contributors](../../contributors)

## License

The MIT License (MIT). Please see [License File](index.phpd) for more information.