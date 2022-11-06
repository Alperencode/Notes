# References

<hr>

## Call by value

### In short: Call by value is when the value of the variable is passed as an argument. The function can't change the value of the variable because it's the copy of the value.

### It costs more memory because it copies the value and creates temporary variable in memory.

<br>

- In this parameter passing method, values of actual parameters are copied to function’s formal parameters and the two types of parameters are stored in different memory locations. So any changes made inside functions are not reflected in actual parameters of the caller.

- While calling a function, we pass values of variables to it. Such functions are known as “Call By Values”.

<br>

## Call by reference

### In short: Unlike the call by value, call by reference is when the reference of the variable is passed as an argument. The function can change the value of the variable because it's the reference of the variable (memory address). 

### This is more efficient than call by value because it doesn't creates a copy the value. It just passes the reference of the variable.

<br>

- Both the actual and formal parameters refer to the same locations, so any changes made inside the function are actually reflected in actual parameters of the caller.

- While calling a function, instead of passing the values of variables, we pass address of variables (location of variables) to the function known as “Call By References