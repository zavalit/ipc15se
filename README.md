# An Example Docker setup for a silexphp 
it was created just to show some running example for "Containerize your php setup" on IPC5se

### Prerequiements:
in order to get it run you need:
   - vagrant
   - ansible-playboot


### How-To
execute the following on your console:

    $ git clone https://github.com/zavalit/ipc15se 
    
    $ cd ipc5se

    $ vagrant up 
    # be pation, it can take a time


log you in

    $ vagrant ssh

and let install all silexphp dependecies

    $ docker exec opt_silexphp_1 /opt/devtools/composer.phar install


afterwords create an index.php in /opt/silexphp/.docker/app/public folder

then call  http://10.20.1.11/ in browser and see what you expect to see from your index.php



