# Outline

## 1. Software Engineering Crisis and Failures

*   **Understanding the Crisis:**
    *   Definition of the software crisis: project overruns (time and budget), failure to meet requirements, poor quality, and maintenance nightmares.
    *   Difference between catastrophic failures (e.g., Ariane 5 explosion) and chronic failures (e.g. ongoing project overruns).
    *   The Standish Chaos Report: Key findings (e.g., high percentage of project failures or challenges) and its criticisms (e.g., incomplete classification of project outcomes, lack of context, measurement issues).
    *   The ongoing nature of the software crisis, with examples of recent major software failures.
    *   The limitations of AI tools in software development, using examples of AI-generated errors.
*   **Revision Focus:**
    *   Be able to discuss the nature of the software crisis using examples.
    *   Critically analyze the Standish Chaos Report, considering its findings and limitations.
    *   Understand the various ways in which software projects can fail.

## 2. Software Project Management and Cost Estimation

*   **The Constraint Triangle:**
    *   Understanding the trade-offs between Time, Quality, and Cost.
    *   Why increasing resources doesn't always improve time or quality.
*   **Brooks' Law:**
    *   "Adding manpower to a late software project makes it later."
    *   Exceptions and limitations to Brooks' Law.
*   **Cost Estimation Techniques:**
    *   Expert estimation (e.g., Planning Poker, Work Breakdown Structure (WBS)).
    *   Formal estimation (e.g., COCOMO).
    *   Combined methods.
*   **Metrics:**
    *   Lines of Code (LOC).
    *   Function Points.
    *   Object Points.
*   **EQF (Estimating Quality Factor) and Estimation Bias:**
    *   Calculating and interpreting EQF.
    *   Calculating and interpreting Estimation Bias.
    *   How these metrics can be used to evaluate estimation accuracy.
*   **Boem's Cone of Uncertainty:**
    *   Understand how the accuracy of estimates changes over the project lifecycle.
*   **Revision Focus:**
    *   Understand the trade-offs between time, cost, and quality.
    *   Be able to discuss and apply different cost estimation techniques.
    *   Calculate and interpret EQF and Estimation Bias.
    *   Explain Boem's Cone of Uncertainty and its implications.
    *   Analyze the factors that affect estimation accuracy.
    *   Know the good practices to deal with schedule slippage and project overruns.

## 3. Object-Oriented Design Patterns

*   **SOLID Principles:**
    *   Single Responsibility Principle.
    *   Open/Closed Principle.
    *   Liskov Substitution Principle.
    *   Interface Segregation Principle.
    *   Dependency Inversion Principle.
*   **Design Patterns:**
    *   Model-View-Controller (MVC) (architectural pattern)
    *   Singleton (creational pattern)
    *   Factory (creational pattern)
    *   Abstract Factory (creational pattern)
    *   Builder (creational pattern)
    *   Adapter (structural pattern)
    *   Façade (structural pattern)
    *   Memento (behavioral pattern)
    *   Chain of Responsibility (behavioral pattern)
    *   Command (behavioral pattern)
    *   Flyweight (structural pattern)
    *   Multiton (creational pattern)
    *   Double-checked locking (concurrency pattern)
*   **Revision Focus:**
    *   Understand and apply the SOLID principles in code examples.
    *   Recognize and explain the purpose of each design pattern.
    *   Be able to illustrate how each pattern is implemented in Java.
    *   Understand the benefits of using each pattern.
    *   Know the drawbacks of each pattern.
    *   Understand the issues with applying OOP in Javascript, and how they can be addressed.
    *   Know the types of advice and how they are applied.
    *   Know the difference between compile-time and run-time weaving.
    *   Know the different types of program slicing and their purposes.

## 4. Agile, XP, and Scrum

*   **Agile Principles:**
    *   Understand the Agile Manifesto and its core values.
    *   12 principles of Agile.
*   **Extreme Programming (XP):**
    *   User stories (characteristics: Independent, Negotiable, Valuable, Estimable, Small, Testable).
    *   Pair programming.
    *   Test-driven development.
    *   Continuous integration.
    *   Planning and feedback loops.
    *   XP process and stages.
    *   The concept of collective code ownership.
    *   Criticisms of XP (e.g., feature creep, lack of upfront design, constant refactoring).
*   **Scrum:**
    *   Roles: Product Owner, Scrum Master, Developers.
    *   Events: Sprint Planning, Daily Scrum, Sprint Review, Sprint Retrospective.
    *   Artifacts: Product Backlog, Sprint Backlog, Increment.
    *   Sprint: Time-boxed iterations, typically 1-4 weeks.
    *   Burn-down charts.
*   **Planning Poker:**
    *   Purpose: collaborative estimation technique.
    *   Process: how it works and why it's effective.
    *   Benefits: reduces anchoring, improves estimation accuracy.
*   **Revision Focus:**
    *   Understand the core principles of Agile.
    *   Explain the key practices of XP and their benefits/drawbacks.
    *   Describe the Scrum framework, including roles, events, and artifacts.
    *   Explain how Planning Poker works and its advantages.
    *   Discuss the criticisms of Agile and XP.
    *   Understand the research findings related to pair programming.

## 5. Concurrency and the Actor Model

*   **Concurrency Challenges:**
    *   Deadlocks: causes and prevention.
    *   Race conditions.
    *   Thread starvation.
    *   Shared memory issues (e.g., lost update problem).
    *   Fairness in thread scheduling.
*   **Traditional Concurrency Mechanisms:**
    *   Threads.
    *   Monitors (mutexes).
    *   Synchronization.
*   **Actor Model:**
    *   Actors: independent entities with their own state and behavior.
    *   Message passing: asynchronous communication.
    *   Mailboxes.
    *   Benefits: avoids shared memory problems, simplifies concurrency.
    *   Fair scheduling.
    *   Location transparency.
    *   Mobility (strong and weak).
    *   Synchronization constraints.
*   **Actor Languages and Frameworks:**
    *   Erlang.
    *   Scala.
    *   Actor Foundry.
*   **Revision Focus:**
    *   Understand the challenges of concurrent programming.
    *   Explain how the Actor model addresses these challenges.
    *   Describe the key features of the Actor model.
    *   Be familiar with Actor languages and frameworks.
    *   Understand the different approaches to message handling in Actor systems.
    *   Discuss the concepts of location transparency and mobility in the context of Actors.
    *   Know the dining philosophers' problem and its solutions.
    *   Understand how to use futures to improve performance.

## 6. Dependency Graphs and Program Slicing

*   **Dependency Graphs:**
    *   Control dependence.
    *   Data dependence.
    *   Control/data dependence.
    *   Program dependency graphs (PDG).
*   **Program Slicing:**
    *   Backward slicing.
    *   Forward slicing.
    *   Static slicing.
    *   Dynamic slicing.
    *   Applications of slicing (e.g., debugging, program understanding, maintenance).
*   **Revision Focus:**
    *   Understand the concepts of control and data dependence.
    *   Be able to construct a simple PDG.
    *   Explain how program slicing works and its various applications.
    *   Differentiate between different types of slicing.
    *   Understand the benefits and limitations of slicing.
    *   Know the basic idea of the HPR algorithm for merging.

## 7. Other Important Concepts

*   **Requirements Analysis:**
    *   Importance of clear, unambiguous, and testable requirements.
    *   Techniques for eliciting and documenting requirements.
*   **Software Design:**
    *   SOLID principles.
    *   Design patterns.
    *   Coupling and cohesion.
*   **Software Testing:**
    *   Unit testing.
    *   Integration testing.
    *   System testing.
    *   Acceptance testing.
    *   Test-driven development.
    *   Regression testing.
*   **Software Maintenance:**
    *   Types of maintenance (e.g., corrective, adaptive, perfective, preventive).
    *   Refactoring.
*   **Software Evolution:**
    *   Adapting software to changing requirements and environments.
