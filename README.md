# EX-21-POINTERS

## NAME: R . NITHISH AADITIYAA

## REGISTER NO: 25011876 [ 212225040287 ]

# AIM:
Write a C program to convert a 23.65 into 25 using pointer

## ALGORITHM:
1.	Declare a double variable to hold the floating-point number (23.65).
2.	Declare a pointer to double to point to the address of the variable.
3.	Use the pointer to modify the value to 25.0.
4.	Print the modified value.

## PROGRAM:
```
#include<stdio.h>
int main()
{
    float n=23.65;
    float *ptr;
    ptr=&n;
    printf("Modified value: %.0f",*ptr+1);
    return 0;
}
```
## OUTPUT:
 	
<img width="874" height="107" alt="Screenshot 2026-03-26 143433" src="https://github.com/user-attachments/assets/307a7f0c-2841-46d2-b493-16fa17bb795f" />


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
#include<stdio.h>
int natural(int num)
{
    long long static int p=1;
    while(num!=0)
    {
        p*=num;
        return natural(num-1);
    }
    return p;
}
int main()
{
    int n;
    scanf("%d",&n);
    printf("The product of first %d natural numbers = %lld",n,natural(n));
    return 0;
}
```
## OUTPUT:

<img width="872" height="186" alt="Screenshot 2026-03-26 143514" src="https://github.com/user-attachments/assets/4ff8776a-e0db-4e51-bb04-5f06ba0a323b" />


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
 #include<stdio.h>
 int main()
 {
     int n;
     scanf("%d",&n);
     int mat[n][n];
     for(int row=0;row<n;row++)
     {
         for(int col=0;col<n;col++)
         {
             scanf("%d",&mat[row][col]);
         }
     }
     printf("\nThe matrix is:\n");
     for(int row=0;row<n;row++)
     {
         for(int col=0;col<n;col++)
         {
             printf("%d ",mat[row][col]);
         }
         printf("\n");
     }
     printf("\n Sum of elements in first row = ");
     int sum1=0;
     for(int row=0;row<n;row++)
     {
         for(int col=0;col<n;col++)
         {
             if(row==0)
             {
                 sum1+=mat[row][col];
             }
         }
     }
     printf("%d",sum1);
     printf("\n Sum of elements in second row = ");
     int sum2=0;
     for(int row=0;row<n;row++)
     {
         for(int col=0;col<n;col++)
         {
             if(row==1)
             {
                 sum2+=mat[row][col];
             }
         }
     }
     printf("%d",sum2);
     printf("\n Sum of elements in third row = ");
     int sum3=0;
     for(int row=0;row<n;row++)
     {
         for(int col=0;col<n;col++)
         {
             if(row==2)
             {
                 sum3+=mat[row][col];
             }
         }
     }
     printf("%d",sum3);
     return 0;
 }
```
## OUTPUT

<img width="896" height="447" alt="Screenshot 2026-03-26 143620" src="https://github.com/user-attachments/assets/a09f1892-6311-42b2-a43c-1ecfadb3971d" />


## RESULT:
Thus the program has been executed successfully.

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
#include<stdio.h>

int main()
{
    int num, a = 0;
    char ch[20];
    scanf("%[^\n]", ch);
    scanf("%d", &num);
    for(int i = 0; i <= num; i++)
    {
     
        for(int j = 0; j <= num - i; j++)
            printf(" "); 
        for(int k = 0; k <= i; k++)
        {
            printf("%2c", ch[a++]);
           
            if(ch[a] == '\0') a = 0;
        }
        printf("\n"); }
    return 0;
}
```
 ## OUTPUT

<img width="876" height="367" alt="Screenshot 2026-03-26 143830" src="https://github.com/user-attachments/assets/22509266-d240-438a-9211-d5b27160b1fd" />


## RESULT
Thus the C program to String process executed successfully.


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
#include<stdio.h>
int main()
{
    int n;
    scanf("%d",&n);
    int arr[n];
    int *ptr=arr;
    int i;
    for(i=0;i<n;i++)
    {
        scanf("%d",(ptr+i));
    }
    printf("\nNumbers: ");
    for(i=0;i<n;i++)
    {
        printf("%d ",*(ptr+i));
    }
    return 0;
}
```
## OUTPUT

<img width="915" height="257" alt="Screenshot 2026-03-26 144014" src="https://github.com/user-attachments/assets/52f1b81a-169c-4b32-8567-692be419e131" />


## RESULT
Thus the C program to read and display an array of any 6 integer elements using pointer has been executed


