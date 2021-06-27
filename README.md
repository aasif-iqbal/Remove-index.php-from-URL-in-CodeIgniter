# Remove-index.php-from-URL-in-CodeIgniter

1. Create a .htaccess file in our project’s root directory or CodeIgniter directory.

```php
RewriteEngine On
RewriteCond %{REQUEST_FILENAME} !-f
RewriteCond %{REQUEST_FILENAME} !-d
RewriteRule ^(.*)$ index.php/$1 [L]
```

2. Removing index.php file
- Open the config.php file in your text editor and remove index.php from here.

###### Change:
```
$config['index_page'] = "index.php";
```

###### To:
```
$config['index_page'] = ''
```

###### Also Change:
```
$config['uri_protocol'] = "AUTO";

```

###### To:
```
$config['uri_protocol'] = "REQUEST_URI";
```

3. Restart Apache Web Server (XAMPP)
![Restart_server](https://user-images.githubusercontent.com/54746639/123535133-af5dbe80-d73f-11eb-82c0-1febf97e91b0.png)

