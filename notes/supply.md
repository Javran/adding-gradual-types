# Safe TypeScript

- as a compiler that compiles TypeScript into JavaScript

- JavaScript
    - prototype-based, can encode class-based object oriented idioms.
    - Objects
        - used as mutable dictonaries
        - to expose methods
    - `null` vs. `undefined`

(1)

typical JavaScript that checks value type at runtime:

```javascript
function f(x) {
    if (typeof x === 'string') {
        ...
    }
}
f(1)
f('1')
```

Safe TypeScript:

```javascript
function f(x : string) {
    ...
}
f(1) // fail statically
f('1')
```

(2) Nominal class and structural interfaces

structural interface is insufficient to capture inheritance-related constraints

```javascript
class Point { x: number; y: number; ... }
class MovablePoint extends Point {
    ...
}

function f(p : Point) {
    ...
}

f(new Point(x,y))
f(new MovablePoint(x,y))
f(new Point(x,y))
f({x: ..., y: ...}) // ?
```

(3) performance concerns

# Reticulated Python

- source to source compiler

- Python 3

    - already have syntax support for optional types
    - has both inheritance and duck typing
    - doesn't know what module would be loaded ahead of time, therefore load time typechecking

# CSharp 4.0

- implemented at compiler level

- CSharp 3.0

    - statically typed
    - string-based interface for calling into other languages

(1) interop

```c#
...
ScriptObject map = win.CreateInstance("VEMap", "myMap")
map.Invoke("LoadMap")
...
```

Improved:

```c#
...
dynamic map = win.CreateInstance("VEMap", "myMap")
map.LoadMap()
...
```

(2) Expando Object

Use feature intended for dynamic langauge in CSharp

```c#
...
dynamic employee = new ExpandoObject()
employee.Name = "Erik"
employee.Address = new ExpandObject()
employee.Address.State = "WA"
Console.WriteLine(employee.Address.State)
employee.Address.Remove("State")
Console.WriteLine(employee.Address.State) // throw an error
...
```
