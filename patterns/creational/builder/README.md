# Builder Design Pattern

![Builder Design Pattern UML Diagram](https://media.geeksforgeeks.org/wp-content/uploads/uml-of-builedr.jpg)

## Introduction

The Builder Design Pattern is a creational design pattern that separates the construction of a complex object from its representation. It allows you to create different representations of an object while keeping the construction process consistent.

## Intent

The main intent of the Builder Design Pattern is to:

- Separate the construction of a complex object from its representation.
- Create an object step by step, by providing a sequence of construction processes.
- Allow different representations of the same object to be created.

## Problem Statement

Consider a scenario where you need to create complex objects with many optional parameters. Using a constructor with a long list of parameters or multiple overloaded constructors can make the code difficult to read and maintain. Additionally, it may not be clear which parameters are mandatory and which are optional.

## Solution

The Builder Design Pattern solves this problem by introducing a separate "Builder" class responsible for constructing the object. The Builder class has methods for setting individual properties of the object and returns the constructed object when it's ready.

## Structure

The key components of the Builder Design Pattern are:

1. **Director:** This is an optional class that defines the order in which construction steps should be executed. It works with the Builder to construct the object.

2. **Builder:** This is an interface or abstract class that declares methods for building parts of the product. Concrete builders implement these methods.

3. **Concrete Builder:** These classes implement the Builder interface and provide specific implementations for constructing the product. They keep track of the state of the object being built.

4. **Product:** This is the complex object being constructed. It has many parts that are built by the Builder.

## Use Cases

- When you need to create complex objects with many optional parameters.
- When you want to ensure the immutability of the constructed object.
- When you want to make the code more readable by providing a fluent and expressive API for constructing objects.

## Pros and Cons

### Pros:

1. Separates the construction process from the representation, making it easier to create different representations of an object.
2. Provides clear control over the construction process.
3. Avoids telescoping constructors with numerous parameters.
4. Allows for the creation of immutable objects.

### Cons:

1. Requires creating a separate builder class, which may add complexity to the code.
2. The code can become verbose if many optional parameters are involved.

## Related Patterns

- **Abstract Factory Pattern:** The Builder pattern is often used with the Abstract Factory pattern. While the Builder focuses on constructing a single complex object, the Abstract Factory creates families of related objects.

## References

- [Builder - Refactoring Guru](https://refactoring.guru/design-patterns/builder)
- [Builder Design Pattern - Wikipedia](https://en.wikipedia.org/wiki/Builder_pattern)