How to run the project?
=======================

This example is explained in
the post
[Symfony/BDD example 05: CRUD](http://by-examples.net/2015/01/02/bdd-example-crud.html).

##1. Preliminary step

First, you need to create and install Vagrant box
named `symfony-v0.4.4`. You will find the instruction
in the post titled
[Generating symfony-v0.4.4 box](http://by-examples.net/2014/12/23/generating-symfony-0-4-4-box.html).

##2. Running the example

    $ git clone https://github.com/by-examples/symfony-bdd-example-05-crud.git
    $ cd symfony-bdd-example-05-crud
    $ vagrant up
    $ vagrant ssh
    $ composer install -o
    $ php app/console doctrine:schema:update --force

##3. Running the tests

    $ vagrant ssh
    $ php app/console cache:clear --env=prod
    $ bin/behat

##4. Visit the application with the browser

Now, you can run the web browser and visit:

    http://localhost:8880/admin/river
    http://localhost:8880/app_dev.php/admin/river

