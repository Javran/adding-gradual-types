# Abstract

- combine static and dynamic typing within the same language
- prototypes or scripts into mature robust programs

- Features in Smalltalk:

    - metaclasses
    - blocks
    - live programming

- Need to accomodate the programming idioms (detail?)

# Introduction

- Popularity of dynamic languages

- Consolidate grown prototypes

- Gradual typing

    - a system allowing developers to define which sections of code are statically typed
      and which are dynamically typed.

    - ensure dynamic code does not violate the assumptions made in statically-typed code

- Smalltalk: emblematic dynamic object-oriented language

    - highly-dynamic nature of the language

    - live programming environment

- programmers rely on various programming idioms -> challenging to type

- Strongtalk: an optional type system, does not influence the runtime semantics of the language

- Key to these guarantees: the insertion of runtime casts a the static/dynamic boundaries

- Gradualtalk: fully compatible with existing code

    - a type system with features:

        - nominal and structural types, union types, self types

        - parametric polymorphism

        - blame tracking

# Gradual Typing for Smalltalk

Examples

- Dyn, Symbol, inherent dynamicity:

    - return type cannot be determined statically
    - using Dyn instead of Object to allow returning any type

- closures as function (arrow) type

- Self type in order not to lose any type info (idiom of chainning invocations?)

    - "Self" is the type of "self"

    - "Self instance" is the type of objects instantiated by "self",
      "Self instance" is therefore only applicable when "self" is a class or metaclass

    - "Self class" ?

- Casts

    - implicit cast by type system
    - explicit cast (coercion) by programmers
    - error can be raised at runtime

- Blame tracking

    - higher-order cast cannot be verified immediately
    - remember info sufficient to assign blame correctly

# Refining the Type System

- already Gradualtalk but with Dyn types

- aim: minimize Dyn, to do so a bunch of features are introduced

- Supporting programmer idioms:

    - backward compatibility

    - seamless intergation

- Parametric polymorphism

    - Problem: otherwise Array element loses type info

- Union Types: different branch might return different types

    - drawback: need explicit coersion to call specific methods?

- Structural types: set of method types

    - introduce type alias, not restricted to structural types

- Nominal Types: types induced by classes

    - Discussion: structural types vs. nominal types

    - Solution: combination

    - Flexible Protocols

- Safety and type soundness

- Summary

    - type grammar

# Type System Semantics

- Self types (TODO)

- (TODO) Need some knowledge of Smalltalk to continue from this point.

# Practical Experience

# Related Work

# Conclusion
