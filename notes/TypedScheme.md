# The Design and Implementation of Typed Scheme

- scripts in untype languages grows and becomes difficult to maintain
- novel: occurrence typing
- making it possible to express refinement types

## Type Refactoring: From Scripts to Programs

Advantage of scripting languages: primitives with flexible semantics to make programs concise.

Disadvantage: difficult to maintain over the long run.

- Lack of type means loss of design information, which has to be recovered every time

- Imagine programmers can simply add type annotations to a module and thus introduce a certain amount of type-safety into the program

Challenge:

- programmers loosely mix and match reasoning from various tyep disciplines.
- flow-oriented reasoning
- scheme has macro support, must be supported as much as possible

## Overview of Typed Scheme

### Occurrence Typing

example.

what it can solve:

how scheme programmers reason:

- ad-hoc type spec
- true union type
- predicate for type testing

in such cases occurrence typing requires minimal change to make it into Typed Scheme

### Refinement Type

boolean-valued functions can be treated as defining a type, which is the subset of input type.

- therefore occurrence typing has to work with arbitrary predicates

### Other Type system features

- true union types
- first-class polymorphic functions (impredicative polymorphism)
- explicitly specify recursive types

### S-expression

?

### Other Important Scheme Features

- `apply` function
- multiple value return mechanism
- use of arbitrary non-false values in conds
- variable-arity / multiple-arity functions

### Macros

- macro expansion before typechecking
- works for simple macro & some that we can infer types for generated variables
- complex macros remain future work.

## Two Examples of Refinements

### Form Validation

- idea: avoid SQL injection by sanitizing user input

- problem: sanitized input are still strings, so we need refinement.

- requires two pieces:

    - predicate: `sql-safe?`
    - final consumer (the function that consumes sanitized user input??)

- Alternative: sanitize in a different module, making SQLSafeString opaque

    - refinement type avoids this

### Restricted Grammars

- idea: describe a subset of data that are valid only in some contexts
- (skipping content)

## A Formal Model of Typed Scheme

### Syntax and operational semantics

- new stuff: Latent predicate and Visible predicate

- standard operational semantics (no runtime check?)

### Preliminaries

- support for assigning distinct types to distinct occurrences of variable
  based on control flow criteria.

  My note: in other words, a variable can have different type depending on its
  context, different occurrence might result in different types.
  This captures the notion of flow-sensitive typing.

Visible Predicates: (TODO) not sure what it means

Latent Predicates: seems like an extension of arrow type (function type),
which can be recognized as a discriminator for a specific type.

(TODO) does contract works better since that provides runtime checks?
