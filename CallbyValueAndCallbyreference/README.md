## Call by Value and Call by reference in C

1. **Call by Value (CBV)**:
    - In CBV, the **values** of actual parameters (variables defined in the calling function) are **copied** into the formal parameters (variables declared in the invoked function).
    - There are **two separate copies** of parameters stored in different memory locations: the original copy and the function's copy.
    - Any changes made inside the function do **not** affect the actual parameters of the caller.
    - Example of CBV:

    ```c
    #include <stdio.h>

    void swapx(int x, int y);

    int main() {
        int a = 10, b = 20;
        swapx(a, b);
        printf("In the Caller:\n");
        printf("a = %d, b = %d\n", a, b);
        return 0;
    }

    void swapx(int x, int y) {
        int t;
        t = x;
        x = y;
        y = t;
        printf("Inside Function:\n");
        printf("x = %d, y = %d\n", x, y);
    }
    ```

    Output:
    ```
    Inside Function: x = 20, y = 10
    In the Caller: a = 10, b = 20
    ```

2. **Call by Reference (CBR)**:
    - In CBR, the **address** of the actual parameters is passed to the function as the formal parameters.
    - Pointers are used to achieve CBR.
    - Both the actual and formal parameters refer to the **same memory locations**.
    - Changes made inside the function are **reflected** in the actual parameters of the caller.
    - Example of CBR:

    ```c
    #include <stdio.h>

    void swapx(int* x, int* y);

    int main() {
        int a = 10, b = 20;
        swapx(&a, &b);
        printf("Inside the Caller:\n");
        printf("a = %d, b = %d\n", a, b);
        return 0;
    }

    void swapx(int* x, int* y) {
        int t;
        t = *x;
        *x = *y;
        *y = t;
        printf("Inside the Function:\n");
        printf("x = %d, y = %d\n", *x, *y);
    }
    ```

    Output:
    ```
    Inside the Function: x = 20, y = 10
    Inside the Caller: a = 20, b = 10
    ```

3. **Difference Summary**:
    - **Call by Value** passes values as copies, preserving the original data.
    - **Call by Reference** passes references (addresses) to variables, directly modifying the original values¹.
