## 1.🧠 OOPs Concepts:-

🔹 1. Class
Blueprint or template for objects.

Defines attributes (variables) and behaviors (methods).

python
Copy
Edit
class Car:
    def __init__(self, brand):
        self.brand = brand
🔹 2. Object
Instance of a class.

Has its own copy of class properties.

python
Copy
Edit
my_car = Car("Toyota")
🔹 3. Encapsulation
Bundles data and methods that operate on the data.

Protects internal state using private variables (_var or __var).

python
Copy
Edit
class Person:
    def __init__(self, name):
        self.__name = name  # private

    def get_name(self):
        return self.__name
🔹 4. Abstraction
Hides complex implementation, shows only essentials.

Achieved via abstract classes or interfaces.

python
Copy
Edit
from abc import ABC, abstractmethod

class Animal(ABC):
    @abstractmethod
    def speak(self):
        pass
🔹 5. Inheritance
One class (child) inherits properties of another (parent).

Promotes reusability.

python
Copy
Edit
class Animal:
    def speak(self):
        print("Sound")

class Dog(Animal):
    def speak(self):
        print("Bark")
🔹 6. Polymorphism
One method behaves differently based on the object.

Achieved via method overriding or duck typing.

python
Copy
Edit
def animal_sound(animal):
    animal.speak()

animal_sound(Dog())  # Output: Bark

## 🔁 Summary Table:
| Concept       | Meaning                             | Key Benefit          |
| ------------- | ----------------------------------- | -------------------- |
| Class         | Template for creating objects       | Structure            |
| Object        | Instance of a class                 | Real-world modeling  |
| Encapsulation | Hides data                          | Data protection      |
| Abstraction   | Shows essentials, hides complexity  | Simplifies interface |
| Inheritance   | Child class uses parent class logic | Code reuse           |
| Polymorphism  | Many forms of one function          | Flexibility          |

