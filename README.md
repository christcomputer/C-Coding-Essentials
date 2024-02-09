# C Programming

1. **Print Hello World in C**
  
```
#include <stdio.h>
#include <stdlib.h>

int main(void) {
	puts("!!!Hello World!!!"); /* prints !!!Hello World!!! */
	return EXIT_SUCCESS;
}
```
This is a C program that prints `“!!!Hello World!!!”` to the standard output stream. Here is a line-by-line explanation of the code:

 * `#include <stdio.h>`: This is a preprocessor directive that tells the compiler to include the header file `stdio.h`, which contains the declarations of input/output functions such as `printf()` and `puts()`.
 * `#include <stdlib.h>`: This is another preprocessor directive that tells the compiler to include the header file `stdlib.h`, which contains the declaration of the macro `EXIT_SUCCESS`, which represents a successful termination of the program.
 * `int main(void)`: This is the definition of the main function, which is the entry point of the program. The int keyword specifies the return type of the function, which is an integer. The void keyword inside the parentheses indicates that the function takes no arguments.
 * `puts("!!!Hello World!!!");`: This is a function call that prints the string `“!!!Hello World!!!”` followed by a newline character to the standard output stream, which is usually the console or the terminal. The `puts()` function is defined in the `stdio.h` header file.
 * `return EXIT_SUCCESS;`: This is a return statement that ends the execution of the main function and returns the value of EXIT_SUCCESS to the operating system. The `EXIT_SUCCESS` macro is defined in the `stdlib.h` header file and has a value of `0`, which indicates a successful termination of the program

2. **Input a Number and Print the number**

```
#include <stdio.h>
#include <stdlib.h>

int main(void) {
	int a;
	printf("Enter a number");
	fflush( stdout );
		scanf("  %d",&a);
	printf("you have entered %d",a);

	return EXIT_SUCCESS;
}
```    
* `fflush(stdout);`: This is a function call that forces any buffered data in the standard output stream, which is usually the console or the terminal, to be written immediately. The `fflush()` function is defined in the `stdio.h` header file. The stdout macro represents the standard output stream. The purpose of this function is to ensure that the prompt message `"Enter a number"` is displayed before the user enters the input, as some systems may delay the output until a newline character is encountered.

3. **Sum of Two numbers**

```
#include <stdio.h>
#include <stdlib.h>

int main(void) {
	int number1,number2,sum;
	printf("Enter two numbers"); /* prints enter two numbers */
	fflush( stdout );/*for printf to execute before scanf  */
	scanf("%d%d",&number1,&number2);
	sum=number1+number2;
	printf("Result is : %d",sum);

	return EXIT_SUCCESS;
}
```

4. **Average of Three number**

```
#include <stdio.h>
#include <stdlib.h>

int main(void) {
	float num1,num2,num3,avg;
	printf("Enter three number");
	fflush( stdout );
	scanf("%f%f%f",&num1,&num2,&num3);
	avg=(num1+num2+num3)/3;
	printf("average of 3 number is :%f",avg);
	return EXIT_SUCCESS;
}
```   

5. **Swapping With Temporary Variable**

```
#include <stdio.h>
#include <stdlib.h>

int main(void) {
	int a=10,b=21,temp;

	temp=a;
	a=b;
	b=temp;

	printf("a:%d  b:%d",a,b);
	return EXIT_SUCCESS;
}
```

6. **Swapping Without Temporary Variable**

```
#include <stdio.h>
#include <stdlib.h>

int main(void) {
	int a=12,b=23;
	a=a+b;
	b=a-b;
	a=a-b;
	printf("a:%d  b:%d",a,b);
	return EXIT_SUCCESS;
}
```
   
7. **Input and Print Your name**

```
#include <stdio.h>
#include <stdlib.h>

int main(void) {
	char name;
	printf("Enter your name: ");
	fflush( stdout );
	scanf("%c",&name);
	printf("Your name is:%c",name);
	return EXIT_SUCCESS;
}
```     

8. **Sum of Two number with setbuf**

```
#include <stdio.h>
#include <stdlib.h>

int main(void) {
	int number1;
	float number2;
	float sum;
	setbuf(stdout,NULL);
	printf("Enter two numbers: ");
	scanf("%d%f",&number1,&number2);
	sum=number1+number2;
	printf("sum is:%f",sum);
	return EXIT_SUCCESS;
}
```
* `setbuf(stdout,NULL);`: This is a function call that disables the buffering of the standard output stream, which is usually the console or the terminal. The `setbuf()` function is defined in the `stdio.h` header file. The stdout macro represents the standard output stream. The `NULL` macro represents a null pointer, which indicates no buffer is used. The purpose of this function is to ensure that the output is displayed immediately, without waiting for a newline character or a buffer flush .

9. **Find Simple Interest**

```
#include <stdio.h>
#include <stdlib.h>

int main(void) {
	int P;
	float R,n,SI;
	setbuf(stdout,NULL);
	printf("Enter the Principal Amount: ");
	scanf("%d",&P);
	printf("Enter the interest: ");
	scanf("%f",&R);
	printf("Enter number of year of loan: ");
	scanf("%f", &n);
	SI=(P*R*n/100);

	printf("simple interest is:%f",SI); 
	return EXIT_SUCCESS;
}
```      

10. **Find a number Positive or Negative**

```
#include <stdio.h>
#include <stdlib.h>

int main(void) {
	int num;
	setbuf(stdout,NULL);
	printf("Enter a number");
	scanf("%d",&num);
	if(num<0){
		printf("number is negative");
	}else{
		printf("number is positive");
	}

	return EXIT_SUCCESS;
}
```

11. **Find Greatest of Two numbers**

```
#include <stdio.h>
#include <stdlib.h>

int main(void) {
	int num;
	setbuf(stdout,NULL);
	printf("Enter a number");
	scanf("%d",&num);
	if(num<0){
		printf("number is negative");
	}else{
		printf("number is positive");
	}

	return EXIT_SUCCESS;
}
```

  * Syntax of if else:
	```
	if (condition) {
	    // code to be executed if the condition is true
	}else {
  	    // code to be executed if the condition is false	
  	}
	```
12. **Largest of Two Number**

```
#include <stdio.h>
#include <stdlib.h>

int main(void) {
	int num1,num2;
	setbuf(stdout,NULL);
	printf("Enter two number:");
	scanf("%d%d",&num1,&num2);
	if(num1>num2){
		printf("Greatest number is %d",num1);
	}else{
		printf("Greatest number is %d",num2);
	}

	return EXIT_SUCCESS;
}
```

13. **Largest of Three Numbers**

```
#include <stdio.h>
#include <stdlib.h>

int main(void) {
	int num1,num2,num3;
	setbuf(stdout,NULL);
	printf("Enter three numbers");
	scanf("%d%d%d",&num1,&num2,&num3);
	if(num1>num2){
		if(num1>num3){
			printf("greatest number is %d",num1);

		}
	}else{
		if(num2>num3){
			printf("greatest number is %d",num2);
		}else{
			printf("greatest number is %d",num3);
		}
	}

	return EXIT_SUCCESS;
}
```

14. **Basic Calculator**

```
#include <stdio.h>
#include <stdlib.h>

int main(void) {
	int num1,num2,choice,result;
	setbuf(stdout,NULL);
	printf("Enter two number");
	scanf("%d%d",&num1,&num2);
	printf("1 for Addition\n2 for Subtraction\n3 for multiplication\n4 for Division\nenter your choice");
	scanf("%d",&choice);
	if(choice==1){
		result=num1+num2;
		printf("Result is= %d",result);
	}else if(choice==2){
		result=num1-num2;
		printf("Result is= %d",result);
	}else if(choice==3){
		result=num1*num2;
		printf("Result is= %d",result);
	}else if(choice==4){
		result=num1/num2;
		printf("Result is= %d",result);
	}else{
		printf("fool!!!!");
	}

	return EXIT_SUCCESS;
}
```

15. **Switch Sample**

```
#include <stdio.h>
#include <stdlib.h>

int main(void) {
	int choice;
	setbuf(stdout,NULL);
	printf("1 for Biriyani\n2 for Porota\n3 for fried rice\n4 for appam\nEnter your choice");
	scanf("%d",&choice);
	switch(choice){
	case 1:
		printf("you have selected Biriyani");
		break;
	case 2:
		printf("you have selected Porota");
		break;
	case 3:
		printf("you have selected fried rice");
		break;
	case 4:
		printf("you have selected appam");
		break;
	default:
		printf("fool");
	}
	return EXIT_SUCCESS;
}
```
 * Switch Syntax:
	```
	switch (expression) {
	    case value1:
	        // statements for value1
	        break; // optional
	    case value2:
	        // statements for value2
	        break; // optional
	    // more cases can be added
	    default:
	        // statements for default case
	        break; // optional
	}
	```
 	* The expression is evaluated once and compared with the values of each case label. If there is a match, the corresponding statements are executed. If there is no match, the default statements are executed if present.
  	* The break statement is used to terminate the switch block and jump to the next line after the switch statement. The break statement is optional, but if omitted, the execution will continue to the next case

16. **Pass or Fail**

```
#include <stdio.h>
#include <stdlib.h>

int main(void) {
	float mark;
	setbuf(stdout,NULL);
	printf("Enter your mark");
	scanf("%f",&mark);
	if(mark<50){
		printf("failed");

	}else if(mark<=100){
		printf("passed");
	}else{
		printf("enter correctly");
	}
	return EXIT_SUCCESS;
}
```

17. **Student Grade**

```
#include <stdio.h>
#include <stdlib.h>

int main(void) {
	float mark;
	setbuf(stdout,NULL);
	printf("Enter your mark percentage: ");
	scanf("%f",&mark);
	if(mark<=0||mark>100){
		printf("Please Enter correctly");
	}else if(mark>=90){
		printf("your grade is A");
	}else if(mark>=80){
		printf("your grade is B");
	}else if(mark>=70){
		printf("your grade is C");
	}else if(mark>=60){
		printf("your grade is D");
	}else if(mark>=50){
		printf("your grade is E");
	}else{
		printf("Failed");
	}
	return EXIT_SUCCESS;
}
```    

18. **Find Week**
    
```
#include <stdio.h>
#include <stdlib.h>

int main(void) {
	int day;
	setbuf(stdout,NULL);
	printf("Enter the day from 1 - 7: ");
	scanf("%d",&day);
	switch(day){
	case 1:
		printf("Day %d of the week is Sunday",day);
		break;
	case 2:
		printf("Day %d of the week is Monday",day);
		break;
	case 3:
		printf("Day %d of the week is Tuesday",day);
		break;
	case 4:
		printf("Day %d of the week is Wednesday",day);
		break;
	case 5:
		printf("Day %d of the week is Thursday",day);
		break;
	case 6:
		printf("Day %d of the week is Friday",day);
		break;
	case 7:
		printf("Day %d of the week is Saturday",day);
		break;
	default:
		printf("Invalid Entry");
	}
	return EXIT_SUCCESS;
}
```

19. **Post / Pre Increment / Decrement**

```
#include <stdio.h>
#include <stdlib.h>

int main(void) {
	int a,b,choice;
	setbuf(stdout,NULL);
	printf("Enter a number: ");
	scanf("%d",&a);
	printf("1 for Post increment b=a++\n2 for Pre increment b=++a\n3 for Post Decrement b=a--\n4 for Pre Decrement b=--a\nEnter your Choice");
	scanf("%d",&choice);
	switch(choice){
	case 1:
		b=a++;
		printf("After Post increment value in b= %d and value in a= %d",b,a);
		break;
	case 2:
		b=++a;
		printf("After Pre increment value in b= %d and value in a= %d",b,a);
		break;
	case 3:
		b=a--;
		printf("After Post Decrement value in b= %d and value in a= %d",b,a);
		break;
	case 4:
		b=--a;
		printf("After Pre Decrement value in b= %d and value in a= %d",b,a);
		break;
	default:
		printf("Invalid entry");

	}
	return EXIT_SUCCESS;
}
```

## for loop

20. **For Loop**

```
#include <stdio.h>
#include <stdlib.h>

int main(void) {
	int i;
	for(i=1;i<=100;i++){
		printf("%d\n",i);
	}

	return EXIT_SUCCESS;
}
```
 * For loop Syntax:
	```
	for (initialization; condition; update) {
	    // statements to be executed
	}
	```
	* The initialization is where the loop control variable is declared and assigned an initial value.
 	* The condition is a logical expression that determines whether the loop should continue or not.
 	* The update is where the loop control variable is modified after each iteration.
  	* The statements inside the loop body are executed as long as the condition is true.

21. **Sum of n numbers**

```
#include <stdio.h>
#include <stdlib.h>

int main(void) {
	int i,sum=0,number;
	setbuf(stdout,NULL);
	printf("Enter a number");
	scanf("%d",&number);
	for(i=1;i<=number;i++){
		sum=sum+i;

	}
	printf("result is: %d",sum);
	return EXIT_SUCCESS;
}
```

22. **Print even numbers**

```
#include <stdio.h>
#include <stdlib.h>

int main(void) {
	int i,limit;
	setbuf(stdout,NULL);
	printf("Enter limit of even number to be printed: ");
	scanf("%d",&limit);
	for(i=2;i<=limit;i++){
		if(i%2==0){
			printf("%d\n",i);
		}
	}
	return EXIT_SUCCESS;
}
```

23. **Prime numbers**

```
#include <stdio.h>
#include <stdlib.h>

int main(void) {
	int i,flag=0,number;
	setbuf(stdout,NULL);
	printf("Enter a number: ");
	scanf("%d",&number);
	for(i=2;i<=number/2;i++){
		if(number%i==0){
			flag=1;
			break;
		}
	}
	if(flag==0){
		printf("%d is prime number",number);

	}else{
		printf("%d is not prime number",number);
	}
	return EXIT_SUCCESS;
}
```

24. **Print Star Pattern**

```
#include <stdio.h>
#include <stdlib.h>

int main(void) {
	int limit,i,j;
	setbuf(stdout,NULL);
	printf("Enter the limit: ");
	scanf("%d",&limit);
	for(i=1;i<=limit;i++){
		for(j=0;j<i;j++){
			printf("* ");
		}
		printf("\n");
	}


	return EXIT_SUCCESS;
}
```

25. **Reverse Pyramid star**

```
#include <stdio.h>
#include <stdlib.h>

int main(void) {
	int i,j,limit;
	setbuf(stdout,NULL);
	printf("Enter the limit: ");
	scanf("%d",&limit);
	for(i=limit;i>=1;i--){
		for(j=0;j<i;j++){
			printf("* ");

		}
		printf("\n");

	}

	return EXIT_SUCCESS;
}
```

26. **Multiplication Table**

```
#include <stdio.h>
#include <stdlib.h>

int main(void) {
	int i,number,result=0;
	setbuf(stdout,NULL);
	printf("Enter a number: ");
	scanf("%d",&number);
	for(i=1;i<=10;i++){
		result=i*number;
		printf("%d * %d = %d \n",i,number,result);
	}
	return EXIT_SUCCESS;
}
```

27. **`break` and `continue` in C**

```
#include <stdio.h>
#include <stdlib.h>

int main(void) {
	int i,choice,n=10;
	setbuf(stdout,NULL);
	printf("1 for break\n2 for switch\nEnter your choice: ");
	scanf("%d",&choice);

	if(choice==1){

	for(i=1;i<=n;i++){
		printf("Hi ");
		if(i==5){
			break;
		}
		printf("Hello\n");
	}
	printf("\nfinished");



	}else if(choice==2){

		for(i=1;i<=n;i++){
			printf("Hi ");
			if(i==5){
				printf("\n");
				continue;
			}
			printf("Hello\n");
		}
		printf("finished");
	}

	return EXIT_SUCCESS;
}
```

28. **Sum of odd number**

```
#include <stdio.h>
#include <stdlib.h>

int main(void) {
	int i,limit,sum=0;
	setbuf(stdout,NULL);
	printf("Enter the limit: ");
	scanf("%d",&limit);
	for(i=1;i<=limit;i=i+2){
		sum=sum+i;
	}
	printf("sum of odd numbers= %d",sum);
	return EXIT_SUCCESS;
}
```

29. **Nested Loop**

```
#include <stdio.h>
#include <stdlib.h>

int main(void) {
	int i,j,num;
	setbuf(stdout,NULL);
	printf("Enter the row of pattern: ");
	scanf("%d",&num);
	for(i=1;i<=num;i++){
		for(j=1;j<=i;j++){
			printf("%d ",j);
		}
		printf("\n");
	}
	return EXIT_SUCCESS;
}
```

## Array

30. **Array Input and Output that array**

```
#include <stdio.h>
#include <stdlib.h>

int main(void) {
	int a[100];
	int i,limit;
	setbuf(stdout,NULL);
	printf("Enter array limit");
	scanf("%d",&limit);
	printf("Enter values: ");
	for(i=0;i<limit;i++){
		scanf("%d",&a[i]);

	}
	printf("Entered values are: ");
	for(i=0;i<limit;i++){
		printf("%d\t", a[i]);
	}
	return EXIT_SUCCESS;
}
```

31. **Sum of Array**

```
#include <stdio.h>
#include <stdlib.h>

int main(void) {
	int values[100];
	int sum=0,i,limit;
	setbuf(stdout,NULL);
	printf("Enter the limit: ");
	scanf("%d",&limit);
	printf("Enter the values: ");
	for(i=0;i<limit;i++){
		scanf("%d",&values[i]);

	}
	for(i=0;i<limit;i++){
		sum=sum+values[i];
	}
	printf("sum is= %d",sum);
	return EXIT_SUCCESS;
}
```

32. **Array Search**

```
#include <stdio.h>
#include <stdlib.h>

int main(void) {
	int values[100];
	int i,searchkey,limit,flag=0;
	setbuf(stdout,NULL);
	printf("Enter the limit: ");
	scanf("%d",&limit);

	printf("Enter the values: ");
	for(i=0;i<limit;i++){
		scanf("%d",&values[i]);
	}
	printf("Enter the Search key: ");
	scanf("%d",&searchkey);
	for(i=0;i<limit;i++){
		if(searchkey==values[i]){
		    flag=1;
			break;
		}

	}
	if(flag==1){
		printf("value is found at %d position",i+1);

	}else{
		printf("value not found");
	}

	return EXIT_SUCCESS;
}
```

33. **Array Selection sort**

```
#include <stdio.h>
#include <stdlib.h>

int main(void) {
	int i,j,values[100],limit,temp;
	setbuf(stdout,NULL);
	printf("Enter the limit: ");
	scanf("%d",&limit);

	printf("Enter the numbers for sort: ");
	for(i=0;i<limit;i++){
		scanf("%d",&values[i]);
	}
	for(i=0;i<limit-1;i++){
		for(j=i+1;j<limit;j++){
			if(values[i]>values[j]){
				temp=values[i];
				values[i]=values[j];
				values[j]=temp;
			}
		}
	}
	printf("sorted values are: ");
	for(i=0;i<limit;i++){
		printf("%d\t",values[i]);
	}
	return EXIT_SUCCESS;
}
```      

34. **Interchange Value of two Array**

```
#include <stdio.h>
#include <stdlib.h>

int main(void) {
	int i,limit,First[100],Second[100];
	setbuf(stdout,NULL);
	printf("Enter the size of Array: ");
	scanf("%d",&limit);

	printf("Enter the Values of Array 1: ");
	for(i=0;i<limit;i++){
		scanf("%d",&First[i]);
	}

	printf("Enter the Values of Array 2: ");
	for(i=0;i<limit;i++){
		scanf("%d",&Second[i]);
	}
	for(i=0;i<limit;i++){
		First[i]=First[i]+Second[i];
		Second[i]=First[i]-Second[i];
		First[i]=First[i]-Second[i];
	}
	printf("Arrays after swapping: ");

	printf("\nArray1: ");
	for(i=0;i<limit;i++){
		printf("%d\t",First[i]);
	}
	printf("\nArray2: ");
	for(i=0;i<limit;i++){
		printf("%d\t",Second[i]);
	}
	return EXIT_SUCCESS;
}
```

35. **No. of Even number in an Array**

```
#include <stdio.h>
#include <stdlib.h>

int main(void) {
	int i,limit,values[100],count=0;
	setbuf(stdout,NULL);
	printf("Enter the size of an array: ");
	scanf("%d",&limit);

	printf("Enter the values of array: ");
	for(i=0;i<limit;i++){
		scanf("%d",&values[i]);
	}
	for(i=0;i<limit;i++){
		if(values[i]%2==0){
			count=count+1;
		}
	}
	printf("Number of even numbers in the given array is %d",count);
	return EXIT_SUCCESS;
}
```

36. **Sort Array in Descending Order**

```
#include <stdio.h>
#include <stdlib.h>

int main(void) {
	int i,j,values[100],limit,temp;
	setbuf(stdout,NULL);

	printf("Enter the limit: ");
	scanf("%d",&limit);

	printf("Enter the values of array: ");
	for(i=0;i<limit;i++){
		scanf("%d",&values[i]);
	}
	for(i=0;i<limit-1;i++){
		for(j=i+1;j<limit;j++){
			if(values[i]<values[j]){
				temp=values[i];
				values[i]=values[j];
				values[j]=temp;
			}
		}
	}
	printf("Sorted array: ");
	for(i=0;i<limit;i++){
		printf("%d\t",values[i]);
	}
	return EXIT_SUCCESS;
}
```

37. **MultiDimensional Array**

```
#include <stdio.h>
#include <stdlib.h>

int main(void) {
	int i,j,values[3][3];
	setbuf(stdout,NULL);
	printf("Enter the values: ");
	for(i=0;i<3;i++){
		for(j=0;j<3;j++){
			scanf("%d",&values[i][j]);
		}
	}
	printf("Entered values are: \n");
	for(i=0;i<3;i++){
		for(j=0;j<3;j++){
			printf("%d\t",values[i][j]);
		}
		printf("\n");
	}
	return EXIT_SUCCESS;
}
```

## Function in C

38. **Function without argument and no return value**

```
#include <stdio.h>
#include <stdlib.h>

void sum();
int main(void) {
	sum();

	return EXIT_SUCCESS;
}
void sum(){
	int num1,num2,sum;
	setbuf(stdout,NULL);
	printf("Enter two numbers: ");
	scanf("%d%d",&num1,&num2);
	sum=num1+num2;
	printf("Sum is %d",sum);
}
```

39. **Function with argument and no return value**

```
#include <stdio.h>
#include <stdlib.h>

void sum(int,int);
int main(void) {
	int a,b;
	setbuf(stdout,NULL);
	printf("Enter two numbers: ");
	scanf("%d%d",&a,&b);
	sum(a,b);
	return EXIT_SUCCESS;
}
void sum(int num1,int num2){
	int b;
	b=num1+num2;
	printf("Sum is %d",b);
}
```

40. **Function with argument and with return value**

```
#include <stdio.h>
#include <stdlib.h>

void sum(int,int);
int main(void) {
	int a,b;
	setbuf(stdout,NULL);
	printf("Enter two numbers: ");
	scanf("%d%d",&a,&b);
	sum(a,b);
	return EXIT_SUCCESS;
}
void sum(int num1,int num2){
	int b;
	b=num1+num2;
	printf("Sum is %d",b);
}
```

41. **Function without argument and with return value**

```
#include <stdio.h>
#include <stdlib.h>

int sum();
int main(void) {
	int c;
	c=sum();
	printf("Sum is %d",c);

	return EXIT_SUCCESS;
}
int sum(){
	int a,b,result;
	setbuf(stdout,NULL);
	printf("Enter two values: ");
	scanf("%d%d",&a,&b);
	result=a+b;
	return result;
}
```

42. **String Palindrome**

```
#include <stdio.h>
#include <stdlib.h>
#include <string.h>

int main(void) {
	int i,length,flag=0;
	char str[20];
	setbuf(stdout,NULL);
	printf("Enter a string: ");
	scanf("%s",str);
	length=strlen(str);


	for(i=0;i<length;i++){
		if(str[i]!=str[length-i-1]){
			flag=1;
			break;
		}
	}
	if(flag==0){
		printf("%s is a palindrome",str);
	}else{
		printf("%s is not a palindrome",str);
	}
	return EXIT_SUCCESS;
}
```

43. **Add 2D Arrays**

```
#include <stdio.h>
#include <stdlib.h>

int main(void) {
	int i,j,n,Array1[10][10],Array2[10][10],sum[10][10];
	setbuf(stdout,NULL);
	printf("Enter the size of arrays");
	scanf("%d",&n);
	printf("Enter the values of array 1: \n");
	for(i=0;i<n;i++){
		for(j=0;j<n;j++){
			scanf("%d",&Array1[i][j]);
		}

	}
	printf("Enter the values of array 2: \n");
	for(i=0;i<n;i++){
		for(j=0;j<n;j++){
			scanf("%d",&Array2[i][j]);
		}

	}
	for(i=0;i<n;i++){
		for(j=0;j<n;j++){
			sum[i][j]=Array1[i][j]+Array2[i][j];
		}

	}
	printf("Sum of 2 arrays is: \n");
	for(i=0;i<n;i++){
		for(j=0;j<n;j++){
			printf("%d\t",sum[i][j]);
		}
		printf("\n");
	}

	return EXIT_SUCCESS;
}
```

44. **Array Display using function**

```
#include <stdio.h>
#include <stdlib.h>

void getArray(int);
void displayArray(int);

int main(void) {
	setbuf(stdout,NULL);
	int limit;
	printf("Enter the size of the array: ");
	scanf("%d",&limit);
	getArray(limit);
	displayArray(limit);

	return EXIT_SUCCESS;
}
void getArray(int limit1){
	int array1[20],i;
	printf("Enter values to the array:  ");
	for(i=0;i<limit1;i++){
		scanf("%d",&array1[i]);
	}


}
void displayArray(int limit2){
	int array2[20],i;
	printf("Array is: \n");
	for(i=0;i<limit2;i++){
		printf("%d\t",array2[i]);
	}

}
```   
