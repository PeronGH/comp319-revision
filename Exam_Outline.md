# 24/25 Exam Revision Outline

## I. Object-Oriented (OO) Design Patterns and Principles

*   **A. OO Design Patterns**
    1. **Model-View-Controller (MVC)**
    
        *   **Components:** Model (data & business logic), View (UI), Controller (glue)
        *   **Benefits:**
            *   Clear seperation of concerns
            *   Easier to port software (e.g., one UI platform to another)
            *   Loose coupling between view and model
            *   Teamwork, one for VC (view & controller) code, another for model
    
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
    
         *   **Definition:** singleton managing multiple instances, keyed access
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
        *   Could be implemented using **template method**.
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
    - **Types of Failures:**
      - **Catastrophic:** Major failures with severe consequences (e.g., Ariane 5 crash).
      - **Chronic:** Project overruns, functionality issues, poor performance, low-quality code.
    - **Reasons:** Incomplete, over-budget, buggy, late, undelivered features, unsupportable code, poor platform compatibility.
    - **Standish Chaos Report:**
      - **Project resolutions:** Successful, Challenged, Incomplete.
      - **Criticisms:** incomplete classification, lack of context, bias in measurement.
    
*   **B. Project Management Constraints**
    *   The "Pick Two" **triangle:** Time, Quality, Cost
    *   **Brooks' Law:** "Adding manpower to a late software project makes it later."
    
*   **C. Cost Estimation**
    1. **Techniques**
        *   **Expert estimation** (e.g., planning poker, Wideband Delphi)
        *   **Formal estimation** (e.g., COCOMO)
        *   **Combined methods**
    
    2. **Metrics**
        *   Lines of Code (LOC)
        *   Function Points
        *   Object Points
    
    3. **Factors affecting productivity**
        *   Application domain experience, process (e.g., agile, waterfall) quality, project size, technology support (e.g., IDE), working environment
    
    4. **Estimation Quality Factor (EQF)**
    
        - Determine the quality of estimation.
    
        *   $\text{EQF} = \frac{1}{\text{Average}(\frac{\text{Deviation}}{\text{Actual}})}$ where $\text{Deviation} = \text{Actual} - \text{Estimator}$
    
        *   Interpretation
            *   higher is better
            *   $\text{EQF} > 10$ is considered very good.
    
    5. **Estimation Bias**
    
        *   $\text{Bias} = \text{Mean}(\text{Estimator}) – \text{ActualValue}$
            *   $\text{BiasPercentage} = \frac{\text{Bias}}{\text{ActualValue}}$
    
        *   Interpretation
            *   $= 0$: unbiased
            *   $> 0$: overestimate
            *   $< 0$: underestimate
    
    6. **Factors affecting estimation accuracy**
    
        *   Early estimations are harder
            *   Boem's Cone of Uncertainty
        *   Management pressure
        *   Inexperienced developers
        *   Lack of design
        *   Quality of the specification

## III. Agile, XP, and Scrum

*   **A. Agile Principles**
    
    *   **Core values:**
    
        1. **Individuals and interactions** over processes and tools
    
        2. **Working software** over comprehensive documentation
    
        3. **Customer collaboration** over contract negotiation
    
        4. **Responding to change** over following a plan
    *   **Principles:**
    
        1. Customer satisfaction through early and continuous delivery
        2. Welcome changing requirements, even late in development
        3. Deliver working software frequently
        4. Business people and developers work together daily
        5. Build projects around motivated individuals
        6. Face-to-face conversation is the best form of communication
        7. Working software is the primary measure of progress
        8. Promote sustainable development pace
        9. Continuous attention to technical excellence
        10. Simplicity is essential
        11. Self-organizing teams produce the best results
        12. Regular reflection and adjustment of team behavior
    
*   **B. Extreme Programming (XP)**
    
    *   **User stories**
    
        *   are short, simple descriptions of a feature told from the perspective of the user.
    
        *   are **INVEST**:
    
            1. Independent
    
               - Story should be self-contained
    
               - Minimal dependencies on other stories
    
            2. Negotiable
    
               - Details can be discussed and modified
    
               - Room for collaboration
    
            3. Valuable
    
               - Delivers value to stakeholders
    
               - Clear benefit to users
    
            4. Estimable
    
               - Team can estimate the effort required
    
               - Scope is clear enough to plan
    
            5. Small
    
               - Can be completed in one sprint
    
               - Not too big or complex
    
            6. Testable
    
               - Clear acceptance criteria
    
               - Can be verified
        *   are estimated using **story points**:
        *   Relative, based on team's perspective, not tied to time units
        *   are **criticised** for:
            *   Capturing only functional requirements
            *   Too vague for contractual basis
            *   Suitable only for experienced developers
            *   Size estimation ignores non-functional requirements
    *   **XP Process**
        *   User stories written jointly by customer and developers
        *   Stories estimated by developers
        *   Stories ordered by priority
            *   High-priority code developed and **tested** before any low-priority code
                *   Unit tests (by developer) & Acceptance tests (by user)
        *   Project plan determines when features will be delivered
        *   Regular iteration schedule established
    *   **Pair programming**
        *   Two programmers: driver and observer, collective code ownership
        *   **Benefits:** reduced defects, knowledge sharing
        *   **Drawbacks:** cost, personality conflicts (non-matching skills), not replacement for code review
    
*   **C. Scrum**
    1. **Key Roles:**
    
        - Product Owner
          - Liaises with all stakeholders
    
        - Developers
          - Development team members
    
        - SCRUM Master
    
          - Enables day-to-day SCRUM practice
    
          - Not a people manager or project manager
    
          - Supports self-organizing team
    
          - Manages daily scrum and removes obstacles
    
          - Provides communication between team and management
    
          - Controls what goes into sprints
    
          - Builds release plan
    
    2. **Key Components:**
    
       - **Product Backlog**
    
         - Maintained throughout project
    
         - Shows outstanding work
    
         - Description of all features
    
         - Features are prioritized
    
         - Items are time/cost estimated
    
       - **Sprint Planning**
    
         - Customer prioritizes work from backlog
    
         - Reviews current backlog
    
         - May add/drop features
    
         - Decides what goes into sprint backlog
    
       - **Sprint Backlog**
    
         - All tasks for current sprint
    
         - Tasks typically 4-16 hours
    
         - Developers sign up for tasks (not assigned)
    
       - **Sprint**
    
         - Iteration of 1-4 weeks
    
         - Produces deliverable user-testable version
    
         - Time boxed
    
         - Only completed/tested functions included
    
         - Progress tracked via sprint burndown
    
       - **Daily SCRUM** (Daily Stand-up)
         - 15-minute meeting at start of day
         - Covers:
           - Progress since yesterday
           - Planning for today
           - Obstacles preventing completion
    
*   **D. Planning Poker**

    *   **Process:**
        1. Each member of the planning team is given a pack of cards with numbers on them
        2. Project manager introduces project
           - Team clarifies assumptions
           - Discuss risk
        3. Each member picks a card as their estimate
        4. Lowest and highest estimation members given chance to justify their decision
        5. Discuss, then go back to step 3, until consensus is reached
    *   Prevents bias from early estimates
