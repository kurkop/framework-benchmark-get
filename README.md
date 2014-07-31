framework-benchmark-get
=======================

Framework-benchmark-get is a framework benchmarking tool that tests the speed of frameworks serving a simple Hello world application using GET HTTP requests.

###Clone:

    git clone https://github.com/kurkop/framework-benchmark-get
    
###Test with httpload

The frameworks are benchmarked using [httpload](https://github.com/perusio/httpload). You can install it as follows:

    git clone https://github.com/perusio/httpload
    cd httpload
    make & make install

It is best to perform framework benchmarks using two computers. One to run the framework and the other to test using httpload (_Clone in two pcs_).

###To run the frameworks:

Mojolicious (port 3000):

    cd mojolicious
    morbo hello.pl
    
Node.js with express (port 4000):

    cd node/express/
    node server.js

Rails (port 6000):

    cd rails/myapp/
    rails server -p 6000

Django (port 8000):

    cd django
    python manage.py runserver 0.0.0.0:8000

### httpload gets "_Hello world_" from all the frameworks. Run httpload as follows:

>parallel: Numbers of process.

>seconds: Time of run

    cd http_test
    httpload -parallel 8 -seconds 10 port3000
    httpload -parallel 8 -seconds 10 port4000
    httpload -parallel 8 -seconds 10 port6000
    httpload -parallel 8 -seconds 10 port8000



