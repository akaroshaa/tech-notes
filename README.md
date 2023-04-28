# to connect mysql with python

pip install mysql-connector-python

import mysql.connector

conn = mysql.connector.connect(host="localhost", user="root", password="root", database="sales", auth_plugin="mysql_native_password")
