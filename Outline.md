# Outline

## I. Software Engineering Crisis and Failures

*   **Definition and Classification of Failures:**
    *   **Catastrophic:** Major failures with severe consequences (e.g., Ariane 5 crash).
    *   **Chronic:** Project overruns, functionality issues, poor performance, low-quality code.
*   **Ways Software Projects Fail:**
    *   Incomplete, over-budget, buggy, late, undelivered features, unsupportable code, poor platform compatibility.
*   **Standish Chaos Report:**
    *   Findings on project success rates and reasons for failure.
    *   Project resolutions: Successful, Challenged, Incomplete.
    *   Criticisms of the Chaos Report (e.g., incomplete classification, lack of context, bias in measurement).
    *   Importance of understanding the context of success/failure.
    *   Understand the definitions of project success, challenged, and impaired used in the Chaos report. Make sure to review the criticisms of the Chaos report, including those by Robert Glass and Magne Jørgensen.
*   **Modern Software Failures:**
    *   Review examples of recent software failures (e.g., Tesla Autopilot crashes, Pfizer vaccine rollout issues, Microsoft Azure platform update failure, CNET AI article errors).
    *   Understand the reasons behind these failures and their consequences.

## II. Software Project Management and Cost Estimation

*   **The Constraint Triangle (Time, Quality, Cost):**
    *   Understand the trade-offs between these three constraints.
    *   Review the factors that affect each constraint.
*   **Brooks' Law (Mythical Man-Month):**
    *   Adding manpower to a late project makes it later.
    *   Understand the exceptions to this law.
*   **Schedule Slippage and Management:**
    *   Analyze the impact of schedule slippage.
    *   Strategies for dealing with slippage (re-staffing, re-scheduling, trimming).
    *   Importance of milestones and task granularity.
*   **Cost Estimation Techniques:**
    *   **Expert Estimation:** Planning poker, Work Breakdown Structure (WBS). Understand the benefits of planning poker in reducing anchoring.
    *   **Formal Estimation:** COCOMO (COnstructive COst MOdel). Be able to explain the significance of the EQF (Estimating Quality Factor) as proposed by DeMarco, as it applies to project management.
    *   **Combined Methods:** Using both expert and formal estimation.
*   **Productivity Metrics:**
    *   Lines of Code (LOC, KLOC).
    *   Function Points (FP) and their calculation.
    *   Object Points.
    *   Understand the strengths and weaknesses of each metric.
*   **Estimating Quality Factor (EQF) and Estimation Bias:**
    *   Calculation and significance of EQF.
    *   Definition and impact of estimation bias.
    *   Factors affecting estimation accuracy.
    *   Understand how to calculate EQF and bias. The ability to draw conclusions about project performance based on EQF and bias data will be assessed.
*   **Boem's Cone of Uncertainty:**
    - Understand how the accuracy of estimates changes over the project lifecycle.
*   **Be able to calculate EQF and bias figures from project data. (Based on past exams)**
*   **Be able to discuss the criticisms given in the "The Rise and Fall of the Chaos report figures" and explain the authors' own approach in evaluating project performance. (Based on past exams)**

## III. Object-Oriented Design and Patterns

*   **SOLID Principles:**
    *   **Single Responsibility Principle (SRP):** Each class should have one specific responsibility.
    *   **Open/Closed Principle (OCP):** Classes should be open for extension but closed for modification. Be able to describe the open/closed principle for OO development, its benefits, and illustrate how it can be implemented in code written in Java.
    *   **Liskov Substitution Principle (LSP):** Subclasses should be substitutable for their base classes without altering program correctness.
    *   **Interface Segregation Principle (ISP):** Clients should not be forced to depend on methods they don't use.
    *   **Dependency Inversion Principle (DIP):** Depend on abstractions, not concretions.
*   **Design Patterns:**
    *   **Architectural:** MVC (Model-View-Controller). Be able to describe the purpose and benefits of the MVC.
    *   **Creational:** Singleton, Factory, Abstract Factory, Builder.
    *   **Structural:** Adapter (Wrapper), Facade.
    *   **Behavioral:** Command, Chain of Responsibility, Memento.
    *   **Concurrency:** Double-checked locking. Be able to describe the purpose and benefits of the Double-checked locking and Abstract factory pattern.
    *   Be familiar with the purpose, benefits, and examples of each pattern.
*   **Code Examples:**
    *   Review the provided Java code examples for each design pattern.
    *   Understand how these patterns are implemented in practice.
*   **Be able to describe and explain the application of the following OO design patterns with the aid of examples and class diagrams:**
    *   **Singleton, Memento, Chain of responsibility, Double lock checking. (Based on past exams)**

## IV. Agile, XP, and Scrum

*   **Agile Manifesto and Principles:**
    *   Understand the values and principles behind Agile development.
    *   Be familiar with the 12 principles of Agile.
*   **Extreme Programming (XP):**
    *   User stories, pair programming, test-driven development, continuous integration.
    *   Understand the XP process and its benefits/drawbacks. Be able to explain and critique the XP pair-programming approach, in your answer refer to relevant research results.
    *   Be able to discuss XP development.
*   **Scrum:**
    *   Roles: Product Owner, Scrum Master, Developers.
    *   Artifacts: Product Backlog, Sprint Backlog, Increment.
    *   Events: Sprint Planning, Daily Scrum, Sprint Review, Sprint Retrospective.
    *   Understand the Scrum process and its benefits/drawbacks. Be able to describe the SCRUM development lifecycle.
*   **Planning Poker:**
    *   Understand how planning poker is used for estimation in Agile.
    *   Review its benefits in reducing anchoring and improving accuracy.
*   **Be able to apply techniques recommended in Agile, SCRUM, and XP to deal with software development issues. (Based on past exams)**

## V. Concurrency and the Actor Model

*   **Concurrency Concepts:**
    *   Threads, tasks, monitors, deadlock, race conditions, thread starvation.
    *   Understand the challenges of concurrent programming.
*   **Actor Model:**
    *   Actors, messages, mailboxes, fair scheduling, location transparency, mobility.
    *   Benefits of the Actor model in addressing concurrency issues.
*   **Actor Languages and Frameworks:**
    *   Erlang, Scala, Akka, Actor Foundry.
    *   Understand the features and advantages of these languages/frameworks.
*   **Safe Messaging:**
    *   Cloning, immutable objects, linear types.
*   **Synchronization and Actors:**
    *   How actors handle synchronization and avoid deadlocks.
*   **Actor model and concurrency:**
    *   Monitor, task, thread and deadlock
    *   The lost update problem
    *   Actor messaging, Actor actions, Fair scheduling, Strong and weak mobility
    *   Be able to describe the use of the Actor model and how it is can be applied to an application running over distributed system architecture.
    *   **Be able to describe how the Actor model could be used to help design and develop a high-performance platform to deal with order processing for an e-commerce web site. (Based on past exams)**

## VI. Aspect-Oriented Programming (AOP)

*   **Cross-Cutting Concerns:**
    *   Definition and examples (logging, security, transaction handling).
    *   Problems caused by cross-cutting concerns (code scattering, duplication, tangling).
*   **AOP Concepts:**
    *   Aspect, advice, join point, pointcut, weaving.
    *   Understand the purpose and usage of each concept.
*   **AOP Platforms:**
    *   AspectJ, Spring AOP, JBoss AOP.
    *   Be familiar with the features and capabilities of these platforms.
*   **AspectJ Examples:**
    *   Review the provided AspectJ code examples.
    *   Understand how to define aspects, pointcuts, and advice.
    *   **Be able to explain the following code in detail by commenting on each line  (Based on past exams)**
    *   **Be able to define an Aspect for logging all setters (not method setters) for any class in a specific package. (Based on past exams)**
    *   **Be able to describe cross-cut concerns, the problems they cause, and explain how the Aspect Orientated Programming approach can be used to help overcome this problem. (Based on past exams)**
*   **Types of Advice:**
    *   `before()`, `after() returning`, `after() throwing`, `after()`, `around()`.
*   **Pointcut Designators:**
    *   `call()`, `execution()`, `get()`, `set()`, `handler()`, `staticinitialization()`, `initialization()`, `preinitialization()`, `withincode()`, `within()`, `cflow()`, `cflowbelow()`, `if()`, `this()`, `target()`, `args()`.
*   **Exception Handling in AOP:**
    *   Using `after() throwing` and `handler()`.
    *   `declare soft` for exception softening.
*   **Inter-type Declarations:**
    *   Adding methods, fields, and constructors to external classes.
    *   Changing inheritance and adding interfaces.
*   **Compile-Time Declarations:**
    *   `declare warning`, `declare error`, `declare precedence`.

## VII. Program Slicing and Dependency Graphs

*   **Dependency Graphs:**
    *   Control dependence, data dependence, control/data dependence.
    *   Understand how to construct a dependency graph from code.
*   **Program Slicing:**
    *   Forward slicing, backward slicing.
    *   Static slicing, dynamic slicing, conditional slicing.
    *   Inter-modular slicing.
    *   Understand the purpose and applications of program slicing.
*   **Be able to construct forward slices and backward slices for a given code segment. (Based on past exams)**
*   **Be able to draw a dependency graph for a given code segment. (Based on past exams)**
*   **Be able to explain how the dependency graph and program slicing can be used to help when debugging the software and maintaining the software. (Based on past exams)**
*   **Slicing Tools:**
    *   JSlice (Java slicing tool).
    *   Understand how these tools work and their capabilities.

## VIII. Software Re-factoring

*   **Reasons for Re-factoring:**
    *   Improve code quality, maintainability, readability, and flexibility.
*   **Re-factoring Techniques:**
    *   Extract method, encapsulate field, rename, move, etc.
    *   Understand the purpose and application of each technique.
*   **Automated Re-factoring Tools:**
    *   Eclipse, IntelliJ IDEA, etc.
    *   Be familiar with the capabilities of these tools.

## IX. Additional Topics

*   **Javascript and OO:**
    *   Understand the challenges and limitations of using OO concepts in Javascript.
    *   Review techniques for emulating classes, inheritance, and privacy in Javascript.
    *   Be familiar with Javascript libraries like jQuery, PIXI JS, AngularJS, and SoundJS.
*   **Mobile Development:**
    *   Fragmentation and challenges of mobile development.
    *   Frameworks like Phonegap/Cordova, React Native, and Flutter.
*   **Concurrency and Parallelism:**
    *   Challenges of developing concurrent systems.
    *   Approaches for improving performance through parallelism.
*   **Testing:**
    *   Unit testing, integration testing, system testing, acceptance testing.
    *   Test-driven development (TDD).
    *   Importance of testing in Agile and XP.
*   **Code Reviews:**
    *   Benefits of code reviews in improving code quality and knowledge sharing.
*   **Documentation:**
    *   Importance of documentation in software development.
    *   Types of documentation (UML diagrams, user guides, system guides, etc.).

## X. Exam Question Types

*   Calculate EQF and bias.
*   Draw dependency graphs.
*   Construct program slices.
*   Explain and critique software development methodologies (Agile, XP, Scrum).
*   Describe and apply design patterns.
*   Discuss the Actor model and concurrency.
*   Analyze code snippets and comment on AOP concepts.
*   Apply techniques from Agile, SCRUM, and XP to solve software development problems.
*   Provide a Java solution to a problem using the Factory object pattern and the Façade structure.