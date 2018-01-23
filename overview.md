- Python

    - dynamic language, do runtime check insertion

    - experiment design choices

    - has the notion of Class and object

        - introduced type alias

    - practical effect?

- JavaScript

    q: does Safe TypeScript extends TypeScript or JavaScript?

    - dynamic language, runtime check insertion

    - target soundness

    - optimize done by

        - removing unnecessary checks if the info is statically known

        - shallow tagging

- Typed Scheme

    - dynamic language (doesn't seem to have runtime checks?)

    - relating predicate and type, boolean plays a special role here

    - practical:

        - ad-hoc type spec

        - predicate for type testing -> require flow-sensitive analysis

- C#

    - static language that has to interoperate with dynamic languages

    - extend type system to allow

        - runtime checks
        - dynamic object to add / remove property at runtime

- Smalltalk (TODO)
