# EX-11-EMI-CALCULATOR

## AIM

To write a program to prepare EMI calculator using function without return type and with arguments.

## ALGORITHM

1.	Start the program.
2.	Read principal amount, rate of interest and months.
3.	Pass these values as arguments to function.
4.	Calculate EMI using the formula, amt=(prpow(1+r,t))/(pow(1+r,t)-1)
5.	Display the result.
6.	Stop the program.

## PROGRAM
#include <stdio.h>
#include <math.h>

// Step 3: Function to calculate EMI
double calculateEMI(double principal, double rate, int months) {
    double r = rate / (12 * 100);  // Convert annual rate (%) to monthly decimal rate
    double numerator = principal * r * pow(1 + r, months);
    double denominator = pow(1 + r, months) - 1;
    return numerator / denominator;
}

int main() {
    // Step 2: Declare variables and read input
    double principal, rate;
    int months;

    printf("Enter principal amount: ");
    scanf("%lf", &principal);

    printf("Enter annual rate of interest (in %%): ");
    scanf("%lf", &rate);

    printf("Enter number of months: ");
    scanf("%d", &months);

    // Step 4: Calculate EMI by calling the function
    double emi = calculateEMI(principal, rate, months);

    // Step 5: Display the result
    printf("EMI amount: %.2lf\n", emi);

    // Step 6: End program
    return 0;
}


## OUTPUT
Enter principal amount: 100000
Enter annual rate of interest (in %): 10
Enter number of months: 12
EMI amount: 8791.59





## RESULT

Thus the program to prepare EMI calculator using function without return type with arguments has been executed successfully
 
 


# EX-12-FIBONACCI-SERIES
## AIM
To write a C program to generate the Fibonacci series for the value 6.

## ALGORITHM
1.	Start the program.
2.	Read number of terms to display.
3.	Add the previous two terms and store it in new term.
4.	Assign 2nd term to 1st term and 3rd term to 2nd term.
5.	Repeat steps 3 and 4 n number of times.
6.	Display the result.
7.	Stop the program.

## PROGRAM
#include <stdio.h>

int main() {
    int n, i;
    int t1 = 0, t2 = 1, nextTerm;

    // Step 2: Read number of terms
    printf("Enter the number of terms: ");
    scanf("%d", &n);

    printf("Fibonacci Series: ");

    for (i = 1; i <= n; i++) {
        // Step 6: Display the current term
        printf("%d ", t1);

        // Step 3: Calculate next term
        nextTerm = t1 + t2;

        // Step 4: Update terms
        t1 = t2;
        t2 = nextTerm;
    }

    printf("\n");

    // Step 7: End program
    return 0;
}

## OUTPUT
Enter the number of terms: 7
Fibonacci Series: 0 1 1 2 3 5 8 








## RESULT
Thus the program to generate the Fibonacci series for the value 6 has been executed successfully.
 
 


# EX-13-ONE-DIMENSIONAL-ARRAY
## AIM
To write a C program to read n elements as input and print the last element of the array.

## ALGORITHM
1.	Start the program.
2.	Read a variable.
3.	Read the array values n number of times.
4.	Print the last element.
5.	Stop the program.

## PROGRAM

## OUTPUT









## RESULT
Thus the program to read n elements as input and print the last element of the array has been executed successfully.
 
 


# EX-14-POSITIVE-ARRAY-ELEMENTS
## AIM
To write a C Program to count total number of positive elements in an array.

## ALGORITHM
1.	Start the program.
2.	Read a variable.
3.	Read the array values n number of times.
4.	If the array value can be divided by 2 then increment count by 1.
5.	Display result.
6.	Stop the program.

## PROGRAM
#include <stdio.h>

int main() {
    int n, count = 0;

    // Step 2 & 3: Read number of elements and array values
    printf("Enter the number of elements: ");
    scanf("%d", &n);

    int arr[n];  // Variable length array

    printf("Enter %d integers:\n", n);
    for (int i = 0; i < n; i++) {
        scanf("%d", &arr[i]);
    }

    // Step 4: Count numbers divisible by 2
    for (int i = 0; i < n; i++) {
        if (arr[i] % 2 == 0) {
            count++;
        }
    }

    // Step 5: Display result
    printf("Count of numbers divisible by 2: %d\n", count);

    // Step 6: End program
    return 0;
}


## OUTPUT
Enter the number of elements: 5
Enter 5 integers:
1 2 3 4 5
Count of numbers divisible by 2: 2





## RESULT
Thus the program to count total number of positive elements in an array has been executed successfully.





 
 


# EX -15 - Replace All Even Elements With 'E' In One Dimensional Array

## Aim:
To write a C program to replace all even elements with 'E' in one dimensional array

## Algorithm:
1.	Input the array:
  Read the size of the array.
  Input the elements of the array.
2.	Iterate through the array:
 	For each element of the array, check if the element is even (i.e., if the element modulo 2 equals 0).
3.	Replace even elements with 'E':
     If an element is even, replace that element with the character 'E'.
4.	Output the updated array:
 Print the updated array after replacements.

## Program:
#include <stdio.h>

int main() {
    int n;

    // Step 1: Read the size of the array
    printf("Enter the size of the array: ");
    scanf("%d", &n);

    // Use a char array to store both numbers and 'E' characters after replacement
    // We'll store digits as characters for consistency.
    char arr[n];

    // Step 1: Input elements (as integers first)
    printf("Enter %d integers:\n", n);
    for (int i = 0; i < n; i++) {
        int temp;
        scanf("%d", &temp);

        // Step 3: Replace even elements with 'E', else store digit as char
        if (temp % 2 == 0) {
            arr[i] = 'E';
        } else {
            // Convert digit to char, assuming single-digit input
            // If multiple-digit numbers can be input, we need a different approach.
            arr[i] = (char)(temp + '0');
        }
    }

    // Step 4: Output the updated array
    printf("Updated array: ");
    for (int i = 0; i < n; i++) {
        printf("%c ", arr[i]);
    }
    printf("\n");

    return 0;
}

## Output:
 
Enter the size of the array: 7
Enter 7 integers:
3 4 7 8 9 2 5
Updated array: 3 E 7 E 9 E 5 


## Result:

Thus, the program to replace all even elements with 'E' in one dimensional array was verified successfully.



