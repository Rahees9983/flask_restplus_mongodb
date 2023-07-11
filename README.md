# FlaskRestPlus_MongoDB

This project is using FlaskRestPlus to do CURD operation on MongoDB using pymongo.

1. You can execute this code in three ways
   a. On localhost (you have to install MongoDB on your localhost)
   b. Using docker
   c. Using Kubernetes

Commands used to execute on Localhost OS used on the machine/VM is Ubuntu 20.04LTS

1. Install MongoDB
     $ sudo apt-get install gnupg curl
   $ curl -fsSL https://pgp.mongodb.com/server-6.0.asc | \
   sudo gpg -o /usr/share/keyrings/mongodb-server-6.0.gpg \
   --dearmor

   $ echo "deb [ arch=amd64,arm64 signed-by=/usr/share/keyrings/mongodb-server-6.0.gpg ] https://repo.mongodb.org/apt/ubuntu focal/mongodb-org/6.0 multiverse" | sudo tee /etc/apt/sources.list.d/mongodb-org-6.0.list

   $ sudo apt-get update

   $ sudo apt-get install -y mongodb-org
   $ sudo systemctl start mongod
   $ sudo systemctl enable mongod
   $ sudo systemctl status mongod

2. Creating a  python Virtual environment
    $ pip install virtualenv
    $ virtualenv -p /usr/bin/python3 flask_venv
    $ source flask_venv/bin/activate
    $ pip3 install -r requirements.txt
    $ pip install markupsafe==2.0.1
    $ python3 app.py

