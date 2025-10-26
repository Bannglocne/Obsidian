
# Lập trình hướng đối tượng (OOP)
- Đối tượng gồm 2 thành phần chính:
	- Thuộc tính (Attribute): là những thông tin, đặc điểm của đối tượng
	- Phương thức (Method): là những hành vi mà đối tượng có thể thực hiện
- Lớp là sự trừu tượng hóa của đối tượng. Những đối tượng có những đặc tính tương tự nhau sẽ được tập hợp thành một lớp.

# Khởi tạo Lớp và Đối tượng
- Lệnh tạo Lớp:
```python
class<Tên lớp>:
    <Phần mô tả lớp>
```
- Ví dụ chi tiết:
```python
>>> class Hocsinh:
    name = "🧹Ziec nha zui ze"
    age = 15
    gender = True
    school = "THPT Ngoc Hoi"
    def show(self):
        print("Name =",self.name)
        print("Age =",self.age)
        print("Male =",self.gender)
        print("School =",self.school)
    def update(self,name,age,gender,school):
        self.name = name
        self.age = age
        self.gender = gender
        self.school = school
>>> hs = Hocsinh()
>>> hs.show()
>>> hs.update("Ban Loc Nguyen", "18", "1", "HUST")
``` 

```python
class BanGhe:
	height = 60
	width = 100
	length = 180
	color = "Red"
	X = 0
	Y = 0
	def change(self,X,Y):
			self.X = X
			self.Y = Y
	def changecolor(self,color):
			self.color = color
	def changedim(self,height,width,length):
			self.height = height
			slef.width = width
			self.length = length
```
- Để truy cập thuộc tính cụ thể của đối tượng: `<Đối tượng>.<thuộc tính>`
- Thay đổi thuộc tính của đối tượng: `<Đối tượng>.<thuộc tính> = <giá trị mới>`
- Phương thức `update()` có chức năng thay đổi thuộc tính của đối tượng
	- Trong các tham số của phương thức này bắt buộc phải có tham số đóng vai trò là chủ thể biến đối tượng cần thay đổi (Có thể sử dụng **self** hoặc bất cứ tên nào khác)
- **self** là từ dùng để chỉ bản thân đối tượng

# Lệnh dir() và _init_()
- Khi tạo một lớp mới tức là chúng ta đã  tạo một kiểu dữ liệu mới - Kiểu dữ liệu do người dùng khởi tạo

## Lệnh dir()
- Cú pháp `dir(<đối tượng hoặc lớp>)`: Hiện tất cả thuộc tính và phương thức của đối tượng, lớp tương ứng
- Tát cả phương thức đều có tên cố định và không thể thay đổi, các thuộc tính và phương thức do ta tạo ra sẽ được liệt kê ở cuối
- Ví dụ:
```python
>>>dir(str)
['__add__', '__class__', '__contains__', '__delattr__', '__dir__', '__doc__', '__eq__', '__format__', '__ge__', '__getattribute__', '__getitem__', '__getnewargs__', '__getstate__', '__gt__', '__hash__', '__init__', '__init_subclass__', '__iter__', '__le__', '__len__', '__lt__', '__mod__', '__mul__', '__ne__', '__new__', '__reduce__', '__reduce_ex__', '__repr__', '__rmod__', '__rmul__', '__setattr__', '__sizeof__', '__str__', '__subclasshook__', 'capitalize', 'casefold', 'center', 'count', 'encode', 'endswith', 'expandtabs', 'find', 'format', 'format_map', 'index', 'isalnum', 'isalpha', 'isascii', 'isdecimal', 'isdigit', 'isidentifier', 'islower', 'isnumeric', 'isprintable', 'isspace', 'istitle', 'isupper', 'join', 'ljust', 'lower', 'lstrip', 'maketrans', 'partition', 'removeprefix', 'removesuffix', 'replace', 'rfind', 'rindex', 'rjust', 'rpartition', 'rsplit', 'rstrip', 'split', 'splitlines', 'startswith', 'strip', 'swapcase', 'title', 'translate', 'upper', 'zfill'])
```

## Lệnh _init_()
- Gán tự động thuộc tính cho đối tượng khi mới khởi tạo
- Chú ý: Phương thức _init_() cần có tham biến (self) đóng vai trò đối tượng được gán các thuộc tính ban đầu
- Ví dụ:
```python
class Hocsinh:
    def __init__ (self, name, age, gender, school):
        self.name = name
        self.age = age
        self.gender = gender
        self.school = school
    def show(self):
        print("Name =", self.name)
        print("Age =", self.age)
        print("Male =", self.gender)
        print("School =", self.school)
hs1 = Hocsinh("Loc",15,1,"THPT Ngoc Hoi")
hs1.show()
 ```

# Các toán tử chồng (Overloaded Operator)
- Là các toán tử +, -, x nhưng khi áp dụng trong các hoàn cảnh khác nhau thì sẽ được hiểu theo những cách khác nhau


| **TOÁN TỬ**                                | **BIỂU DIỄN** |    **HOẠT ĐỘNG**    |
|:------------------------------------------ |:-------------:|:-------------------:|
| Phép cộng                                  |    p1 + p2    |   `p1.__add__(p2)`    |
| Phép trừ                                   |    p1 - p2    |   `p1.__sub__(p2)`    |
| Phép nhân                                  |    p1 * p2    |   `p1.__mul__(p2)`    |
| Lũy thừa                                   |   p1 ** p2    |   `p1.__pow__(p2)`    |
| Phép chia                                  |    p1 / p2    | `p1.__truediv__(p2)`  |
| Phép chia lấy phần nguyên (Floor Division) |   p1 // p2    | `p1.__floordiv__(p2)` |
| Số dư (modulo)                             |    p1 % p2    |   `p1.__mod__(p2)`    |
| Thao tác trên bit: phép dịch trái          |   p1 << p2    |  `p1.__lshift__(p2)`  |
| Thao tác trên bit: phép dịch phải          |   p1 >> p2    |  `p1.__rshift__(p2)` |
| Thao tác trên bit: phép AND                |    p1 & p2    |   `p1.__and__(p2)`   |
| Thao tác trên bit: phép OR                 |   p1 \| p2    |    `p1.__or__(p2)`   |
| Thao tác trên bit: phép XOR                |    p1 ^ p2    |   `p1.__xor__(p2)`   |
| Thao tác trên bit: phép NOT                |      ~p1      |   `p1.__invert__()`   |

# Lớp con và tính kế thừa
- Các đối tượng có thể kế thừa nhau nếu chúng được sinh dựa trên các đối tượng khác có tính chất phổ quát hơn
- Cách tạo:
```python
class <tên lớp con>(<Lớp cha>):
    <Lệnh mô tả 1>
    ...
    <Lệnh mô tả N>
```
- Ví dụ:
```python
class Person: #Tạo lớp cha
    def __init__(self, name):  #Gán tự động thuộc tính
        self.name = name
    def greet(self):
        print("Hello, my name is", self.name)
class Student(Person):
    def __init__(self, name, student_id):
        super().__init__(name)
        self.student_id = student_id
    def study(self):
        print("I'm studying.")
# Tạo một đối tượng từ lớp con
student = Student("John", "12345")
# Gọi phương thức từ lớp cha
student.greet()  # Output: Hello, my name is John
# Gọi phương thức từ lớp con
student.study()  # Output: I'm studying.
```
- Hàm `super()` có tác dụng gọi phương thức của lớp cha từ một lớp con.

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