%title: Is this thing on? Testing JavaScript, 1, 2, 3.
%author: David Beveridge <davidjbeveridge@gmail.com>
%date: 2015-05-27






-> # An incomplete guide to TDD in JavaScript <-

-> David Beveridge <-

-> Originate, Inc. <-
-> www.originate.com <-



--------------------------------------------------------------------------------





-> # What will we cover? <-

* What is (and isn't) (T/B)DD?

* How do I TDD?

* BDD in JavaScript

* Example

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

* Jerks and Dogma ruin everything

--------------------------------------------------------------------------------





-> # The Bad Parts <-

* Jerks and Dogma ruin everything
* Learning Curve

--------------------------------------------------------------------------------





-> # The Bad Parts <-

* Jerks and Dogma ruin everything
* Learning Curve
  - Tools
  - Thinking BDD
  - Refactoring
  - Design
  - Brittle vs. flexible specs

--------------------------------------------------------------------------------





-> # The Good Parts <-

--------------------------------------------------------------------------------





-> # A tangent about software quality... <-

