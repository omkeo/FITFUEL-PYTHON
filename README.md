
----------------------------------------------------------------------------------------------------------------------------------------------------------
1.Update the package lists
sudo apt update
----------------------------------------------------------------------------------------------------------------------------------------------------------
2.Install Python 3 and pip
sudo apt install python3 python3-pip
----------------------------------------------------------------------------------------------------------------------------------------------------------
3.Install Flask, MySQL Connector, and Werkzeug using APT
sudo apt install python3-flask python3-mysql.connector python3-werkzeug
----------------------------------------------------------------------------------------------------------------------------------------------------------
4. Install MySQL client (to connect to your MySQL RDS)
sudo apt install mysql-client
----------------------------------------------------------------------------------------------------------------------------------------------------------
5.Connect to MySQL RDS instance
mysql -h database-1.c5oaaia40odt.ap-south-1.rds.amazonaws.com -u <your-mysql-username> -p
----------------------------------------------------------------------------------------------------------------------------------------------------------
6. Create the database and table (if not created already)
CREATE DATABASE user_db;

USE user_db;

CREATE TABLE users (
    id INT AUTO_INCREMENT PRIMARY KEY,
    name VARCHAR(100),
    email VARCHAR(100) UNIQUE,
    password VARCHAR(255)
);
----------------------------------------------------------------------------------------------------------------------------------------------------------

cd ~/FITFUEL


Run the Flask application

python3 app.py


http://<EC2_PUBLIC_IP>:5000
