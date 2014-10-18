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

Here is a sample javascript to create your own object with properties and methors, just like on prototypejs:

myClass= Class.create();
myClass.prototype = {
    _someVar: 0, // I like to leave variables starting with _
    othervariable: true, // not mandatory
    initialize: function(someParameterOnCreate) { // this is the constructor on prototypejs
        this._someVar = someParameterOnCreate;
        alert('yes, we are up!');
    },
    incSomeVar: function() { // this is how you declare functions
        this._someVar++;
    }
}

// Create instance (will alert 'yes, we are up!'):
var myInstance = new myClass(5);
// so this should alert "5":
alert(myInstance._someVar);
// call that function!
myInstance.incSomeVar();
// now it should alert "6":
alert(myInstance._someVar);
