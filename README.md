# unit-testing-samples
This repository is a collections of unit-testing code samples for both Backend and Frontend.

## What is the Testing Pyramid?
Introduced by Mike Cohn in his book `Succeeding with Agile (2009)`, the pyramid is a metaphor for thinking about testing in software. It’s an idea that has caught on so strongly that, to this day, it’s still the industry standard in engineering circles.

The pyramid attempts to visually represent a logical organization of testing standards. It consists of three distinct layers:

![Testing Pyramid](./pyramid.jpg)



### **Types of Testing?**
- **Unit Testing:** 
  - Test the individual blocks of an application such as a class or a function or a component.
  - Each unit is tested in isolation,independent of other units
  - Dependencies are mocked
  - Takes less time to test
  - Easy to write and maintain

- **Integration Testing:** 
  - Test the combination of units and ensure they are working together
  - Take more time than unit tests

- **End to End(E2E) Testing:** 
  - Test the entire application flow and ensure it works as designed from start to finish
  - Involve real UI, database, API
  - Take longest time
  - Cost implication as you interact with real api that maybe charged based on no. of requests.

  ---

**Unit tests are isolated and independent of each other**

+ Any given behaviour should be specified in **one and only one test**
+ The execution/order of execution of one test **cannot affect the others**

The code is designed to support this independence (see "Design principles" below).

**Unit tests are lightweight tests**

+ Repeatable
+ Fast
+ Consistent
+ Easy to write and read

**Unit tests are code too**

They should meet the same level of quality as the code being tested. They can be refactored as well to make them more maintainable and/or readable.



### Design principles

The key to good unit testing is to write **testable code**. Applying simple design principles can help, in particular:

+ Use a **good naming** convention and **comment** your code (the "why?" not the "how"), keep in mind that comments are not a substitute for bad naming or bad design
+ **DRY**: Don't Repeat Yourself, avoid code duplication
+ **Single responsibility**: each object/function must focus on a single task
+ Keep a **single level of abstraction** in the same component (for example, do not mix business logic with lower-level technical details in the same method)
+ **Minimize dependencies** between components: encapsulate, interchange less information between components
+ **Support configurability** rather than hard-coding, this prevents having to replicate the exact same environment when testing (e.g.: markup)
+ Apply adequate **design patterns**, especially **dependency injection** that allows separating an object's creation responsibility from business logic
+ Avoid global mutable state