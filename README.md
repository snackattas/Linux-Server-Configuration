# Basic information about server
  * IP address: 52.43.192.233
  * SSH port: 2200
  * url: [http://ec2-52-43-192-233.us-west-2.compute.amazonaws.com/](http://ec2-52-43-192-233.us-west-2.compute.amazonaws.com/)
  * I logged into the server using the udacity_key.rsa, but for practice I generated my own public/private key and used that one instead.  I also disabled root login.  So the private key will be included in this repo.
      * **the file is id_rsa and the password is grader**
      * So the signature to get into the server is: `ssh -p 2200 grader@52.43.192.233`
  * My catalog app/the python packages are in a virtualenv, and use .wsgi files and .conf files as a result.   
    * I basically followed this [guide](https://github.com/stueken/FSND-P5_Linux-Server-Configuration) of a fellow Udacity student in building the server, except, without adding many of the extra features he added. 
    * I thought putting the catalog in its own virtualenv would be good practice if I ever wanted a single server to share many projects.
  * the github repo of my [catalog project](https://github.com/snackattas/LizardApp) 

# Software installed
  * I have included the results from `pip list` and `apt list --installed` in this git repo, but I realize those are lists of automatically included packages, and dependencies of packages I explicitly downloaded, so it's hard to tell what I actually did. 
  * Going through my .bash_history file is a jumbled mess because I often logged in and out of the server and of grader, and I do a lot of directory hopping and `sudo service apache2 restart` to check my configurations.  So I'll list the things I explicitly installed here
  * For Ubuntu (via apt-get):
      * Well I didn't download anything new to change the TZ to UTC but I did reconfigure a package with `sudo dpkg-reconfigure tzdata`
      * apache2
      * python-setuptools
      * libapache2-mod-wsgi
      * git
      * python-dev
      * python-pip
      * postgresql
      * python-psycopg2
      * python-sqlalchemy
  * For Python (via pip):
      * werkzeug
      * flask
      * oauth2client
      * requests
      * http2lib
      * MagickWand
      * Wand
      * SQLAlchemy-ImageAttach
      * Flask-SQLAlchemy
      * pytz
      * SQLAlchemy
      * virtualenv

# Third party resources
  * I really followed that guide very closely 
  * The forums were very helpful! Had trouble with getting apache to run with my app and not the sample page.  Also the typical filepath issues with templates not being founud and clientSecrets not being found.  Other than that, it was smooth sailing!
 
