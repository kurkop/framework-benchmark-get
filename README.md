framework-benchmark-get
=======================

Framework benchmark. **Hello world (GET)**

###Clone:

    git clone https://github.com/kurkop/framework-benchmark-get
    
###Test with httpload

The test of framework benchmark is deploy with [httpload](https://github.com/perusio/httpload). You can install:

    git clone https://github.com/perusio/httpload
    cd httpload
    make & make install

By test the benchmark framework is advisable to use two computers, one run the framework and other the test httpload (_Clone in two pcs_).

###Run the frameworks:

Mojolicious (port 3000):

    cd mojolicious
    morbo hello.pl
    
Node express (port 4000):

    cd node/express/
    node server.js

Rails (port 6000):

    cd rails/myapp/
    rails server -p 6000

Django (port 8000):

    cd django
    python manage.py runserver 0.0.0.0:8000
