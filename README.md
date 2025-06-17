# Calculator
Program: Develop a menu-driven program to implement arithmetic operations such as +, -, *, /, and % using UDF, switch case, and looping. Make sure that the program is endless until a certain letter is pressed.

Code:
```cpp
#include <iostream>
using namespace std;

int add(int a, int b) {
    return a + b;
}

int subtract(int a, int b) {
    return a - b;
}

int multiply(int a, int b) {
    return a * b;
}

float divide(int a, int b) {
    if (b == 0) {
        cout << "Error: Division by zero!" << endl;
        return 0;
    }
    return (float)a / b;
}

int modulo(int a, int b) {
    if (b == 0) {
        cout << "Error: Modulo by zero!" << endl;
        return 0;
    }
    return a % b;
}

int main() {
    char continueChoice;

    do {
        int num1, num2;
        char operation;

        cout << "======= Arithmetic Calculator =======" << endl;
        cout << "Enter an operator (+, -, *, /, %): ";
        cin >> operation;

        // Check using nested if-else
        if (operation == '+' || operation == '-' || operation == '*' || operation == '/' || operation == '%') {
            cout << "Enter the first number: ";
            cin >> num1;

            cout << "Enter the second number: ";
            cin >> num2;

            // Perform using switch-case
            switch (operation) {
                case '+':
                    cout << "Result: " << add(num1, num2) << endl;
                    break;
                case '-':
                    cout << "Result: " << subtract(num1, num2) << endl;
                    break;
                case '*':
                    cout << "Result: " << multiply(num1, num2) << endl;
                    break;
                case '/':
                    cout << "Result: " << divide(num1, num2) << endl;
                    break;
                case '%':
                    cout << "Result: " << modulo(num1, num2) << endl;
                    break;
            }
        } else {
            cout << "Invalid operator! Please try again." << endl;
        }

        cout << "\nPress 'q' or 'Q' to quit, any other key to continue: ";
        cin >> continueChoice;

    } while (continueChoice != 'q' && continueChoice != 'Q');

    cout << "\nThank you for using the calculator!" << endl;
    return 0;
}
```
Output:
![Calculator](https://github.com/jinaljain0705/DSA-with-C--/blob/Project-5/Project%20-%20Calculator/Output/calculator.png)
