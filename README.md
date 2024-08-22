# `null-lang`

## Version History

**8\/21/2024: `v1.0`**
> \- Updated README.md with roadmap for NULL programming language <br>
> \- Sections Added: <br>
> - S

## TODO:
> \- Design syntax grammar for NULL <br>
> \- Create lexer/scanner <br>
> \- Create parser <br>
> \- Create AST <br>
> \- Create evaluator <br>


## Description

NULL-Lang is my attempt to create an object-oriented interpreted programming language using **Java**.

## Documentation

Below is my **'vision'** for the full documentation for writing NULL code:

### NULL File

NULL code must be written in a `.nul` file. To run a NULL program, run the following command: `jnull file.nul`

### Comments

For comments, use `$` for a **single-line comment** and `$** *$` for multi-line comment.

```
$ Single-line comment 

$**
 * - - - - - - - - - 
 * Multi-line comment
 * - - - - - - - - -
*$
```

### Printing to Console

For printing to the console, you will use the `printout` keyword followed by any literal or expression.

```
$ Prints a string
printout "String";    

$ Prints a number
printout 192;

$ Prints a boolean value
printout false;

$ Prints an expression
printout 8 * (7 - 2);  
```

### Datatypes

In NULL, the only datatypes provided will be the following:
- Integers   `int`
- Floats     `flt`
- Strings    `str`
- Booleans   `bool`

### Variables & Assignment

Defining variables requires the use of the keyword `var` followed by `#<d_type>` with <d_type> being a datatype. Following the datatype is the name of the variable 

```
var #int a := 6;
var #flt b := 123.4;
var #str c := "Hello World!";
var #bool d := true;
```

### Collections


### Logical Expressions


### Conditionals


### Loops


### Functions


### Classes


### Inheritance

