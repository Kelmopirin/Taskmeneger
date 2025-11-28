![[bin/Pasted image 20251128222011.png]]
# UML Kapcsolatok Python Példákkal

## 1. Directed Association (irányított asszociáció)

``` python
class Teacher:
    def __init__(self, name):
        self.name = name

class Student:
    def __init__(self, name, teacher):
        self.name = name
        self.teacher = teacher  # irányított kapcsolat
```

## 2. Inheritance (öröklődés)

``` python
class Animal:
    def speak(self):
        return "..."

class Dog(Animal):
    def speak(self):
        return "Woof!"
```

## 3. Composition (kompozíció)

``` python
class Engine:
    def start(self):
        print("Engine started")

class Car:
    def __init__(self):
        self.engine = Engine()  # Car owns Engine completely
```

## 4. Realization / Implementation (megvalósítás interfész alapján)

``` python
from abc import ABC, abstractmethod

class Worker(ABC):
    @abstractmethod
    def work(self):
        pass

class Programmer(Worker):
    def work(self):
        print("Writing code")
```

## 5. Aggregation (aggregáció)

``` python
class Book:
    def __init__(self, title):
        self.title = title

class Library:
    def __init__(self, books):
        self.books = books  # könyvek létezhetnek a Library-től függetlenül
```

## 6. Dependency (függőség)

``` python
class Printer:
    def print_document(self, text):
        print(text)

class Report:
    def generate(self, printer: Printer):
        printer.print_document("Generating report...")
```




# Ábrázolás
![[bin/Pasted image 20251128231457.png]]

### Itt az association nem irányított ezért nem rajzolunk nyilat vagyis:

``` python
class Course:
    def __init__(self, name):
        self.name = name
        self.students=[] # tanulók listája

class Student:
    def __init__(self, name):
        self.name = name
        self.courses=[]  # kurzusok listája
```
