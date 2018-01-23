# Gradual Typing for Functional Languages

- Introduction to gradual typed lambda calculus
- consistency


# Design and Evaluation of Gradual Typing for Python

## Static typing vs. Dynamic typing

Static typing:

- excels at documention, enforcing constrain
- IDE (auto completion for example)
- help compiler to generate more efficient code

Dynamic typing:

- rapid prototyping
- use of metaprogramming and reflection (are these dynamic-specific techs?)

## Summary

- Impl: source-to-source translator

- Semantics of casts: different choices

    - proxy-based (guarded)
    - ubiquitous lightweight checks (transient)
    - monotonically more precise (monotonic)

- Same Syntax (as PEP3107)

- PEP3107: just defines the syntax, interpreting it left unspecified. types are just expressions

- no type for local variables: use inference

- load time typechecking

- inserts runtime checks

- Dyn

- 3 approaches (dynamic semantics)

    - proxy: guarded

      - cast insertion
      - proxy for reading & writing
      - no obj identity, can be problematic

    - lightweight checks: transient

      - insert checks at use sites
      - no blame tracking

    - more precise: monotonic

      - locking type to a more precise one
      - require locking down object to static info

# The Design and Implementation of Typed Scheme: From Scripts to Programs

- occurrence typing: assign distinct occurrences of a variable based on control flow criteria

# Gavin Bierman, Adding dynamic types to CSharp
# E. Allende, Gradual Typing for smalltalk
