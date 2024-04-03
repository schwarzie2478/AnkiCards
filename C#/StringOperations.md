# String Operations in C#

## How to insert a character in a string?

%
You can use a stringbuilder to do string operations. This class has an insert function that allows you to add a character or string at a certain location.

## How to iterate over an string?

%
The most straightforward solution to convert to a chararray.  
But this doesn't work well when dealing with special characters in other languages!  
There you need to split the string with the following method:   
```CSharp
    var graphemes = StringInfo.GetTextElementEnumerator(str);
```
