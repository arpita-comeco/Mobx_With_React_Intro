## Introduction to MobX
MobX is an open source state management tool. When creating a web application, developers often seek an effective way of managing state within their applications. One solution is to use a unidirectional data flow pattern named Flux, introduced by the React team, and later implemented in a package called React-Redux, which made the use of the Flux pattern even easier.

MobX, a simple, scalable, and standalone state management library, follows functional reactive programming (FRP) implementation and prevents inconsistent state by ensuring that all derivations are performed automatically. According to the MobX getting started page, “MobX makes state management simple again by addressing the root issue: it makes it impossible to produce an inconsistent state.”

MobX is standalone and does not depend on any frontend library or framework to work. There are implementations of the MobX in popular front-end frameworks like React, Vue, and Angular.

## MobX

In addition to being a library, MobX also introduces a few concepts: state, actions, and derivations (including reactions and computed values).

Application state refers to the entire model of an application, and can contain different data types including array, numbers, and objects. In MobX, actions are methods that manipulate and update the state. These methods can be bound to a JavaScript event handler to ensure a UI event triggers them.

Anything (not just a value) that is derived from the application state without further interaction is referred to as a derivation. Derivations will listen to any particular state and then perform some computation to produce a distinct value from that state. A derivation can return any data type, including objects. In MobX, the two types of derivations are reactions and computed values.

Sometimes, when a state changes, there may be automatic side effects needed to update the state. MobX refers to this as a reaction, and differentiates reactions from event handlers in the DOM. Reactions can make a remote network request, call the local storage, or even append a new DOM element on the fly.

Unlike reactions, which do not necessarily return a value, computed value derivations always return a value derived from the current state.


# Demonstration

Creating a PetOwnerStore class as an intro so as to understand the intricates of Mobx functionality.


