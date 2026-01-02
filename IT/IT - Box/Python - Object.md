
> [!NOTE] Note
> In Python, all data (numbers, strings, lists, etc.) are objects.


# Object-Oriented Programming (OOP)
- **Object**:
	- Attribute: Information of Object
	- Method: Actions that Object can perform
- Objects with similar properties are grouped together in a **Class**.

## Mutable $ Immutable Data
> If `<obj1>` **is** `<obj2>` = **True**, `<obj1>` == `<obj2>` = **True**. The opposite is not true.
> A **is** B = **True** <=> `id(A)` = `id(B)`


| Immutable                                    | Mutable         |
| -------------------------------------------- | --------------- |
| int, float, complex, bool, str, range, tuple | list, set, dict |


## Classify Data Types

| Atom                      | Container                          | Iterable                                                      | Sequence |
| ------------------------- | ---------------------------------- | ------------------------------------------------------------- | -------- |
| int, float, complex, bool | Contains multiple other data objects inside<br>range, str, tuple, list, set, dict | Can used `in` and `for`<br>str, range, tuple, list, set, dict | Can used `in` and `for`; Access **index** <br>str,range,tuple,list         |


# Create Object & Class
```python
>>> class Hocsinh:
    name = "🧹Ziec nha zui ze"
    def show(self):
        print("Name =",self.name)
    def update(self,name):
        self.name = name
>>> hs = Hocsinh()
>>> hs.show()
>>> hs.update("Ban Loc Nguyen")
``` 

```python
class BanGhe:
	width = 100
	length = 180
	color = "Red"
	def changedim(self,color):
			slef.color = color
```

## dir()
When we create a new class, we create a new data type - User-initiated data type.
-`dir(<object or class\>)`: Show all properties and methods of the corresponding object and class

##  _init_()
Makes it easier to create objects with initial values:
```python
class Hocsinh:
	def __init__ (self, name,gender,country="VN" ):
		self.name = name
		self.gender = gender
	def show(self):
		print("Name =", self.name)
		print("Male =", self.gender)
hs1 = Hocsinh("Loc",1,)
hs1.show()
 ```

# Overloaded Operator
| **TOÁN TỬ**    | **BIỂU DIỄN** |     **HOẠT ĐỘNG**     |
|:-------------- |:-------------:|:---------------------:|
| Add            |    p1 + p2    |   `p1.__add__(p2)`    |
| Subtract       |    p1 - p2    |   `p1.__sub__(p2)`    |
| Multiple       |    p1 * p2    |   `p1.__mul__(p2)`    |
| Power          |   p1 ** p2    |   `p1.__pow__(p2)`    |
| Devide         |    p1 / p2    | `p1.__truediv__(p2)`  |
| Floor Division |   p1 // p2    | `p1.__floordiv__(p2)` |
| Modulo         |    p1 % p2    |   `p1.__mod__(p2)`    |
| Dịch trái      |   p1 << p2    |  `p1.__lshift__(p2)`  |
| Dịch phải      |   p1 >> p2    |  `p1.__rshift__(p2)`  |
| AND            |    p1 & p2    |   `p1.__and__(p2)`    |
| OR             |   p1 \| p2    |    `p1.__or__(p2)`    |
| XOR            |    p1 ^ p2    |   `p1.__xor__(p2)`    |
| NOT            |      ~p1      |   `p1.__invert__()`   |

# Inheritance
```python
class Parent:
    def __init__(self, x, y):
        self.x = x
        self.y = y

class Child(Parent):
    def __init__(self, x, y, z):
        super().__init__(x, y)  # Gọi __init__() của lớp cha
        self.z = z

child = Child(1, 2, 3)
print(child.x)  # Output: 1
print(child.y)  # Output: 2
print(child.z)  # Output: 3
```

# Encapsulation
Protecting data inside a class.
```python
class Person: 
	self._age = age # Protected property
	def __init__(self, name):  
		self.__name = name  
  
p1 = Person("Loc")  
print(p1.__name)  # This will cause an error
print(p1.get_age()) # Get private property value
```

# Inner Class
```python
class Outer:  
	def __init__(self):  
		self.name = "Outer"  
	class Inner:  
		def __init__(self):  
			self.name = "Inner"  

# Accessing Inner Class from the Outside
outer = Outer()  
inner = outer.Inner()  

# Accessing Outer Class from Inner Class
outer = Outer()  
inner = outer.Inner(outer)
```