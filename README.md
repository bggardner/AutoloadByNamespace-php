AutoloadByNamespace-php
=======================

Class autoloader for PHP


Features
--------

- Handles autoloading of classes based on 'base' namespace


Dependencies
------------

- PHP 5.1.2+


Usage
-----

Each class you create should exist in its own file.  In the example below, Foo.php only contains the myNamespace\Foo class.

    <?php
      require_once 'AutoloadByNamespace.php';
      spl_autoload_register('AutoloadByNamespace::autoload');
      AutoloadByNamespace::register('MyNamespace', '/includes/classes');
      
      $foo = new myNamespace\Foo(); // Autoloads '/includes/classes/Foo.php'
    ?>

      
