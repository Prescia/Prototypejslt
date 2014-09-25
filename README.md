Prototypejslt
=============

A split of prototypeJS to hold only the basic functions and avoid conflicts

The basic version, prototype_oop.js, adds only the bare necessary to create and handle classes, objects and hashes.
The prototype_ajax.js builds on top of that to add all the ajax handling functions

A possible future version might include element controls, but that would require not just spliting prototype,
but actually rewriting parts of it to remove any reference to the $ function, since the whole point here is to make a 
REALY no-conflict version of prototype

Sure good jQuery and other libraries might use proper closure, but there are 2 good reasons to still want prototype_oop.js:

1. You will never care if whatever other libraries can conflict with it
2. What other libraries? if you just want a basic OO handling, you can have it with less than 40k, instead of almost 200k
