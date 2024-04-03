# General Knowledge & random tidbits
## What is an ghrapheme cluster?

%
A “character” may not be just a single Unicode code point.  
Instead, that basic unit may be made up of multiple Unicode code points.  
When breaking up an string into characters,  
some special characters in certain language are represented by their Unicode.  
This is called a ghrapheme cluster.  

So you should use a different way to get individual chars from strings  
( in .NET String has the method GetTextElements)

