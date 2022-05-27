# CSC3002-Review-Question-Unofficial-Answer



## Ch1: Overview of C++

1. Source file.
2. `//` and `/*  */`. 
3. `< >` for C++ Standard library like `<iostream>`, ` <vector>`; `" "` for External library defined by users like `“morsecode.h”`.
4. `const double CENTIMETERS_PER_INCH = 2.54;`
5. `main`; `return 0;`. 
6. Line break, end current line and output a new line.
7. `int i = 0;` means `int(type) i(name) = 0(value); `. Scope is $-2^{31} \sim 2^{31}-1$. 
8. a, b, c, f, h, k, l

<img src="images/ch1a.png" style="zoom: 67%;" />

9. domain of values & operations
10. domain of values & operations
11. ASCII = *America Standard Code for Information Interchange*
12. true(1), false(0)
13. `double x;`,  `cin >> x;`
14. `cout << “i=” << i << “ d = ” << d << “ c = ” << c << “ s = “ << s;`
15. 5 (`int`), 3 (`int`), 3.8 (`double`), 18.0 (`double`), 4 (`int`), 2 (`int`)
16. **Unary minus**: represent negative number, can work as the left value; **Subtraction**: minus two numbers, an operation, requires two numbers to operate.   
17. When a number exceeds the scope of its type, the number’s bit will be cut down for assignment.

<img src="images/ch1b.png" style="zoom:50%;" />

18. Transform a type to another type. `int i; double j = 9.9; i = int(j);`

19. (a) 4; (b) 2; (c) 42; (d) 42.

20. `a = (x>y) ? x: y;`

21. `++x`: add x by 1 and return; `x++`: return x first and then add x by 1;

22. Only calculate right-side value when necessary. E.g., `if (1 == 1 || x = y)`: this will not judge whether x equals to y since left term is always `true`.

23. ```cpp
    if (/*condition*/){ /*expression1*/ } else{ /*expression2*/ };
    switch(/*variable*/){
        case 1:{ /*expression1*/ break;} 
        case 2:{ /*expression2*/ break;}
        default:{ /*expressionx*/ break;}
    }
    while(/*condition*/){
        /*expression*/
    }
    for (/*init*/;/*stop*/;/*step*/){ /*expression*/ }
    ```

24. Select a case to execute. `break` means exit current switch statement, or the program will execute the consecutive next case.

25. The value to stop iteration.

26. ```cpp
    for (int i=1;i<=100;i++) {  }
    for (int i=0;i<100;i+=7) {  }   
    for (int i=100;i>=0; i-=2) {  }
    ```

    

## Ch2 Functions and Libraries

1. **Function:** receive an input, give an output, part of the program. **Program:** a complete executing unit.
2. **Call:** Invoke the function. **Argument:** variables passed to the function. **Return:** function output value

3. **False.** No need to write a prototype every time, main() also doesn’t need.
4. `double sqrt(double i);`
5. Yes. For example, in `if` condition statement.
6. Function that returns a `bool` value.
7. *Overloading*: Define multiple implementation for the same function name (but different function parameters) Use signatures to choose the most appropriate implementation to invoke.

<img src="images/ch2a.png" alt="ch2a" style="zoom:50%;" />

8. Write the variable’s initial value in the prototype / function name. E.g., `int f(x, y = 0);`
9. False. `int f(x = 0, y)` is false, it will cause ambiguity when invoking `f(1)`;
10. The memory to store local variables (initialize in function).
11. The value of each argument is copied into the corresponding parameter variable when calling a function. 
12. Local is its scope, the variable’s life cycle is inside the function. When the function finished, the variable will be destructed. 
13. It means *call by reference* [doge], No new variables are created. 
14. Use &. E.g., `func(ostream & os)`

15. Explanation from slides: 

    <img src="images/ch2b.png" alt="ch2b" style="zoom:50%;" />

<img src="images/ch2c.png" alt="ch2c" style="zoom: 80%;" />

16. `#include “mylib.h”`
17. Use `extern`
18. Unified, Simple, Sufficient, Flexible, Stable
19. Maintain the same structure and effect. Making changes in the behavior of a library forces clients to change their programs, this reduces its utility.
20. Pseudo random, which means it’s not actually pure random, but having some certain rules.
21. Largest `int` type number, $2^{31} - 1$. 

22. Explanation from textbook: 

<img src="images/ch2d.png" alt="ch2d" style="zoom:50%;" />

23. `randomInteger(1, 100)`
24. It depends on the implementation actually. For Stanford Library’s case, the answer is Yes, be like $\{-5, -4, -3, …, 3,4\}$. The source code: 

<img src="images/ch2e.png" alt="ch2e" style="zoom:50%;" />

25. No, `d1` and `d2` will have the same value.
26. true (if not set the seed according to current time)
27. Initial state of the random number, to generate random sequence.
28. Set the seed fixed.
29. Please see [Stanford Library random.h docs](https://web.stanford.edu/dept/cs_edu/resources/cslib_docs/random.html)

<img src="images/ch2f.png" alt="ch2f" style="zoom:50%;" />



## Ch3 Strings

