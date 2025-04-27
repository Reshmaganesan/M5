EX-21-POINTERS
# AIM:
Write a C program to convert a 23.65 into 25 using pointer

## ALGORITHM:
1.	Declare a double variable to hold the floating-point number (23.65).
2.	Declare a pointer to double to point to the address of the variable.
3.	Use the pointer to modify the value to 25.0.
4.	Print the modified value.

## PROGRAM:
```
#include <stdio.h>

int main() {
    float num = 23.65;  // Initial value
    float *ptr = &num;  // Pointer to the variable num
    
    printf("Original value: %.2f\n", *ptr);  // Print the original value using the pointer
    
    // Modify the value through the pointer
    *ptr = 25.0;

    printf("Modified value: %.2f\n", *ptr);  // Print the modified value using the pointer
    
    return 0;
}
```
## OUTPUT:
 ![image](https://github.com/user-attachments/assets/023d852f-eefa-46c7-bad8-417a79be4060)
	











## RESULT:
Thus the program to convert a 23.65 into 25 using pointer has been executed successfully.
 
 


# EX-22-FUNCTIONS AND STORAGE CLASS

## AIM:

Write a C program to calculate the Product of first 12 natural numbers using Recursion

## ALGORITHM:

1.	Define a recursive function calculateProduct that takes an integer parameter n.
2.	Return n multiplied by the result of the calculateProduct function called with n - 1.
3.	Declare an integer variable n and an unsigned long long variable product.
4.	Initialize n with the value 12 (for the first 12 natural numbers).
5.	Call the calculateProduct function with n and store the result in the product variable.
6.	Print the result, indicating it is the product of the first 12 natural numbers.

## PROGRAM:
```
#include <stdio.h>

// Recursive function to calculate the product of first n natural numbers
long long product(int n) {
    if (n == 1) {
        return 1; // Base case: product of 1 is 1
    }
    return n * product(n - 1); // Recursive case
}

int main() {
    int n = 12;  // First 12 natural numbers
    long long result = product(n); // Calculate the product using recursion
    
    printf("The product of the first %d natural numbers is: %lld\n", n, result);
    return 0;
}
```
## OUTPUT:
![image](https://github.com/user-attachments/assets/9a3f783d-d942-4f33-ad60-eb891d6a1e4d)
         		
## RESULT:

Thus the program has been executed successfully.
 
 


# EX-23-ARRAYS AND ITS OPERATIONS

## AIM:

Write C Program to find Sum of each row of a Matrix

## ALGORITHM:

1.	Declare and initialize the matrix with the desired values.
2.	Create a loop to iterate through each row of the matrix.
3.	Inside the loop, calculate the sum of the elements in each row.
4.	Print the sum for each row.

## PROGRAM:
```
#include <stdio.h>

int main() {
    int rows, cols;
    
    
    scanf("%d", &rows);
   
    scanf("%d", &cols);
    
    int matrix[rows][cols];
    
    
    printf("Enter the elements of the matrix:\n");
    for (int i = 0; i < rows; i++) {
        for (int j = 0; j < cols; j++) {
            printf("Enter element at [%d][%d]: ", i + 1, j + 1);
            scanf("%d", &matrix[i][j]);
        }
    }
    
  
    printf("\nSum of each row:\n");
    for (int i = 0; i < rows; i++) {
        int rowSum = 0;
        for (int j = 0; j < cols; j++) {
            rowSum += matrix[i][j]; 
        }
        printf("Sum of row %d: %d\n", i + 1, rowSum);
    }

    return 0;
}
```


## OUTPUT

![image](https://github.com/user-attachments/assets/d50b3541-fc59-4309-80b5-d3eb97054646)

 
 

 ## RESULT
 


# EX-24-STRINGS

## AIM:

Write C program for the below pyramid string pattern. Enter a string: PROGRAM Enter number of rows: 5 P R O G R A M P R O G R A M P R O G R A M

## ALGORITHM:

1.	Input the number of rows for the pyramid (e.g., num_rows).
2.	Initialize variables:i for the row count (starting from 1),j for the character count (starting from 1)
3.	Start a loop for i from 1 to num_rows (for each row of the pyramid).
4.	Calculate the midpoint position as midpoint = (2 * num_rows - 1) / 2.
5.	End the program.

## PROGRAM:
```
#include <stdio.h>
#include <string.h>

int main() {
    char str[100];
    int rows;
   
    scanf("%s", str);
    
   
    scanf("%d", &rows);
    
    int len = strlen(str);  
    for (int i = 1; i <= rows; i++) {
       
        for (int j = 1; j <= rows - i; j++) {
            printf(" ");
        }
        
        
        for (int j = 1; j <= i; j++) {
            printf("%c ", str[(j - 1) % len]); 
        }
        
       
        printf("\n");
    }

    return 0;
}
```

 ## OUTPUT

 ![image](https://github.com/user-attachments/assets/b4b83bcb-969b-4e89-981e-0e58e92b96f8)


## RESULT

Thus the C program to String process executed successfully
 

 
.



# EX -25 –DISPLAYING ARRAYS USING POINTERS
## AIM

Write a c program to read and display an array of any 6 integer elements using pointer

## ALGORITHM
Step 1: Start the program.
Step 2: Declare the following:
•	Integer variable i for iteration.
•	Integer variable n to store the number of elements.
•	Integer array arr[10] to hold up to 10 elements.
•	Integer pointer parr and initialize it to point to the array arr.
Step 3: Read the value of n (number of elements) from the user.
Step 4: Loop from i = 0 to i < n:
•	Read an integer value and store it in the address parr + i using pointer arithmetic.
Step 5: Loop from i = 0 to i < n:
•	Print the element at *(parr + i) using pointer dereferencing.
Step 6: End the program.

## PROGRAM
```
#include <stdio.h>

int main() {
    int arr[6];         
    int *ptr = arr;     
    
    
    printf("Enter 6 integers:\n");
    for (int i = 0; i < 6; i++) {
        printf("Enter element %d: ", i + 1);
        scanf("%d", ptr + i);  
    }
    
  
    printf("\nThe elements of the array are:\n");
    for (int i = 0; i < 6; i++) {
        printf("Element %d: %d\n", i + 1, *(ptr + i));  // 
    }

    return 0;
}
```
## OUTPUT

 ![image](https://github.com/user-attachments/assets/fc0efe68-fb0e-4904-b91e-a2fba7db2d3b)


## RESULT

Thus the C program to read and display an array of any 6 integer elements using pointer has been executed


