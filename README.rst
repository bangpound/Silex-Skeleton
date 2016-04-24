!&# Silex Skeleton
==================

Welcome to !&# Silex Skeleton - a fully-functional Silex application that
you can use as the skeleton for your new applications. We use this as a
platform for learning and experimentation.

This document contains information on how to start using the Silex Skeleton.

Creating a Silex Application
----------------------------

Silex uses `Composer`_ to ease the creation of a new project:

.. code-block:: console

    $ composer create-project bangpound/silex-skeleton path/to/install ~1.0@dev

Composer will create a new Silex project under the `path/to/install` directory.

If your application will serve static assets using the PHP built-in web server
during development, you should add these lines to the top of `web/index_dev.php`:

.. code-block:: php

    if (php_sapi_name() === 'cli-server' && is_file(__DIR__.preg_replace('#(\?.*)$#', '', $_SERVER['REQUEST_URI']))) {
        return false;
    }

Browsing the Demo Application
-----------------------------

Congratulations! You're now ready to use Silex.

To see a real-live Silex page in action, start the PHP built-in web server with
command:

.. code-block:: console

    $ cd path/to/install
    $ COMPOSER_PROCESS_TIMEOUT=0 composer run

Then, browse to http://localhost:8888/index_dev.php/

Running tests
-------------

.. code-block:: console

    $ cd path/to/install
    $ composer test

Getting started with Silex
--------------------------

This distribution is meant to be the starting point for your Silex applications.

A great way to start learning Silex is via the `Documentation`_, which will
take you through all the features of Silex.

What's inside?
---------------

The Silex Skeleton is configured with the following service providers:

* `UrlGeneratorServiceProvider`_ - Provides a service for generating URLs for
  named routes.

* `ServiceControllerServiceProvider`_ - As your Silex application grows, you
  may wish to begin organizing your controllers in a more formal fashion.
  Silex can use controller classes out of the box, but with a bit of work,
  your controllers can be created as services, giving you the full power of
  dependency injection and lazy loading.

* `HttpFragmentServiceProvider`_ - Provides fragment rendering in templates.

* `AssetServiceProvider`_ - Provides versioned URLs of front end assets.

* `TwigServiceProvider`_ - Provides integration with the Twig template engine.

* `WebProfilerServiceProvider`_ - Enable the Symfony web debug toolbar and
  the Symfony profiler in your Silex application when developing.

* `MonologServiceProvider`_ - Enable logging in the development environment.

* `VarDumperServiceProvider`_ - Integrates Twig and the VarDumper component.

Read the `Providers`_ documentation for more details about Silex Service
Providers.

Enjoy!

.. _Composer: http://getcomposer.org/
.. _Documentation: http://silex.sensiolabs.org/documentation
.. _UrlGeneratorServiceProvider: http://silex.sensiolabs.org/doc/master/providers/url_generator.html
.. _ServiceControllerServiceProvider: http://silex.sensiolabs.org/doc/master/providers/service_controller.html
.. _HttpFragmentServiceProvider: http://silex.sensiolabs.org/doc/master/providers/http_fragment.html
.. _AssetServiceProvider: http://silex.sensiolabs.org/doc/master/providers/asset.html
.. _TwigServiceProvider: http://silex.sensiolabs.org/doc/master/providers/twig.html
.. _WebProfilerServiceProvider: http://github.com/silexphp/Silex-WebProfiler
.. _MonologServiceProvider: http://silex.sensiolabs.org/doc/master/providers/monolog.html
.. _VarDumperServiceProvider: http://silex.sensiolabs.org/doc/master/providers/var-dumper.html
.. _Providers: http://silex.sensiolabs.org/doc/providers.html
