# Safe & Efficient Gradual Typing for TypeScript

- differntial subtyping: computes minimum amount of runtime type info
- erasure modality: safely and selectively erase type info

TypeScript: JavaScript with optional type annotation.

- object oriented  gradual type system
- compiler erases all type info
- intentionally unsound

- extended to support a sound variant
- instrument by using a runtime library

- Partial Erasure: "any" <=> RTTI

- Programming style: Object uses in JS: dictionary vs. Object method carrier
- use of null vs. undefined
- type-safety aspect of the type system?

- Nominal classes and structural interfaces

- RTTI-based gradual typing

    - user-defined types are registered in RT
    - objects are tagged and never become less precise as it evolves.
    - shallowly tagged
    - not descending into a structure to tag, but when needed, accessed values are shallowly tagged.

- Differential subtyping

    - only type as necessary (omitting facts that can be statically determined)
    - splitting

- erased type: info hiding, performance.

## Summary

- differential subtyping
- erasure modality

- proposals are "intentionally unsound" to be usable. type annotation does not prevent runtime type error
- TypeScript won't check at runtime?
- objects are instrumented with runtime type info
- propagate invariants only when needed, not descending info an Object unless necessary
- minimize runtime info as we go by the observation that static type discipline are unnecessary to check at runtime
- allow fully erasing type info either by programmer

- aspects of JS:

    - Object as dictionary
    - Object that implements methods

- exceptions?

# Parts


