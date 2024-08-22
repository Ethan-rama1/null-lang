# `null-lang`

## Version History

**8\/21/2024: `v1.0`**
> \- Created repository <br>
> \- Updated README.md with roadmap for NULL programming language <br>
> \- Sections Added: <br>
> &ensp;&ensp;&ensp;&ensp; + Description <br>
> &ensp;&ensp;&ensp;&ensp; + Documentation <br>

**8\/22/2024: `v1.01`**
> \- Updated documentation:
> &ensp;&ensp;&ensp;&ensp; + Conditionals <br>

## TODO:
> \- Design syntax grammar for NULL <br>
> \- Create lexer/scanner to scan all tokens in NULL programs <br>
> \- Create parser to parse all tokens found <br>
> \- Create AST to  <br>
> \- Create evaluator to interpret NULL code: <br>
> &ensp;&ensp;&ensp;&ensp; + Implement binary operations <br>
> &ensp;&ensp;&ensp;&ensp; + Implement unary operations <br>
> &ensp;&ensp;&ensp;&ensp; + Implement printing <br>
> &ensp;&ensp;&ensp;&ensp; + Implement variable assignments <br>
> &ensp;&ensp;&ensp;&ensp; + Implement blocks <br>
> &ensp;&ensp;&ensp;&ensp; + Implement conditionals <br>
> &ensp;&ensp;&ensp;&ensp; + Implement loops <br>
> &ensp;&ensp;&ensp;&ensp; + Implement functions <br>
> &ensp;&ensp;&ensp;&ensp; + Implement classes <br>
> &ensp;&ensp;&ensp;&ensp; + Implement inheritance <br>


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

### Logical, Relational, and Comparison Operators

Let's assume we have the following variables defined:

```
var #bool a := true;
var #bool b := false;
var #int c := 13;
var #int d := 19;
```

For logical operators, we have `and` for the **AND** boolean operation, `or` for the **OR** boolean operation, and `not` for the **NOT** boolean operation:

```
printout a and b    $ Prints 'false'
printout a or b     $ Prints 'true'
printout not a      $ Prints 'false'
```

Next, we have the relational and comparison operators:

| Operator | Example                   |
|----------|---------------------------|
| `>`      | `c > d    $ 'false'`      |
| `<`      | `c < d    $ 'true'`       |
| `>=`     | `c >= d   $ 'false'`      |
| `<=`     | `c <= d   $ 'true'`       |
| `==`     | `c == d   $ 'false'`      |
| `!=`     | `c != d   $ 'true'`       |


### Conditionals

For conditionals, we have the if statement


### Loops


### Functions


### Classes


### Inheritance

