## What is DI?

A concept that allows a developer to create and entire codebase comprised of loosely coupled code.

### Benefits of DI

- Late binding: Able to swap components out at runtime instead of compile time.
- Extensibility: Able to extend the functionality of a class while adhering to single resposibility. Open/closed principle
- Parallel Development: Agree on shared interface, implement classes seperately.
- Maintainability: Clearly defined responsibilities makes it easy to see where changes need to be made. Often requires new classes and new composition.
- Testability: Loosely coupled code allows the developer to test the class in isolation independant from the system by injecting test double to an interface.

### How to DI

- Create Seams
  - Volatile vs Stable Dependencies
  - Volatile if needs config/setup, does not exist yet, can only be installed in Prod env, or underministic results.
  - Examples: DateTime.Now, Databases, Queues, CRM system, expensive calc engine with expensive license, random number generators, etc.
- Object composition
- Object lifetime: singleton, request, transient
- Interception/Decorator pattern/Aspect Oriented Programming

#### The DI Container

- DI Container vs Poor Mans DI
- Configuring the container
  - Auto wiring
  - XML config (aka late binding)
  - Code as configuration
- Composition root
- Register -> Resolve -> Release

#### DI Patterns

- Constructor Injection: Default choice. Not present in base class libraries
- Others: Property Injection, Method Injection, Ambient Context

#### DI Refactorings

- Mapping Runtime values to abstractions - Abstract factory
- Working with short lived dependencies.
- Resolving Cyclic Dependencies
- Constructor overinjection
