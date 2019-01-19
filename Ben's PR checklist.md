# Ben's PR checklist

## Goals
This guide is an outline of things to look for when reviewing a pull request for an Android app. It is not an exacting specification of all possible issues, rather an general overview of potential problem areas. Use your judgement in context when applying these guidelines.

## Code style
* Lines too long
* too many nested function calls `doFoo(createFactory(bar.items().toList()), getHandler())`
* too many nested callbacks
* too many nested if statements
* verbose function names indicating many operations `maybeGenerateKeyOrRetrieveKey()`
* overly generic class/variable/function names
* non-obvious abbreviated variable names. `i`/`x`/`y` are OK when used to represent index, X position, and Y position respectively, but would otherwise be frowned upon. 

## OO design
1. Parallel inheritance hierarchies
2. Super classes which depend on concrete classes calling into them
3. Super classes which expose writable properties to subclasses
 