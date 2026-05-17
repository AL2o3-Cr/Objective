# The Objective language is composed entirely of objects.

## File extensions:
* .oj (ObJect)
* .uj (Universal obJect)
* .ej (Executable obJect)
* .pj (Point obJect)
* .ojs (ObJective Script)

## Parents and Children

This is a system similar to inheritance, but it also works like composition.

A parent is an object used as a template for creating a child.

In `int num`, *int* is the parent, *num* is the child. But here, num is not of class int, but is the child, which is of great importance in non-pj objects.

## uj, ej, and pj

oj is the original object from which the main trinity is born.
uj - structures the program and contains other objects.
ej - contains the executable code, as well as temporary variables of types pj and uj.
pj - contains data, its structure: {name;data;type}

## Addressing

You can always access `ga` (global address).
`ga:0` - direct access to the language.

`ga:1` - the main file of the current execution.
`ga:2` - general imports.

`ga:3` ~ `ga:255` - other execution files not related to imports. Can be configured. By default, `ga:5` contains the system.

Example: `ga:1.1` is the executable file header.

There is also `la` (local address).
`sga`/`sla` (string global/local address) - text representation.

## Built-in:
### Types:
* dict - contains up to 250 named objects, descendant of uj
* arr - indexed set of objects, descendant of uj
* bit - one bit, descendant of pj
* byte - one byte, pj
* str - a set of bytes specialized for writing text, pj
* num - a set of bytes for writing any number, expandable as needed
* file - file system access objects, i.e., I/O, descendant of oj
* ej - an object containing executable code
* code("async" or "threads") - an object containing code executed non-sequentially or multithreaded, ej is parent

### Functions

* ifs(bit$cond, oj$true,\ oj$false);  
* while(bit$cond, oj$true,\ oj$finally);  
* foreach(uj$code, num || uj,\ uj$finally);  
* switch(uj$var, dict$answers,\ uj$false);  
i.e.
