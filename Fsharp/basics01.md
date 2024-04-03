# FSharp basics

## What does :? mean in F#
%
In F#, the :? operator is used for type testing.  
It checks if a particular instance is of a specific type at runtime.  
This is similar to the is keyword in C#.

## What are partially active patterns?
%
F.e.:
> let (|ObjArray|_|) (x:obj) = defines a partial active pattern named ObjArray. 

The function takes one parameter x of type obj.  
This function can be used in a pattern matching expression to try to convert an object into an array of objects and handle the result.  

For example:
```fsharp
match obj with
| ObjArray arr -> printfn "Array length: %d" arr.Length
| _ -> printfn "Object is not an array"
```

## explain the following code 

```fsharp
let (|IsEven|IsOdd|) x = 
    if x % 2 = 0 then 
        IsEven 
    else 
        IsOdd

let num = 5
match num with
| IsEven -> printfn "The number is even"
| IsOdd -> printfn "The number is odd"

```
%

This is an active pattern used to return odd and even result as a value in F#
