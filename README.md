# composer
Composer is a tool for dependency management in PHP. It allows you to declare the libraries your project depends on and it will manage (install/update) them for you. just like maven in java and npm im javascript

# How to install composer in windows
- [Get composer](https://getcomposer.org/doc/00-intro.md#installation-windows)
- click the Composer-Setup.exe button
- Open the Composer-Setup.exe and only press next, next until composer is installed
- Restart your machine
- And now you can use any composer command in any directory in your machine.

# Composer commands
- Initialized composer
```
composer init
```

- Require a library
```
composer require <vendor/package>
```

- Install libraries
```
composer install
```

- Update libraries
```
composer update
```

- Update autoloader
```
// For development
composer dump-autoload

// For production
composer dump-autoload -o
// o stands for optimize
```
###### Run this everytime you change the autoload property in composer.json to reload the autoloader

# What is autoloader
- Autoloader is process of loading(including/ requiring) all the .php files in our entire project so that we can just use namespaces to reuse our code.

#### We can just require_once the vendor/autoload.php in index.php to use our dependencies code in our entire project.
```
require_once __DIR__ . "<path>/vendor/autoload.php";
```

#### Include the autoloader in our composer.json file to load our project sourcr code.
```
"autoload": {
   "psr-4": {
       "<projectName>\\": "src/"
   }
}
```

# What is superglobals
- It is accesible anywhere throughout our whole project regardless of the scope.

# What is packagist.org
[Packagist.org](https://packagist.org/) is like the maven repository in java where you can see the dependencies available to be downloaded.

# Project Structure
[Basic project structure](https://github.com/sudeep611/PHP_Project_Getting_Started)
