## Polymorphism ##

## 1. What does the word 'polymorphism' mean?
Many forms.

## 2. What does it mean when we apply polymorphism to OO design? Give a simple Java example.
We can use the same method in multiple classes (by implementing an interface) and keep the code DRY.

In the theme park example, ISecurity implements a boolean method isAllowedTo which takes in an instance of the visitor object and is used in two different classes to allow different things (only allowing children under 15 into the playground, and only allowing adults over 18 to the tobacco stall).

# From the ISecurity interface
public interface ISecurity { boolean isAllowedTo(Visitor visitor); }

# From the class Playground
public boolean isAllowedTo(Visitor visitor) { return visitor.getAge() <= 15; }

# From the class TobaccoStall
public boolean isAllowedTo(Visitor visitor) { return visitor.getAge() >= 18; }

## 3. What can we use to implement polymorphism in Java?
Abstract classes and Interfaces.

## 4. How many 'forms' can an object take when using polymorphism?
As many as you can think of.

## 5. Give an example of when you could use polymorphism.
When you want to use Method Overloading(to have more than one method with the same name that can take in different variables and produce different results).

## Composition ##

## 6. What do we mean by 'composition' in reference to object-oriented programming?
Composition means a class file references one or more objects that are used in other class files as instance variables.

## 7. When would you use composition? Provide a simple example in Java.
When you need to call an instance from a different class file. The example below adds a Car object to the Customer's possession using an instance of vehicle class.

# From the class Customer
public void addVehicle(Car car) { this.vehicles.add(car); }

## 8. What is/are the advantage(s) of using composition?
More flexible design. You can reuse existing code.

## 9. When an object is destroyed, what happens to all the objects it is composed of?
They are all destroyed too.
