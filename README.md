# Protonix

<p align="center"> <img width="643" alt="Screenshot 2023-12-25 at 00 01 53" src="https://github.com/CatX711/Protonix/assets/104099162/1a9dfe3e-9558-421d-930f-0c05fd6d4544"> </p>

<br />
<br />

>*“Any fool can write code that a computer can understand. <br />
>Good programmers write code that humans can understand.”* <br />
>
>*― Martin Fowler*


<br />
<br />
<br />

**Protonix** is a generic use compiled programming language designed for ease of use and readability. It attempts to lessen the mass boilerplate which current-day languages are full of. The language does not contain semicolons (thank God).

<br />
<br />


DATATYPES:

```c
    INTEGERS:   
    int8 <-- 8 bit int  
    int16 <-- 16 bit int
    int32 <-- 32 bit int
    int64 <-- 64 bit int
    int128 <-- 128 bit int
    Icomplex <-- complex int

    ui8 <-- unsigned 8 bit int   
    ui16 <-- unsigned 16 bit int
    ui32 <- unsigned 32 bit int
    ui64 <-- unsigned 32 bit int
    ui128 <-- unsigned 128 bit int 

    FLOATS:   
    float32 <-- 32 bit float
    float64 <-- 64 bit float 

    BOOLEANS:
    TRUE <-- true bool
    FALSE <-- false bool

    STRINGS:
    String.new("") <-- create a new string
```    


<br />
<br />
<br />


# Hello

<br />
<br />

Here is a simple output program using Protonix.

<br />

FILENAME: hello.px
```rs

main :: (){
    print("Hello from the Protonix Compiler!")
}
```

<br />
<br />

As we can see, no standard library is needed to create a basic program. Variable definition, printing and outputting all comes with Protonix's compiler. Let's break this program down. <br />
In Protonix, we use :: to assign a type to another thing. The way we define a function is by assinging `main` some open and closes brackets. This is what makes it a function.
We are giving main the type of a function.

<br />
<br />

Main is the entry point to every Protonix program, so main's code will be prioritized over everything else. <br />


<br />
<br />
<br />

# Variables

<br />
<br />

Here is a program that defines two variables and then prints them. 

<br />

FILENAME: vars.px
```rs
main :: (){
    mystring :: String.new("Blablabla")
    myint :: int = 86

    print("{!mystring} {!myint}") // Blablabla 86
}
```

<br />
<br />

Here we create a new string using `String.new()` and giving it a value. <br />
We also make an integer variable with the value of 86. Use `{!}` to output variables.


<br />
<br />


# Functions 

<br />
<br />

Functions are very powerful in Protonix. They allow for seamless code reuse, without flooding memory. <br />
There are two types of functions: `Singular Return Type and Outcome-annotated Return Type` functions.

<br />
<br />
<br />

## Single Return Type Functions

<br />
<br />

Look at this example:

<br />

```rs
calculate_sum :: (a:int, b:int) -> int {
    return a + b
}
```

This function calculates the sum of two integer values (a and b). When passing in parameters, we have to describe the placeholder variables and their types. <br />
`Calculate_sum` has a singular return type of int, straightforwardly providing the result of the addition operation.

<br />

***Parameters:***

    a:int: First integer value for addition.
    b:int: Second integer value for addition.

<br />

***Returns:***

An int representing the sum of the two input integers (a + b).
Usage Example:

<br />

```rs
main :: (){
    result :: int = calculate_sum(5, 10)
    print("Result: {!result}") // 15
}
```

<br />
<br />
<br />

## Multiple Return Type Functions (Outcome-Annotated)

<br />

Here's an example of Outcome-annotated an function:

<br />
<br />


```rs
divide_numbers :: (a:float, b:float) -> Outcome<float, str> {
    if b == 0.0 {
        return Failure("Division by zero is not allowed.")
    } else {
        return Success(a / b)
    }
}
```

<br />
<br />


Description:

The divide_numbers function in Protonix divides two float values (a and b). It utilizes Outcome Annotations to manage potential outcomes, covering successful division scenarios and division by zero errors.

<br />
<br />

Parameters:

    a:float: Numerator value for division.
    b:float: Denominator value for division.

<br />

Returns:

An Outcome encompassing two possible scenarios:

    Success<float>: Indicates a successful division, returning a float result.
    Failure<str>: Signifies an error scenario, returning an error message (str) for division by zero cases.

<br />
<br />

Usage Example:

```js
main :: (){
    result :: Outcome<float, str> = divide_numbers(10.0, 2.0)
    
    check result {
        case Success(value) | print("Result: {!value}")
        case Failure(error) | print("Error: {!error}")
    }
}
```

<br />
<br />

Check is like a switch. "In a specific case, do this".
Use the pipe `|` to provide instructions on what to do in a specific case.

Behavior:

    For a non-zero denominator (b), the function returns a Success outcome with the division result (a / b) as a float.

    If the denominator (b) is zero, it returns a Failure outcome with the error message "Division by zero is not allowed."

Considerations:

    The functions demonstrate both singular return types and Outcome Annotations, providing examples of handling different return scenarios.

<br />
<br />

The best use case for Outcome-annotated Functions is when managing things that could easily fail and being able to <br />
throw an error. Also, it's good for having multiple outcomes 


<!--
Syntax test
```rs
include stdio::*

main :: (){
    mystring :: String.new("Bolablaca")

    print("Hello from the Protonix Compiler!")
    print("{!mystring}")

    stdio.scan(something i dunno);
}


Math :: its{
    
}

its Math{

}

toolkit Math{

}
```
-->
