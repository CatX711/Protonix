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
    String::new("") <-- create a new string
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
In Protonix, we use :: to assign something to another thing. The way we define a function is by assinging `main` open and closes brackets. This is what makes it a function.

<br />
<br />

Main is the entry point to every Protonix program, so main's code will be prioritized over everything else. <br />


<br />
<br />
<br />

# Variables

<br />
<br />





<!--
Syntax test
```rs
include stdio::*

main :: (){
    var mystring String::new("Bolablaca")

    print("Hello from the Protonix Compiler!")
    print("{!mystring}")

    stdio::scan(something i dunno);
}
```
-->
