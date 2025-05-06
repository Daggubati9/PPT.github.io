## 1.🧠 OOPs Concepts:-

## a. Class
A blueprint for creating objects.

Defines properties (variables) and methods (functions).

Example:

python
Copy
Edit
class Car:
    def __init__(self, model):
        self.model = model
## b. Object
A real-world instance of a class.

Example:

python
Copy
Edit
my_car = Car("Toyota")
## c. Encapsulation
Hides internal data and shows only what's necessary.

Achieved using private variables and getters/setters.

Protects data from unauthorized access.

## d. Abstraction
Shows only essential features, hides details.

Example: You use a car without knowing how the engine works.

In code, done using abstract classes or interfaces.

## e. Inheritance
Allows a class (child) to use properties and methods of another class (parent).

Promotes code reuse.

Example:

python
Copy
Edit
class Vehicle:
    def move(self): print("Moving")

class Car(Vehicle):
    pass
## f. Polymorphism
Same method name, but different behavior depending on object.

Two types:

Compile-time (method overloading) – limited in Python

Run-time (method overriding)

Example:

python
Copy
Edit
class Animal:
    def speak(self): print("Animal sound")

class Dog(Animal):
    def speak(self): print("Bark")
## 🔁 Summary Table:
Concept	Meaning	Key Benefit
Class	Template for creating objects	Structure
Object	Instance of a class	Real-world modeling
Encapsulation	Hides data	Data protection
Abstraction	Shows essentials, hides complexity	Simplifies interface
Inheritance	Child class uses parent class logic	Code reuse
Polymorphism	Many forms of one function	Flexibility
