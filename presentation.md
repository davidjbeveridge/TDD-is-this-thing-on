%title: Is this thing on? Testing JavaScript, 1, 2, 3.
%author: David Beveridge <davidjbeveridge@gmail.com>
%date: 2015-05-27






-> # An incomplete guide to TDD in JavaScript <-

-> David Beveridge <-

-> Originate, Inc. <-
-> www.originate.com <-



--------------------------------------------------------------------------------





-> # What will we cover? <-

* What is (and isn't) TDD?

* How do I TDD?

* Conclusion

--------------------------------------------------------------------------------





-> # What *won't* we cover? <-

* Performance Testing

* Regression Testing (at least, not in detail)

* Tool comparison

--------------------------------------------------------------------------------





-> # What is (and isn't) (T/B)DD? <-

--------------------------------------------------------------------------------





-> # What is (and isn't) (T/B)DD? <-

* The Big Lie


-> You have to write your tests *first* <-

--------------------------------------------------------------------------------





-> # What is (and isn't) (T/B)DD? <-

* The Big Lie



-> TDD == "Test Driven Development" <-

-> *What do you think of when someone says "test"?* <-


* SAT, ACT, CSAP
* SpaceX Test Launch
* Polygraph test
* Emissions testing
* Medical tests
* Metal purity tests (e.g., precious metals)

--------------------------------------------------------------------------------





-> # What is (and isn't) (T/B)DD? <-

* The Big Lie



-> TDD == "Test Driven Development" <-

-> *What do you think of when someone says "test"?* <-


* SAT, ACT, CSAP
* SpaceX Test Launch
* Polygraph test
* Emissions testing
* Medical tests
* Metal purity tests (e.g., precious metals)


What is testing?

Proving, measuring, or confirming the veracity, authenticity, performance,
safety, completeness, purity, or other qualities of a system.

--------------------------------------------------------------------------------





-> # What is (and isn't) (T/B)DD? <-

* The Big Lie



-> TDD == "Test Driven Development" <-

-> *How can you test something that doesn't exist?* <-

--------------------------------------------------------------------------------





-> # What is (and isn't) (T/B)DD? <-

* The Big Lie



-> TDD == "Test Driven Development" <-

-> How can you test something that doesn't exist? <-

-> You can't. But you can *specify behavior* for something you're <-
-> going to create before you create it. <-

--------------------------------------------------------------------------------





-> # What is (and isn't) (T/B)DD? <-

* The Big Lie



-> TDD == "Test Driven Development" <-

-> How can you test something that doesn't exist? <-

-> You can't. But you can *specify behavior* for something you're <-
-> going to create before you create it. <-

We specify behavior for things all the time:

* Penal Code
* School Rules
* Code of Conduct
* Terms of Service
* User Stories
* Acceptance Criteria

--------------------------------------------------------------------------------





-> # What is (and isn't) (T/B)DD? <-

* The Big Lie



-> TDD == "Test Driven Development" <-

-> How can you test something that doesn't exist? <-

-> You can't. But you can *specify behavior* for something you're <-
-> going to create before you create it. <-

We specify behavior for things all the time:

* Penal Code
* School Rules
* Code of Conduct
* Terms of Service
* User Stories
* Acceptance Criteria
* *Automated software suites*

--------------------------------------------------------------------------------













-> From here on out, I'll try to say *specifications*, or *specs* <-
-> instead of "tests", and *BDD* instead of "TDD". <-


-> (BDD = "Behavior-Driven Development") <-

--------------------------------------------------------------------------------





-> # What is (and isn't) BDD? <-

* Specifications for software's behavior
  - Writen before your implementation
* *Design Tool*

--------------------------------------------------------------------------------





-> # What is (and isn't) BDD? <-

* Specifications for software's behavior
  - Writen before your implementation
* *Design Tool*

Other design tools:

* Structured programming (e.g., `if/else`, `for` intead of GOTO)
* Declarative programming (tell the computer the prolem, not the solution)
  - SQL
  - Logic programming
  - Functional programming
* Code style guides (e.g., no methods longer than 10 lines)
* "Design Patterns" (ala the Gang of Four Book)
* Immutability (don't make changes to objects, ever)

All these tools introduce *extra constraints* on your solution' implementation

--------------------------------------------------------------------------------





-> # What is (and isn't) BDD? <-

* Specifications for software's behavior
  - Writen before your implementation
* *Design Tool*
  - Just another constraint on your implementation
  - Forces the public interface to be explicit
  - Helps you reason about the boundaries of your solution
  - Encourages loose coupling of objects
  - Automatic documentation

--------------------------------------------------------------------------------





-> # What is (and isn't) BDD? <-

* Specifications for software's behavior
  - Writen before your implementation
* Design Tool
* *Debugging Tool*

--------------------------------------------------------------------------------





-> # What is (and isn't) BDD? <-

* Specifications for software's behavior
  - Writen before your implementation
* Design Tool
* *Debugging Tool*
  - Does the refresh for you
  - Displays a stack trace
  - Single change at a time helps find bugs faster

--------------------------------------------------------------------------------





-> # What is (and isn't) BDD? <-

* Specifications for software's behavior
  - Writen before your implementation
* Design Tool
* Debugging Tool
* *Proof of correctness*

--------------------------------------------------------------------------------





> Today a usual technique is to make a program and then to test it. But: program
> testing can be a very effective way to show the presence of bugs, but is
> hopelessly inadequate for showing their absence. The only effective way to
> raise the confidence level of a program significantly is to give a convincing
> proof of its correctness. But one should not first make the program and then
> prove its correctness, because then the requirement of providing the proof
> would only increase the poor programmer’s burden. On the contrary: the
> programmer should let correctness proof and program grow hand in hand.
> Argument three is essentially based on the following observation. If one first
> asks oneself what the structure of a convincing proof would be and, having
> found this, then constructs a program satisfying this proof’s requirements,
> then these correctness concerns turn out to be a very effective heuristic
> guidance.

-- Edsger W. Dijkstra, The Humble Programmer (1972)

--------------------------------------------------------------------------------





-> # What is (and isn't) BDD? <-

* Specifications for software's behavior
  - Writen before your implementation
* Design Tool
* Debugging Tool
* Proof of correctness
  - Requires intelligible program requirements
  - Adequate proof of correct behavior (i.e., covers all edge cases)
  - Reasoned and written along with the program, not afterward

--------------------------------------------------------------------------------





-> # The Bad Parts <-

* *Jerks and Dogma ruin everything*

--------------------------------------------------------------------------------





-> # The Bad Parts <-

* Jerks and Dogma ruin everything
* *Learning Curve*

--------------------------------------------------------------------------------





-> # The Bad Parts <-

* Jerks and Dogma ruin everything
* *Learning Curve*
  - Tools
  - Thinking BDD
  - Refactoring
  - Design
  - Brittle vs. flexible specs

--------------------------------------------------------------------------------





-> # The Bad Parts <-

* Jerks and Dogma ruin everything
* Learning Curve
  - Tools
  - Thinking BDD
  - Refactoring
  - Design
  - Brittle vs. flexible specs
* *Test-first facists*

--------------------------------------------------------------------------------





-> # The Good Parts <-

* *Less remembering stuff*

--------------------------------------------------------------------------------





-> # The Good Parts <-

* Less remembering stuff
* *Fast feedback about your code*

--------------------------------------------------------------------------------





-> # The Good Parts <-

* Less remembering stuff
* Fast feedback about your code
* *Clear boundaries for refactoring*

--------------------------------------------------------------------------------





-> # The Good Parts <-

* Less remembering stuff
* Fast feedback about your code
* Clear boundaries for refactoring
* *(Some) assurance against regression*

--------------------------------------------------------------------------------





-> # The Good Parts <-

* Less remembering stuff
* Fast feedback about your code
* Clear boundaries for refactoring
* (Some) assurance against regression
* *A design document your team can read*

--------------------------------------------------------------------------------





-> # The Good Parts <-

* Less remembering stuff
* Fast feedback about your code
* Clear boundaries for refactoring
* (Some) assurance against regression
* A design document your team can read
* *Complements existing tools*

--------------------------------------------------------------------------------





-> # A tangent about existing tools... <-

--------------------------------------------------------------------------------





-> # Existing Tools: SOLID  <-

Introduced by Michael Feathers & Robert C. Martin

* *Single Responsibility Principle*
  - *A class should have only a single responsibility*
* Open/Closed Principle
  - Software entities should be open for extension, but closed for
    modification.
* Liskov Substitution Principle
  - Objects in a program should be replaceable with instances of their
    subtypes without altering the correctness of that program
* Interface Segregation Principle
  - Many client-specific interfaces are better than one general-purpose
    interface
* Dependency Inversion Principle
  - Depend upon Abstractions. Do not depend upon concretions

https://en.wikipedia.org/wiki/Solid_%28object-oriented_design%29
http://cleancoders.com/category/solid-principles#videos

--------------------------------------------------------------------------------





-> # Existing Tools: SOLID  <-

Introduced by Michael Feathers & Robert C. Martin

* Single Responsibility Principle
  - A class should have only a single responsibility
* *Open/Closed Principle*
  - *Software entities should be open for extension, but closed for*
    *modification.*
* Liskov Substitution Principle
  - Objects in a program should be replaceable with instances of their
    subtypes without altering the correctness of that program
* Interface Segregation Principle
  - Many client-specific interfaces are better than one general-purpose
    interface
* Dependency Inversion Principle
  - Depend upon Abstractions. Do not depend upon concretions

https://en.wikipedia.org/wiki/Solid_%28object-oriented_design%29
http://cleancoders.com/category/solid-principles#videos

--------------------------------------------------------------------------------





-> # Existing Tools: SOLID  <-

Introduced by Michael Feathers & Robert C. Martin

* Single Responsibility Principle
  - A class should have only a single responsibility
* Open/Closed Principle
  - Software entities should be open for extension, but closed for
    modification.
* *Liskov Substitution Principle*
  - *Objects in a program should be replaceable with instances of their
    *subtypes without altering the correctness of that program*
* Interface Segregation Principle
  - Many client-specific interfaces are better than one general-purpose
    interface
* Dependency Inversion Principle
  - Depend upon Abstractions. Do not depend upon concretions

https://en.wikipedia.org/wiki/Solid_%28object-oriented_design%29
http://cleancoders.com/category/solid-principles#videos

--------------------------------------------------------------------------------





-> # Existing Tools: SOLID  <-

Introduced by Michael Feathers & Robert C. Martin

* Single Responsibility Principle
  - A class should have only a single responsibility
* Open/Closed Principle
  - Software entities should be open for extension, but closed for
    modification.
* Liskov Substitution Principle
  - Objects in a program should be replaceable with instances of their
    subtypes without altering the correctness of that program
* *Interface Segregation Principle*
  - *Many client-specific interfaces are better than one general-purpose*
    *interface*
* Dependency Inversion Principle
  - Depend upon Abstractions. Do not depend upon concretions

https://en.wikipedia.org/wiki/Solid_%28object-oriented_design%29
http://cleancoders.com/category/solid-principles#videos

--------------------------------------------------------------------------------





-> # Existing Tools: SOLID  <-

Introduced by Michael Feathers & Robert C. Martin

* Single Responsibility Principle
  - A class should have only a single responsibility
* Open/Closed Principle
  - Software entities should be open for extension, but closed for
    modification.
* Liskov Substitution Principle
  - Objects in a program should be replaceable with instances of their
    subtypes without altering the correctness of that program
* Interface Segregation Principle
  - Many client-specific interfaces are better than one general-purpose
    interface
* *Dependency Inversion Principle*
  - *Depend upon Abstractions. Do not depend upon concretions*

https://en.wikipedia.org/wiki/Solid_%28object-oriented_design%29
http://cleancoders.com/category/solid-principles#videos

--------------------------------------------------------------------------------





-> # Existing Tools: Refactoring  <-


Martin C. Fowler

noun: a *change* made to the internal *structure of software* to make it easier
to understand and cheaper to modify *without changing its observable behavior*

verb: to restructure software by applying a series of refactorings without
changing its observable behavior

## Code Smells

* Comments
* Long Method
* Long Class
* Conditional Complexity
* Private Methods
* Shotgun Surgery
* Data Classes

http://refactoring.com/

--------------------------------------------------------------------------------





-> # How do I BDD?  <-


*1. Red*

  Write a spec; make sure it fails

## 2. Green

  Write just enough code to make the spec pass

3. Refactor

  Optimize the code to make it easier to make the next change
  Improve the clarity of the code
  Change the code, not the specs
  The specs should pass when you're done

--------------------------------------------------------------------------------





-> # How do I BDD?  <-

Thinking BDD: Learn to ask yourself questions

- What will this feature do?
- Where do I start?
- What might be a convenient interface for that?

When things get sticky, ask:

- Why is this so darn hard?
- Is this object/method handling too many responsibilities?
- How can I avoid making a decision?
- Is there a more convenient way to think about this interface?
- How could the code be clearer?

--------------------------------------------------------------------------------





-> # BDD in JavaScript  <-


Tools:

- Mocha: Test suite and runner

  http://mochajs.org/

- Chai:  Expectation library

  http://chaijs.com/

- Sinon: Stubs, Spies, and Mocks

  http://sinonjs.org/

--------------------------------------------------------------------------------













-> (David: it's time to pause and write code) <-
