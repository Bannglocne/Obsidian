
# Python
```bash
-m pip install mysql-connector-python
```
**Create Connection**
```python
import mysql.connector
mydb = mysql.connector.connect(  
	host="localhost",  
	user="yourusername",  
	password="yourpassword"
	database="mydatabase"
)
```

**Create Database + Table**
```python
mycursor = mydb.cursor()    
mycursor.execute("CREATE DATABASE mydatabase")
mycursor.execute("CREATE TABLE customers (id INT AUTO_INCREMENT PRIMARY KEY, name VARCHAR(255), address VARCHAR(255))")
```

**Insert Into**
```python
sql = "INSERT INTO customers (name, address) VALUES (%s, %s)"  
val = [
	("Loc", "Hanoi") ,
	 ("Pham Hang", "Hanoi")
 ]
mycursor.execute(sql, val)  
mydb.commit()  # Require to make the changes
```

**Select**
```python
mycursor.execute("SELECT name, address FROM customers")
myresult = mycursor.fetchall()
myresult = mycursor.fetchone() # return the first row of the result
```

**Where**
```python
sql = "SELECT * FROM customers WHERE address = %s"  
adr = ("Yellow Garden 2", )  
mycursor.execute(sql, adr)  
myresult = mycursor.fetchall()
```