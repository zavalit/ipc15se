# An Example Docker setup for a silexphp 
it was created just to show some running example for "Containerize your php setup" talk on IPC15se

### Prerequiements:
in order to get it run you need:
   - vagrant
   - ansible-playbook


### How-To
execute the following on your console:

    $ git clone https://github.com/zavalit/ipc15se 
    
    $ cd ipc5se

    $ vagrant up 
    # be pation, it can take a time


log you in

    $ vagrant ssh

and let install all silexphp dependencies

    $ docker exec opt_silexphp_1 /opt/devtools/composer.phar install


afterwords create an index.php in /opt/silexphp/.docker/app/public folder

then call  http://10.20.1.11/ in your browser and see what you expect to see from your index.php

#### nice part: you have a php-7 docker image there, let it hacked:!  

