# 19AI304-Fundamentals-of-C-Programming-2025-Odd-M4
# IAPR-4- Module 4 - FoC
## 7. Implementation of Functions.
## 8. Implementation of passing parameters.
# Ex.No:16
  Implement a C program to read a date in the format DD/MM/YYYY and determine whether the entered date is valid. The program should check the correctness of the day, month, and year, including leap year calculations for February.
# Date : 
# Aim:
 To implement a C program that validates a user-entered date using a function without parameters and without return value, ensuring the correctness of day, month, year, and leap year conditions.
# Algorithm:
### Step 1:
  Start
### Step 2: 
  Include the standard input-output library: #include<stdio.h>.
### Step 3:
### Call the function `validateDate()`.
### Inside `validateDate()` function:
### Step 4: 
  Declare variables `dd`, `mm`, and `yy`.
### Step 5: 
  Ask the user to enter a date in `DD/MM/YYYY` format.
### Step 6: 
  Read the date values using `scanf`.
### Step 7: 
  Check if the year is between **1900 and 9999**.
 - If the year is invalid, display **"Year is not valid"** and stop further checks.
### Step 8: 
  Check if the month is between **1 and 12**.
- If the month is invalid, display **"Month is not valid"** and stop further checks.
### Step 9: 
  If the month has **31 days**, check if the day is between **1 and 31**.
### Step 10: 
  If the month has **30 days**, check if the day is between **1 and 30**.
### Step 11: 
  If the month is **February**:
  - Check if the day is between **1 and 28**, or if the day is **29**, verify if it's a **leap year**.
### Step 12: 
  If any valid condition is satisfied, display **"Date is valid."**
### Step 13: 
  Otherwise, display **"Date is invalid."**
### Step 14: 
  Stop
# Program:
#include <stdio.h>

int main() {
    int d, m, y;
    int daysInMonth;

    printf("Enter date (DD/MM/YYYY): ");
    scanf("%d/%d/%d", &d, &m, &y);

    // Check valid year
    if (y <= 0) {
        printf("Invalid Date\n");
        return 0;
    }

    // Check valid month
    if (m < 1 || m > 12) {
        printf("Invalid Date\n");
        return 0;
    }

    // Days in each month
    if (m == 2) {
        // Leap year check
        if ((y % 400 == 0) || (y % 4 == 0 && y % 100 != 0))
            daysInMonth = 29;
        else
            daysInMonth = 28;
    }
    else if (m == 4 || m == 6 || m == 9 || m == 11) {
        daysInMonth = 30;
    }
    else {
        daysInMonth = 31;
    }

    // Check valid day
    if (d < 1 || d > daysInMonth) {
        printf("Invalid Date\n");
    } else {
        printf("Valid Date\n");
    }

    return 0;
}


# Output:
<img width="1762" height="863" alt="Screenshot 2025-12-26 232819" src="https://github.com/user-attachments/assets/1f1f0777-3457-47e4-ab29-709108edae0a" />
<img width="1766" height="857" alt="Screenshot 2025-12-26 232838" src="https://github.com/user-attachments/assets/f38d9d29-a4e6-495c-9e16-64a5b4339304" />

# Result: 
Thus, the program was implemented and executed successfully, and the required output was obtained.


# 19AI304-Fundamentals-of-C-Programming-2025-Odd-M4
# IAPR-4- Module 4 - FoC
# Ex.No:17
  Develop a C program to read two numbers from the user and determine the maximum and minimum values. Use user-defined functions with arguments and return values—one function to find the maximum (max()) and another to find the minimum (min()).
# Date : 
# Aim:
 To develop a C program that uses functions with parameters and return values to compute and display the maximum and minimum of two user-entered numbers.
# Algorithm:
### Step 1:
  Start
### Step 2: 
  Include the standard input-output library: #include<stdio.h>.
### Step 3: 
  Declare variables `num1`, `num2`, `maximum`, and `minimum`.
### Step 4: 
  Ask the user to enter two numbers.
### Step 5: 
  Read the numbers using `scanf`.
### Step 6: 
  Call the function `max(num1, num2)`.
### Step 7: 
  Inside function `max(num1, num2)`:
- **Step 7.1:** Receive two integer arguments.  
- **Step 7.2:** Compare the two numbers.  
- **Step 7.3:** If `num1 > num2`, return `num1`.  
- **Step 7.4:** Otherwise, return `num2`.
### Step 8: 
  Store the returned value in `maximum`.
### Step 9: 
  Call the function `min(num1, num2)`.
### Step 10: 
  Inside function `min(num1, num2)`:
- **Step 10.1:** Receive two integer arguments.  
- **Step 10.2:** Compare the two numbers.  
- **Step 10.3:** If `num1 > num2`, return `num2`.  
- **Step 10.4:** Otherwise, return `num1`.
### Step 11: 
  Store the returned value in `minimum`.
### Step 12: 
  Display the returned maximum and minimum values.
### Step 13: 
  Stop
# Program:#include <stdio.h>

// Function to find maximum
int max(int a, int b) {
    return (a > b) ? a : b;
}

// Function to find minimum
int min(int a, int b) {
    return (a < b) ? a : b;
}

int main() {
    int x, y;

    printf("Enter two numbers: ");
    scanf("%d %d", &x, &y);

    printf("Maximum value: %d\n", max(x, y));
    printf("Minimum value: %d\n", min(x, y));

    return 0;
}

# Output:
<img width="1909" height="798" alt="Screenshot 2025-12-26 233047" src="https://github.com/user-attachments/assets/e18dcde4-661f-4248-bacd-1d778ab573f1" />

# Result: 
Thus, the program was implemented and executed successfully, and the required output was obtained.


# 19AI304-Fundamentals-of-C-Programming-2025-Odd-M4
# IAPR-4- Module 4 - FoC
# Ex.No:18
  Develop a C program to convert temperatures between Celsius and Fahrenheit: Convert Celsius to Fahrenheit using a function that returns the converted value. Convert Fahrenheit to Celsius using another function that returns the converted value. Display the results in the main() function.
# Date : 
# Aim:
 To develop a C program that converts temperatures between Celsius and Fahrenheit using functions with return values.
# Algorithm:
### Step 1:
  Start
### Step 2: 
  Include the standard input-output library: #include<stdio.h>.  
### Step 3:
 Declare function prototypes:
 - `float celtof();`  
 - `float ftocel();`
### Step 4: 
  Enter the `main()` function.
### Step 5:
  Call the `celtof()` function to convert Celsius to Fahrenheit.
### Step 6: 
  Inside `celtof()` function:
 - Declare float variables `C` and `F`.  
 - Display the message: **"Enter the temperature in Celsius"**.  
 - Read the value of `C` from the user.  
 - Calculate Fahrenheit using the formula: `F = (C * 9 / 5) + 32`.  
 - Return `F` to `main()`.
### Step 7: 
  Print the returned Fahrenheit value in `main()`.
### Step 8: 
  Call the `ftocel()` function to convert Fahrenheit to Celsius.
### Step 9: 
  Inside `ftocel()` function:
 - Declare float variables `f` and `celsius`.  
 - Display the message: **"Enter the temperature in Fahrenheit"**.  
 - Read the value of `f` from the user.  
 - Calculate Celsius using the formula: `celsius = (f - 32) * 5 / 9`.  
 - Return `celsius` to `main()`.
### Step 10: 
 Print the returned Celsius value in `main()`.
### Step 11: 
 Stop
# Program:
#include <stdio.h>

// Convert Celsius to Fahrenheit
float celsiusToFahrenheit(float c) {
    return (c * 9 / 5) + 32;
}

// Convert Fahrenheit to Celsius
float fahrenheitToCelsius(float f) {
    return (f - 32) * 5 / 9;
}

int main() {
    float c, f;

    printf("Enter temperature in Celsius: ");
    scanf("%f", &c);

    printf("Fahrenheit: %.2f\n", celsiusToFahrenheit(c));

    printf("\nEnter temperature in Fahrenheit: ");
    scanf("%f", &f);

    printf("Celsius: %.2f\n", fahrenheitToCelsius(f));

    return 0;
}

# Output:

<img width="1749" height="825" alt="Screenshot 2025-12-26 233335" src="https://github.com/user-attachments/assets/dca78183-6fef-44c5-bdb9-cabd9bc30d7c" />

# Result: 
Thus, the program was implemented and executed successfully, and the required output was obtained.

 
# 19AI304-Fundamentals-of-C-Programming-2025-Odd-M4
# IAPR-4- Module 4 - FoC
# Ex.No:19
  Build a C program to print the elements of a given 4×4 matrix in spiral order starting from the top-left element and moving clockwise,using a user-defined parameterized function without return spiralPrint().
# Date : 
# Aim:
 To build a C program to display the elements of a 2D array in spiral form, traversing the outer elements first and then moving inward in a clockwise direction, using a user-defined parameterized function without return spiralPrint().
# Algorithm:
### Step 1:
  Start
### Step 2: 
  Include the standard input-output library: #include<stdio.h>.  
### Step 3: 
  Define constants `R` and `C` for the number of rows and columns in the matrix.
### Step 4: 
  Declare a function `spiralPrint(int m, int n, int a[R][C])` to print the matrix in spiral order.
### Step 5: 
  Inside `spiralPrint()` function:
 - Initialize variables:  
   - `k = 0` → starting row index  
   - `l = 0` → starting column index  
   - `m` → ending row index  
   - `n` → ending column index  
 - Repeat the following while `k < m` and `l < n`:
   - a. **Print the top row from left to right**:  
     - Loop from column `l` to `n-1` and print `a[k][i]`.  
     - Increment `k`.       
   - b. **Print the last column from top to bottom**:  
     - Loop from row `k` to `m-1` and print `a[i][n-1]`.  
     - Decrement `n`.       
   - c. **If `k < m`, print the bottom row from right to left**:  
     - Loop from column `n-1` to `l` and print `a[m-1][i]`.  
     - Decrement `m`.       
   - d. **If `l < n`, print the first column from bottom to top**:  
     - Loop from row `m-1` to `k` and print `a[i][l]`.  
     - Increment `l`.
### Step 6: 
  In the `main()` function:
- Declare and initialize a 4×4 matrix `a`.  
- Call `spiralPrint(R, C, a)` to print the elements in spiral order.
### Step 7: 
  Stop
# Program:

#include <stdio.h>
void spiralPrint(int a[4][4]) {
    int top = 0, bottom = 3, left = 0, right = 3, i;

    while (top <= bottom && left <= right) {

        for (i = left; i <= right; i++)
            printf("%d ", a[top][i]);
        top++;

        for (i = top; i <= bottom; i++)
            printf("%d ", a[i][right]);
        right--;

        for (i = right; i >= left; i--)
            printf("%d ", a[bottom][i]);
        bottom--;

        for (i = bottom; i >= top; i--)
            printf("%d ", a[i][left]);
        left++;
    }
}

int main() {
    int mat[4][4], i, j;

    printf("Enter 4x4 matrix elements:\n");
    for (i = 0; i < 4; i++)
        for (j = 0; j < 4; j++)
            scanf("%d", &mat[i][j]);

    printf("\nSpiral Order:\n");
    spiralPrint(mat);

    return 0;
}
# Output:
<img width="1851" height="864" alt="Screenshot 2025-12-26 233550" src="https://github.com/user-attachments/assets/96d7d78f-ebf6-4174-bdc3-b4401f48fd83" />


# Result: 
Thus, the program was implemented and executed successfully, and the required output was obtained.


# 19AI304-Fundamentals-of-C-Programming-2025-Odd-M4
# IAPR-4- Module 4 - FoC
# Ex.No:20
  Build a C program to convert a string such that the first and last characters, as well as the characters before and after each space, are converted to uppercase. Implement this using a user-defined parameterized function without return.
# Date : 
# Aim:
To build a C program to convert a string as described above, using a user-defined parameterized function without return convertFirstCLastC(char str[]).
# Algorithm:
### Step 1:
  Start
### Step 2: 
  Include the standard input-output library: #include<stdio.h>.  
### Step 3: 
  Declare a user-defined void function `convertFirstCLastC(char str[])` that takes the string as a parameter.
### Step 4: 
 Inside `convertFirstCLastC(char str[])` function:
 - Find the length of the string `len`.  
 - Convert the first character `str[0]` to uppercase.  
 - Loop through the string from index `1` to `len-2`:  
   - If a character is a space, capitalize the character before and after it.  
 - Convert the last character `str[len-1]` to uppercase.
### Step 5: 
 In `main()` function:
 - Declare a string `str[100]`.  
 - Read the input string from the user.  
 - Call the function `convertFirstCLastC(char str[])`.  
 - Print the modified string.
### Step 6: 
 Stop
# Program:
#include <stdio.h>
#include <ctype.h>
#include <string.h>

void convertUpper(char str[]) {
    int i, len = strlen(str);

    if (len == 0) return;

    str[0] = toupper(str[0]);
    if (str[len - 1] == '\n')
        str[len - 2] = toupper(str[len - 2]);
    else
        str[len - 1] = toupper(str[len - 1]);

    for (i = 1; str[i] != '\0'; i++) {
        if (str[i] == ' ') {
            str[i - 1] = toupper(str[i - 1]);
            if (str[i + 1] != '\0' && str[i + 1] != '\n')
                str[i + 1] = toupper(str[i + 1]);
        }
    }
}

int main() {
    char str[200];

    printf("Enter a string:\n");
    fgets(str, sizeof(str), stdin);

    convertUpper(str);

    printf("\nConverted string:\n%s", str);

    return 0;
}
# Output:
<img width="1897" height="826" alt="Screenshot 2025-12-26 233804" src="https://github.com/user-attachments/assets/115f45f8-1c5e-4509-93c8-133c0560e403" />

# Result: 
Thus, the program was implemented and executed successfully, and the required output was obtained.

