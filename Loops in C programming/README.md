# Different types of loop in C program

## for loop:
   * This loop has a fixed number of iterations, which are specified by an initialization, a test, and an update expression.
   * For example:
     ```
           // print numbers from 1 to 10
      for (int i = 1; i <= 10; i++) {
          printf("%d\n", i);
      }
     ```

## while loop: 
  * This loop repeats as long as the test condition is true. The test condition is checked before each iteration. 
  * For example:
    ```
    // print numbers from 1 to 10
    int i = 1;
    while (i <= 10) {
        printf("%d\n", i);
        i++;
    }
    ```
## do-while loop: 
  * This loop is similar to the while loop, but the test condition is checked after each iteration. This means that the loop body is executed at least once, even if the condition is false.
  * For example:
    ```
    // print numbers from 1 to 10
    int i = 1;
    do {
        printf("%d\n", i);
        i++;
    } while (i <= 10);
    ```   
