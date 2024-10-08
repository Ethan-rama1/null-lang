# `null-lang`

## Version History

**8\/21/2024: `v1.0`**
> \- Created repository <br>
> \- Updated README.md with roadmap for NULL programming language <br>
> \- Sections Added: <br>
> &ensp;&ensp;&ensp;&ensp; + Description <br>
> &ensp;&ensp;&ensp;&ensp; + Documentation <br>

**8\/22/2024: `v1.01`**
> \- Updated documentation: <br>
> &ensp;&ensp;&ensp;&ensp; + Conditionals <br>
> &ensp;&ensp;&ensp;&ensp; + Loops <br>
> &ensp;&ensp;&ensp;&ensp; + Functions <br>

**8\/25/2024: `v1.02`**
> \- Updated documentation: <br>
> &ensp;&ensp;&ensp;&ensp; + Classes <br>
> &ensp;&ensp;&ensp;&ensp; + Inheritance <br>

**8\/26/2024: `v1.03`**
> \- Updated grammar rules for NULL: <br>
> &ensp;&ensp;&ensp;&ensp; + Declarations <br>
> &ensp;&ensp;&ensp;&ensp; + Lexical <br>
> &ensp;&ensp;&ensp;&ensp; + Expressions <br>
> &ensp;&ensp;&ensp;&ensp; + Statements <br>
> &ensp;&ensp;&ensp;&ensp; + Simplification <br>

## TODO:
> \- Design syntax grammar for NULL <br>
> \- Create lexer/scanner to scan all tokens in NULL programs <br>
> \- Create parser to parse all tokens found <br>
> \- Create AST to order all tokens according to grammar <br>
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

For conditionals, we use `if (<bool expr>) { <expr> }` for 'if' statements. To use 'else-if' or 'else' statements, we use `elif (<bool expr>) { <expr> }` and `else { <expr> }` following the closing brace `}`. Below is some example code utilizing conditionals in NULL:

```
var #int a := 5;

if (a > 5) {
    printout "Greater than 5";
} elif (a < 5) {
    printout "Less than 5";
} else {
    printout "Equal to 5;
}
```


### Loops

We have two different types of loops: while loops and for loops. We use `while (<condition>) { <expr> }` for while loops and `for (var #int i := <value>; <condition>; <update>) { <expr> }`. Below is some example code utilizing loops in NULL:

```
var #int sum := 0
for (var #int i := 0; i < 10; i := i + 1) {
    sum := sum + i;
    printout sum;    $ Print current sum of values 1-10
}

var #int num := 5302
while (num != 0) {
    printout num % 10;   $ Prints each digit in number
    num := num / 10;
}
```


### Functions

Functions have a couple of syntax including defining functions and making function calls. For defining functions, we use `func #<type> <name>(#<type_1> <param_1>, #<type_2> <param_2>, . . .) { <expr> }` with `#<type>` and parameters being optional. For function calls, we use `<name>(<args>);`. For functions with return types, we use `ret <value>` to return values from a function. Below is some example code demonstrating defining and calling functions:

```
func #int add(#int a, #int b) {
    ret a + b;
}

func writeFoo() {
    printout "Foo";
}

printout add(5, 7);   $ Prints 12
writeFoo();   $ Performs code in writeFoo function
```


### Classes

Classes have many syntaxes including defining a class, instantiating objects, and default methods in classes such as the constructor, toString, and equals methods. For defining classes, we use `@class <name> { <attributes> <methods> }`. For instantiating objects, we use `@<class_name> <name> := <class_name>(<attributes>)`. Below is some example code defining classes and instantiating objects:

```
@class Person {
    var #str name;
    var #int age;

    func Person(#str name, #int age) {
        this.name = name;
        this.age = age;
    }

    func #str toString() {
        ret name + " " + age;
    }

    func #bool equals(@Object o) {
        if (this == o) {
            ret true;
        }
        if (o == null or getClass() != o.getClass()) {
            ret false;
        }
        @Person person := (@Person) o;
        ret @Objects.equals(name, person.name) && @Objects.equals(age, person.age);
    }
}

@Person p1 = Person("John Doe", 30);
@Person p2 = p1;
printout p1.toString();
printoout p1.equals(p2);
```


### Inheritance

Class inheritance works similarly to java. For defining an inherited class, we use: `@class <i_name> -> <base> { <attributes> <methods> }`. To override inherited methods from base class, we use: `@replace func <ret_type> <name>(<params>) { }`. To call superclass' constructor in subclass constructor, we use: `super(<args>);`. Below is some example code defining inherited classes:

```
@class Tree {
    var #int height;
    var #int age;

    func Tree(#int height, #int age) {
        this.height = height;
        this.age = age;
    }
}

@class AppleTree -> Tree {
    var #int height;
    var #int age;
    var #str fruit;

    func AppleTree(#int height, #int age, #int fruit) {
        super(height, age);
        this.fruit = fruit;
    }
}
```


## NULL Grammar

Here we define a list of tokens that will be used in the grammar:

### Declarations:

```
DECLARATION ::= VAR_DEC | FUNC_DEC | CLASS_DEC | STATEMENT ;
VAR_DEC     ::= "var" DATATYPE IDENTIFIER (":=" EXPRESSION)? ";" ;  
FUNC_DEC    ::= "func" FUNCTION ;
CLASS_DEC   ::= "@class" IDENTIFIER ( "->" IDENTIFIER )? "{" FUNCTION* "}" ;
```

### Statements:

```
STATEMENT    ::= EXPR_STMT | FOR_STMT | IF_STMT | ELIF_STMT | PRINT_STMT | RET_STMT | WHILE_STMT | BLOCK ;
EXPR_STMT    ::= EXPRESSION ";" ;
FOR_STMT     ::= "for" "(" ( VAR_DEC | EXPR_STMT ";" ) EXPRESSION? ";" EXPRESSION? ")" BLOCK ;
IF_STMT      ::= "if" "(" EXPRESSION ")" BLOCK ELIF_STMT* ( "else" BLOCK )? ;
ELIF_STMT    ::= "elif" "(" EXPRESSION ")" BLOCK ;
PRINT_STMT   ::= "printout" EXPRESSION ";"
RET_STMT     ::= "ret" EXPRESSION ";"
WHILE_STMT   ::= "while" "(" EXPRESSION ")" BLOCK ;
BLOCK        ::= "{" DECLARATION* "}" ;
```

### Expressions:

```
EXPRESSION    ::= ASSIGNMENT ;
ASSIGNMENT    ::= ( CALL "." )? IDENTIFIER ":=" ASSIGNMENT | LOGIC_OR ; 
LOGIC_OR      ::= LOGIC_AND ( "or" LOGIC_AND )* ;
LOGIC_AND     ::= EQUALITY ( "and" EQUALITY )* ;
EQUALITY      ::= COMPARISON ( ( "!=" | "==" ) COMPARISON )* ;
COMPARISON    ::= TERM ( ( ">" | ">=" | "<" | "<=" ) TERM )* ;
TERM          ::= FACTOR ( ( "+" | "-" ) FACTOR )* ;
FACTOR        ::= UNARY ( ( "*" | "/" ) UNARY )* ;
UNARY         ::= ( "!" | "-" ) UNARY | CALL ; 
CALL          ::= PRIMARY ( "(" ARGS ")" | "." IDENTIFIER )* ;
PRIMARY       ::= "true" | "false" | "null" | "this" | NUMBER | STRING | IDENTIFIER | "(" EXPRESSION ")" | "super" "." IDENTIFIER ; 
```

### Simplification

```
FUNCTION    ::= ( RET_TYPE )? IDENTIFIER "(" ( PARAMS )? ")" BLOCK ;
DATATYPE    ::= "#" TYPE ;
TYPE        ::= "int" | "str" | "flt" | "bool" ;
RET_TYPE    ::= "#" TYPE ;
PARAMS      ::= DATATYPE IDENTIFIER ( "," DATATYPE IDENTIFIER )* ;
ARGS        ::= IDENTIFIER ( "," IDENTIFIER )* ;
```

### Lexical

```
NUMBER      ::= DIGIT+ ( "." DIGIT+ )? ;
STRING      ::= "\"" (any non-"\"" character)* "\"" ;
IDENTIFIER  ::= ALPHA ( ALPHA | DIGIT )* ;
ALPHA       ::= [a-zA-Z_] ;
DIGIT       ::= [0-9] ;
```
