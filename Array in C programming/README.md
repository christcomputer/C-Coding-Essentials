# Array

1. An array in C is a collection of elements of the same data type that are stored in contiguous memory locations. 
2. Arrays can have one or more dimensions, and can be initialized with or without specifying the size.

* declare a one-dimensional array of 5 integers
```
int arr[5];
```
* initialize a one-dimensional array with 5 elements
```
int arr[] = {10, 20, 30, 40, 50};
```
* declare and initialize a two-dimensional array of 3 rows and 4 columns
```
int mat[3][4] = {{1, 2, 3, 4},
                 {5, 6, 7, 8},
                 {9, 10, 11, 12}};
```
* access the first element of the array
```
int x = arr[0]; // x = 10
```
* access the element at row 2 and column 3 of the matrix
```
int y = mat[1][2]; // y = 7
```
* loop through the array and print its elements
```
for (int i = 0; i < 5; i++) {
    printf("%d ", arr[i]);
}
// output: 10 20 30 40 50
```
* loop through the matrix and print its elements
```
for (int i = 0; i < 3; i++) {
    for (int j = 0; j < 4; j++) {
        printf("%d ", mat[i][j]);
    }
    printf("\n");
}
// output:
// 1 2 3 4
// 5 6 7 8
// 9 10 11 12
```   
