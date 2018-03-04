# Gradual Typing for Functional Languages

Motivation: integrate static and dynamic typing and thereby combine the benefit of both.

Intuition: structure of a type may be partially known / unknown at compile time,
job of the type system is to capture known incompatibilities.

"pay-as-you-go"

Program result: either expected value, cast error, but never type error.

- Other similar:

    - improve runtime performance by using annotation
    - Soft typing
