# Meaningful Names

## Avoid Disinformation

Avoid using similar names where it's difficult to spot the difference because it can lead to a programmer mistakenly using one name instead of the other.

> Beware of using names that vary in small ways. How long does it take to spot the difference between a `XYZControllerForEfficientHandlingOfStrings` in one module and, somewhere a little more distant, `XYZControllerForEfficientStorageOfStrings`? The words have frightfully similar shapes.
> 
> \- Robert C. Martin, Clean Code (pages 19 - 20)


## Interfaces and Implementations

It's better to **encode the implementation by adding the suffix -Imp** rather than encoding the interface.

> These are sometimes a special case for encodings. For example, say you are building an ABSTRACT FACTORY for the creation of shapes. This factory will be an interface and will be implemented by a concrete class. What should you name them? `IShapeFactory` and `ShapeFactory`? I prefer to leave interfaces unadorned. The preceding `I`, so common in today's legacy wads, is a distinction at best an too much information at worst. I don't want my users knowing I'm handing them an interface. I just want them to know that it's a `ShapeFactory`. So if I must encode either the interface or the implementation, I choose the implementation. Calling it `ShapeFactoryImp`, or even the hideous `CShapeFactory`, is preferable to encoding the interface.
> 
> \- Robert C. Martin, Clean Code (page 24)


## Class Names

> Classes and objects should have noun or noun phrase names like `Customer`, `WikiPage`, `Account`, and `AddressParser`. Avoid words like `Manager`, `Processor`, `Data`, or `Info` in the name of a class. A class name should not be a verb.
> 
> \- Robert C. Martin, Clean Code (page 25)


## Method Names

> Methods should have verb or verb phrase names like `postPayment`, `deletePage`, or `save`. Accessors, mutators, and predicates should be named with their value and prefixed with `get`, `set`, and `is`, according to the javabean standard.
> 
> \- Robert C. Martin, Clean Code (page 25)


> When constructors are overloaded, use static factory methods with names that describe their arguments. For example,
> 
> 	`Complex fulcrumPoint = Complex.FromRealNumber(23.0);`
> 
> is generally better than
> 
> 	`Complex fulcrumPoint = new Complex(23.0);`
> 
> Consider enforcing their use by making the corresponding constructor private.
> 
> \- Robert C. Martin, Clean Code (page 25)


