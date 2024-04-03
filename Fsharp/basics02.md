
# FSharp basics

## what is an discriminated union in f# and can you give an example
%
In F#, a discriminated union is a type that represents a sum type or a choice between multiple possible values. Each value, known as a union case, is tagged with a label or case identifier, allowing them to be distinguished from one another. Discriminated unions are a powerful feature in F# that enable concise and expressive modeling of data structures and domain-specific concepts.


Here's an example of how to define and use a discriminated union in F#:


```fsharp
type Shape =
    | Circle of float
    | Rectangle of float * float
    | Triangle of float * float * float
```
## How to take in arguments in F#
Body
%
You can provide an main method with an decorator indicating that this is the entrypoint of the program


```fsharp
[<EntryPoint>]
let main args =
    printfn "Arguments passed to function : %A" args
    // Return 0. This indicates success.

```
