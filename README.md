# to connect mysql with python

pip install mysql-connector-python


import pandas as pd
import mysql.connector
conn = mysql.connector.connect(host="localhost", user="root", password="root", database="sales", auth_plugin="mysql_native_password")
df = pd.read_sql("select * from customers", conn)
df





# to connect mysql with python using SQLAlchemy

pip install "sqlalchemy<2.0"


import pandas as pd
import sqlalchemy as sq
conn = sq.create_engine("mysql+mysqlconnector://root:root@localhost:3306/sales")
df = pd.read_sql("customers", conn)
df
