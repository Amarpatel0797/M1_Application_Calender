# A simple calculator written in C

# Introduction:-   
Simple calculator is a project to allow users to calculate basic four operations in mathematics ,they are addition, subtraction, multiplication, division but in this Project
which I'm Implementing ,also included three additional operations such as Factorial, Power ,modulas .However, the input has to be in the form "number1 operator1 number2
"(i.e 10+5).    


### RATIONALE:
I did this implementaion because I did not find a nice implemenation of a "full formula" calculator online: I only found simple examples that support only one operator.
This implementation supports full formulas (limited only by the size of the stack and the queue).

### FEATURES / KNOWN ISSUES
Accepts the following operators:
 * +: sum
 * -: sub
 * *: multiplication
 * /: division
 * %: modulus
 * ^: exponentiation
 * (): used to change default precedence

Current implementation is a Proof of Concept, aiming at keeping the code clear.
As such, it has very strong limitations:

 * Only integer artihmetic supported
 * Stack and Queue used are limited in capacity (hardcoded value)
 * It accepts some expressions like "()1+1", whereas tools like "bc" reject those
 * Error messages can be improved
 * Input parser does not recognize negative numbers. However, easy workaround is to write "(0-1)" instead of "-1"
 * Acually, it does not support any unary operator (-, +, ! ...). Adding support is tricky and error-prone
   * For instance, if we accept "~" as the unary minus, expressions like "\~1" and "1\~" would both produce "-1"
   * To avoid this more logic needs to be added, and this is beyond the scope of this project
 * In order to add correct support for unary operators, a grammar definition and parser should be used (think of lex + yacc)


### HOW TO USE IT:
Compile and run:
./calculator "expression".

You can use quotes if your expression contains spaces or parenthesis.
Alternatively, you can avoid spaces and scape parenthesis.

EXAMPLES:
```
./calculator 1+1+2-3
result: 1

./calculator 16/2/2
result: 4

./calculator 16/\(2/2\)
result: 16

./calculator " 1 + 2 * (3 - 5) * 6"
result: -23

./calculator "16/(2/2)"
result: 16

/calculator "16 % 2 % 1"
result: 0

./calculator "16 % (2 % 1)"
Modulo by zero

./calculator "2^3"
result: 8
```


# SDLC Activity Based Learning
Build | Code Quality | Git Inspector | code quality score | code grade |
|---------|------------|-------------|--------------------|------------
|[![C/C++ CI](https://github.com/yogishR/Stepin_c_minproject/actions/workflows/c++.yml/badge.svg)](https://github.com/yogishR/Stepin_c_minproject/actions/workflows/c++.yml)| [![Unit Testing - Unity](https://github.com/yogishR/Stepin_c_minproject/actions/workflows/unity.yml/badge.svg)](https://github.com/yogishR/Stepin_c_minproject/actions/workflows/unity.yml)| [![Contribution Check - Git Inspector](https://github.com/yogishR/Stepin_c_minproject/actions/workflows/codeinspector.yml/badge.svg)](https://github.com/yogishR/Stepin_c_minproject/actions/workflows/codeinspector.yml)|  [![Static Code Quality- Cppcheck](https://github.com/yogishR/Stepin_c_minproject/actions/workflows/cpp.yml/badge.svg)](https://github.com/yogishR/Stepin_c_minproject/actions/workflows/cpp.yml) | ![Code Quality Score](https://www.code-inspector.com/project/27777/score/svg) |![Code Badge](https://www.code-inspector.com/project/27777/status/svg)
