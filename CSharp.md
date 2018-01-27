# Adding Dynamic Types to C-Sharp

Abstract:

- statically typed languages has to interoperate with APIs and object models defined
  in dynamic languages

- deferring type checking for program fragments until runtime

- subtyping remains transitive (what does this mean?)

## Introduction

- web-based application tends to use dynamic languages,
  statically typed languages has to interoperate.

- DLR: Dynamic Language Runtime on top of CLR (Commmon Language Runtime)

- applicable to any class-based object-oriented languages

## An Introduction to Dynamic Types in CS4.0

### JavaScript Access in Sliverlight

- formerly: string-based interoperation.
- now: new type `dynamic`

- C# resolution at runtime (what does this mean?)

### COM Interop

hmmm....

### Expando Object

- allow adding and removing property at runtime

### Dynamic Binding of Ordinary Objects

- (?) C#'s overload resolution

### Dynamic Conversions

allow assigning dynamic value to static ones, with runtime checks

## An Overview of the C# Type System

- Bidirectional type system

    two phases: type checking and type synthesis

    type checking: determine whether a specific term can be assigned a specific type
    type synthesis: determine a type from a given term (used when we do not know anything about an exp)

- coercive subtyping: generate coercions when determining subtyping

- one do not need to forgo transitivity as said

## Source Language: Featherweight CS4.0

FCS4 = CS4 simplified while retaining being a valid subset of it.

Simplification:

- `public` only, no static method, all are `virtual` or `override`.
- `bool`, `int` and `byte` as value types
- class type (with `object` and `dynamic`) and delegate are reference types

Ordinary expression & Statement expression
