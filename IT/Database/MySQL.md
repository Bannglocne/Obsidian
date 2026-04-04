#database 
# Python
```bash
-m pip install mysql-connector-python
```

```python
import mysql.connector
mydb = mysql.connector.connect(  
	host="localhost",  
	user="yourusername",  
	password="yourpassword"
	database="mydatabase"
)
mycursor = mydb.cursor()

sql =" " # MySQL statements
val = [ ] # Data used in SQL statements

mycursor.execute(sql, val)  # Run MySQL statments

myresult = mycursor.fetchall() # Get all rows
myresult = mycursor.fetchone() # Get only the next row from the result

mydb.commit()  # Require to make the changes
```