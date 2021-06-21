# Reading Notes
## Authentication
_____________________________________________________________________________________________________________________________________


### Explain what a “Singleton” is (in Computer Science terms)
- the singleton pattern is a software design pattern that restricts the instantiation of a class to one "single" instance. This is useful when exactly one object is needed to coordinate actions across the system.
Source - [Wikipedia, the free encyclopedia](https://en.wikipedia.org/wiki/Singleton_pattern)

### Explain how the Singleton pattern can be used with Node modules, specifically with classes
- Modules are cached after the first time they are loaded. This means (among other things) that every call to require(‘foo’) will get exactly the same object returned, if it would resolve to the same file.
Source - [Arek Jaworski](https://medium.com/swlh/node-js-and-singleton-pattern-7b08d11c726a)

### If you were tasked with building a middleware system like Express uses, what approach might you take to construct/operate it?

```
class PrivateSingleton {
    constructor() {
        this.message = 'I am an instance';
    }
}
class Singleton {
    constructor() {
        throw new Error('Use Singleton.getInstance()');
    }
    static getInstance() {
        if (!Singleton.instance) {
            Singleton.instance = new PrivateSingleton();
        }
        return Singleton.instance;
    }
}
module.exports = Singleton;
```

Source - [Arek Jaworski](https://medium.com/swlh/node-js-and-singleton-pattern-7b08d11c726a)

### Vocabulary 

Router Middleware - a middleware function with no mount path. This code is executed for every request to the router

Dynamic Module Loading - is a mechanism by which a computer program can, at run time, load a library (or other binary) into memory, retrieve the addresses of functions and variables contained in the library, execute those functions or access those variables, and unload the library from memory.

Singleton Pattern - the singleton pattern is a software design pattern that restricts the instantiation of a class to one "single" instance.

CRUD -> REST method matches -
```
Create = PUT with a new URI
         POST to a base URI returning a newly created URI
Read   = GET
Update = PUT with an existing URI
Delete = DELETE
```
Mock Testing -  is an approach to unit testing that lets you make assertions about how the code under test is interacting with other system modules.


