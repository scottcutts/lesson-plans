# Arithmetic

Our first language will work parse and interpret arthimetic expressions. This will get us the basic framework for parsing and representing programs.

## Setup

Step zero is to setup a project. You'll want to add some dependencies:

- FastParse: http://www.lihaoyi.com/fastparse/
- Cats: https://typelevel.org/cats/

At this stage we're assuming you're comfortable creating Scala projects with your own preferred setup, but you can grab the setup from the solutions if you want.


## Numbers

Our very first interpreter will parse numbers and evaluate them to ... the number they represent. In more formal terms our language will recognise exactly one type of expression, a literal integer. We will parse these literals into a data structure, our abstract syntax tree (AST). We will then have an interpreter that evaluates the AST to produce a value. Since we only have one type of expressions we only need to represent one type of value.


## Expressions

Our next step is to extend our language with arithmetic expressions. To start with we'll just allow addition and subtraction of literals. More formally we'll have the grammar

Expr :=
    Literal  # This is what we've already implemented
  | Literal + Literal
  | Literal * Literal

At the moment you don't need to worry about precedence.