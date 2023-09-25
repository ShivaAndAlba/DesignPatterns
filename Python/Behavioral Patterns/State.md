# State Pattern

## TLDR
Used to describe a finite state machine in your code, when an object can change its behavior depending on internal state.

## When to use
1. Object's behavior dpends on internal state and needs to change behavior in real time.
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
