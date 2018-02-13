(Title TBD)

# Abstract

- Static and dynamic type systems have their strengths and weaknesses.
- There are attempts to find a place between static and dynamic type systems in both research and industry.
- Gradual type system is one of these solutions widely used. And in this survey we will look at
  works that extends existing programming language to support gradual typing.

# Introduction

- the strengths and weaknesses of both:

    - dynamic languages:

        - suitable for scripting (bash, perl, awk, etc.), web techiniques (JavaScript)
          for fast prototyping (but programmer would still have some concepts of types in mind but without
          having an actual type system, which might otherwise get in the way)

        - present everywhere: some scripting languages are standard feature of UNIX, and every modern browser
          is equipped with JavaScript engines.

        - hard to maintain overtime: as the interaction between functions and values tends to grow out of control
          for programmers

        - slow due to its highly dynamic nature

    - static languages:

        - less maintanenance effort, as type system keeps an eye.

        - less accessible: end-user sees compiled code, won't normally have compiler, build system and toolchain available.

        - could have better performance due to

          - have little or no runtime check and dispatching
          - having more type info around exposes more oppotunities for optimization

- attempts of combining both:

    - Goals:

        - a type system that programmers can opt-in (for Dynamic -> Static road)
        - or capable of enforcing more constraints (for Static -> _ road)
        - allow static language to interact with dynamic ones (e.g. CSharp)
        - (what else?)

    - Gradual Typing: introduction

        - Gradually Typed Lambda Calculus
        - blame
        - gradual guarantee

    - Alternatives:

        - Soft Typing / Contracts
        - Liquid type / refinement type / dependent type

    - discussion:

        - Why Gradual typing

# Gradual typing in existing programming languages

Extending existing programming language requires designers to understand:

- language features
- programming idiom

(enumerate through ~~languages~~ research works investigated):

(Q: languages or research works?)

- show examples in extended language, perferably showcase interaction
  between language-specific features and gradual typing

- Safe TypeScript

    (probably showcasing)
    - Object as map
    - Object in the sense of OOP

    - "occurrence typing" (see "Type Guards and Differentiating Types" of advanced types)
      (note: this one is probably not related to Safe TypeScript)
    - Array as tuple (also not in Safe TypeScript)

- Typed Scheme

    - occurrence typing
    - simple macros

- Reticulated Python

    - structural typing to match for Python's duck typing

- CSharp (this being the only static language that wants interaction with dynamic ones)

    - syntactic improvement
    - dynamic Object ("Expando Object")

- Gradualtalk (TODO)

# Challenges and Solutions

(Need to be re-organized)

- type system extension:

    - introducing a dynamic type (changes to type judgment)

        - subtyping (consistency & transitivity)

    - Or: improve type system precision

        - using predicates
        - constraints as type level computation (requires a type system of sufficient expressiveness)

    - typing structural data

        - nominal
        - structural

- Object-oriented programming

    - object identity
    - giving `this` / `self` special type treatment
    - inheritance (could merge with subtyping)

- variable / member mutation

- implementation & performance

    - cast insertion
    - Large array
    - runtime check overhead

- language-specific challenges

# Related Work

- (TODO) sound gradual typing is nominally alive and well

# Future

# Summary
