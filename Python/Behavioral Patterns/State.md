# State Pattern

## TLDR
Used to describe a finite state machine in your code, when an object can change its behavior depending on internal state.

## When to use
1. Object's behavior depends on internal state and needs to change behavior in real time.
1. When your code has many cases\if..else\enumerated statements.

## Description
### UML 
![State UML](./images/State_UML.jpeg)
1. Context
    - defines interface of intrests to clients.
    - maintains an instance of concreteState(State1, State2) subclass that defines the current state.
1. State
    - defines interface for encapsulating the behavior associated with a particular state of the Context.
1. concreteState Subclass
    - each subclass implements a behavior associated with the state of the Context.

### Notes
- Transition implemitation
    - In Short: state pattern models state specifiec behavior, table approach focuses on defining state transition.
        - concreteState subclass defines the transition behavior, this forces an interface in Context to let State objects to change Context's current state.
            - Pros:
                - makes it easy to modify\extend concreteState.
            - Cons:
                - State subclasses have knowladge of atleast one other State subclass, this intreduces implemitation dependencies between subclasses.
        - If the transition rules are simple\fixed then Context can implement it.
        - Another way to define transition is using table mapping to define every state transtition to succeeding state.
            - Pros:
                - changing the transtion between state requires only changing values in a table and code.
            - Cons:
                - less efficient.
                - harder to understand.
                - difficult to add actions to state transition.
- 
