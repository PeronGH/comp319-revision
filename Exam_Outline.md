# 24/25 Exam Revision Outline

## I. Object-Oriented (OO) Design Patterns and Principles

*   **A. OO Design Patterns**
    1. **Model-View-Controller (MVC)**
    
        *   **Components:** Model (data & business logic), View (UI), Controller (glue)
        *   **Benefits:**
            *   Clear seperation of concerns
            *   Easier to port software UI platform to UI platform
    
        *   **Coupling between components:**
            *   View - Controller: Tight; controller processes input and instructs view to render
            *   Controller - Model: Moderate; controller passes events to model
            *   Model - View: Loose; view may fetch data from model
    
    2. **Singleton**
    
        *   **Definition:** ensuring only one instance of a class
    
        *   **Purpose:** resource management, global state, single point of control
    
        *   **Implementation:** private constructor, static instance
    
        *   **Instantiation:**
    
            *   Lazy: created when first requested
            *   Eager: created at the time the class is loaded or initialized
    
        *   **Double-checked locking:**
    
            *   If lazily instantiated by multiple threads, multiple singleton may be created if there is only one check
    
            *   ```java
                public class Singleton {
                    private static volatile Singleton instance;  // Note the 'volatile' keyword
                
                    private Singleton() {}
                
                    public static Singleton getInstance() {
                        if (instance == null) { // First check (without locking)
                            synchronized (Singleton.class) {
                                if (instance == null) { // Second check (within synchronized block)
                                    instance = new Singleton();
                                }
                            }
                        }
                        return instance;
                    }
                }
                ```
    
    3. **Abstract Factory**
    
        *   **Definition:**
            *   `AbstractFactory` creates `AbstractProduct`
            *   `ConcreteFactory` implementing `AbstractFactory` creates `ConcreteProduct` implementing `AbstractProduct`
        *   **Purpose:** create families of related objects
        *   **Factory method:** a static method creating different `ConcreteProduct` implementing `AbstractProduct` based on input.
        *   **Use cases:** different encryption algorithms, UI components for different OS
    
    4. **Builder**
    
        *   **Definition:** the builder allows you to construct the object piece by piece. The final object can be constructed once necessary information is provided.
        *   **Purpose:** separate object construction from its representation
        *   **Use cases:** SQL statement builder, HTTP request builder
    
    5. **Wrapper/Adapter**
    
        *   **Definition:** adapt interfaces, providing a standard interface to different implementations
        *   **Benefits:** 
            *   Easier to swap modules
            *   Easier to implement standard functions
        *   **Use cases:** database connectors, SMS providers
    
    6. **Façade**
    
        *   **Definition:** provide simplified interface to a complex subsystem & hide internal details
        *   Package access control to enforce the use of the facade
    
    7. **Memento**
    
        *   **Definition:** snapshot capturing and restoring object state
        *   **Components:** Originator (holding state), Memento (the snapshot), Caretaker (holding Memento objects)
        *   **Use cases:** undo/redo, version control
        *   **Implementation:** defined as inner class of Originator to share data with Originator privately
    
    8. **Command**
    
        *   **Definition:** encapsulate requests as objects
        *   **Benefits:**
            *   All arguments can be validated once for each command
            *   Can return standardized results or status codes
            *   Security logic can be implemented at the command level to unify authentication
            *   The command interface is adaptable
            *   Can implement role-based access control
    
    9. **Chain of Responsibility**
        *   **Definition:** pass requests along a chain of handlers
        *   **Example:** System logging
    
    10. **Flyweight**
    
        *   **Definition:** share memory for similar objects
        *   Related to Multiton
        *   **Example:** Font definitions in a word processor
    
    11. **Multiton**
    
         *   **Definition:** multiple managed instances, keyed access
         *   **Example:** Customer Relationship Manager (CRM) instances
    
*   **B. OO Principles (SOLID)**
    
    1. **Single Responsibility Principle**
        *   Each class should have one specific responsibility.
        *   Improves code maintainability, reusability, testability, and coherence.
        *   Avoids "God" classes that do too much.
    2. **Open/Closed Principle**
        *   Classes should be open for extension but closed for modification.
        *   Use interfaces, abstract classes, `final`, and `protected` keywords.
        *   Avoids modifying existing code, which can introduce bugs.
        *   Template pattern as an example.
    3. **Liskov Substitution Principle**
        *   Subtypes must be substitutable for their base types.
        *   Avoids unexpected behavior when using inheritance.
        *   Ensures that subclasses adhere to the contract of the base class.
    4. **Interface Segregation Principle**
        *   Clients should not be forced to depend on interfaces they don't use.
        *   Break down large interfaces into smaller, more specific ones.
        *   Avoids "fat" interfaces.
    5. **Dependency Inversion Principle**
        *   High-level modules should not depend on low-level modules; both should depend on abstractions.
        *   Abstractions should not depend on details; details should depend on abstractions.
        *   Improves code decoupling and flexibility.

## II. Project Management and Cost Estimation

*   **A. Software Engineering Crisis**
    *   Historical context (Standish Chaos Report)
    *   Types of failures (catastrophic, chronic)
    *   Reasons for project failure (incomplete requirements, poor planning, etc.)
    *   Criticisms of the Chaos Report (e.g., "The Rise and Fall of the Chaos Report Figures")
*   **B. Project Management Constraints**
    *   The "Pick Two" triangle (Time, Quality, Cost)
    *   Trade-offs between constraints
    *   Brooks' Law ("Adding manpower to a late software project makes it later.")
*   **C. Cost Estimation**
    1. **Techniques**
        *   Expert estimation (e.g., planning poker, Wideband Delphi)
        *   Formal estimation (e.g., COCOMO)
        *   Combined methods
    2. **Metrics**
        *   Lines of Code (LOC)
        *   Function Points
        *   Object Points
    3. **Factors affecting productivity**
        *   Application domain experience, process quality, project size, technology support, working environment
    4. **Estimation Quality Factor (EQF)**
        *   Definition and calculation
            *   $\text{EQF} = \frac{1}{\text{Average}(\frac{\text{Deviation}}{\text{Actual}})}$
        *   Interpretation (higher is better)
    5. **Estimation Bias**
        *   Definition and calculation
            *   $\text{Bias} = \text{Mean}(\text{Estimator}) – \text{ActualValue}$
            *   $\text{BiasPercentage} = \frac{\text{Mean}(\text{Estimator}) – \text{ActualValue}}{\text{ActualValue}}$
        *   Interpretation (positive vs. negative bias)
    6. **Factors affecting estimation accuracy**
        *   Early estimations are harder
        *   Management pressure
        *   Inexperienced developers
        *   Lack of design
        *   Quality of the specification
    7. **Boem's Cone of Uncertainty**

## III. Agile, XP, and Scrum

*   **A. Agile Principles**
    *   Agile Manifesto
    *   12 principles of Agile development
*   **B. Extreme Programming (XP)**
    *   User stories (INVEST – Independent, Negotiable, Valuable, Estimable, Small, Testable)
    *   Pair programming
        *   Benefits (reduced defects, knowledge sharing)
        *   Drawbacks (cost, personality conflicts)
        *   Research findings (e.g., Williams, Lui)
    *   Test-driven development (TDD)
    *   Continuous integration
    *   Refactoring
    *   On-site customer
    *   Planning game
    *   Small releases
    *   Collective code ownership
*   **C. Scrum**
    1. **Roles**
        *   Product Owner
        *   Scrum Master
        *   Development Team
    2. **Events**
        *   Sprint Planning
        *   Daily Scrum
        *   Sprint Review
        *   Sprint Retrospective
    3. **Artifacts**
        *   Product Backlog
        *   Sprint Backlog
        *   Increment (working software)
    4. **Concepts**
        *   Sprints (iterations)
        *   Timeboxing
        *   Burndown charts
        *   Velocity
    5. **Scrum Values**
        *   Commitment, Focus, Openness, Respect, Courage

## IV. Unimportant Topics

*   **A. Program Slicing**
    *   Forward and backward slicing
    *   Static and dynamic slicing
    *   Dependency graphs
    *   Use cases: debugging, program understanding, maintenance
    *   Tools: JSlice
*   **B. Actor Model**
    *   Concurrency model
    *   Actors: independent units of computation
    *   Messaging: asynchronous, no shared memory
    *   Mailboxes
    *   Fair scheduling
    *   Location transparency
    *   Mobility (strong vs. weak)
    *   Examples: Erlang, Akka, Actor Foundry
*   **C. Javascript**
    *   OO features in Javascript
        *   Prototypes, inheritance, dynamic typing
    *   Benefits and limitations compared to Java
    *   Privacy: private is not available in Javascript, but there are workarounds to emulate it (closures, naming convention, obfuscation)
    *   Concurrency in Javascript (single-threaded, non-blocking I/O, async/await)
    *   Use of Javascript for building web applications
    *   HTML5, DOM, AJAX, JSON
    *   Javascript libraries (Jquery, PIXI JS, AngularJS, SoundJS)
    *   Mobile development with Javascript (Phonegap, React Native, Flutter)
    *   Node.js for server-side development
*   **D. Typescript**
    *   Superset of Javascript
    *   Strong static typing
    *   Compiled into Javascript
*   **E. Design by Contract**
    *   Use assertions to define pre-conditions, post-conditions, and invariants
    *   Helps to ensure code correctness and improve documentation
*   **F. Re-factoring**
    *   Definition and purpose
    *   Common re-factoring techniques (e.g., Extract Method, Rename, Encapsulate Field)
    *   Tools support for re-factoring (e.g., in Eclipse)
