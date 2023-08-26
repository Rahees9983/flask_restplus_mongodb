# FlaskRestPlus_MongoDB

## This documentation guides you in setting up CURD operations on MongoDB using flask, pymongo, swagger and FlaskRestPlus.
#### You can execute this code in three different ways
   * a. On localhost (you have to install MongoDB on your localhost)
   * b. Using docker
   * c. Using Kubernetes

### a. Commands used to execute on Localhost OS used on the machine/VM is Ubuntu 20.04LTS

##### 1. Install MongoDB Community Edition
Follow these steps to install MongoDB Community Edition using the apt package manager.
###### Import the public key used by the package management system
```
sudo apt-get install gnupg curl
curl -fsSL https://pgp.mongodb.com/server-6.0.asc | \
sudo gpg -o /usr/share/keyrings/mongodb-server-6.0.gpg \
--dearmor
```
###### Create a list file for MongoDB
```
echo "deb [ arch=amd64,arm64 signed-by=/usr/share/keyrings/mongodb-server-6.0.gpg ] https://repo.mongodb.org/apt/ubuntu focal/mongodb-org/6.0 multiverse" | sudo tee /etc/apt/sources.list.d/mongodb-org-6.0.list

```
###### Reload local package database
```
sudo apt-get update
```
###### Install the MongoDB packages
```
sudo apt-get install -y mongodb-org
```
###### Run MongoDB Community Edition
```
sudo systemctl start mongod
```
If you receive an error similar to the following when starting mongod:

Failed to start mongod.service: Unit mongod.service not found.

Run the following command first:
```
sudo systemctl daemon-reload
```
###### Verify that MongoDB has started successfully
```
sudo systemctl status mongod
```
You can optionally ensure that MongoDB will start following a system reboot by issuing the following command:
```
sudo systemctl enable mongod
```
##### 2. Installing python virtual environment
```
apt install python3-pip
apt install python3-virtualenv
```

##### 3. Creating a  python Virtual environment on your localhost
```
virtualenv -p /usr/bin/python3 flask_venv
source flask_venv/bin/activate
```
##### 4. Clone the git repository for source code
```
git clone https://github.com/Rahees9983/flask_restplus_mongodb.git
cd flask_restplus_mongodb
pip3 install -r requirements.txt
pip install markupsafe==2.0.1
```
##### 5. Run the Flask application on the localhost
```
python3 app.py
```
