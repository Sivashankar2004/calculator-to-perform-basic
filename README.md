# calculator-to-perform-

#include <stdio.h>

int main() {
    char operator;
    double num1, num2, result;

    // Get the operation from the user
    printf("Enter an operator (+, -, *, /): ");
    scanf("%c", &operator);

    // Get two numbers from the user
    printf("Enter two numbers: ");
    scanf("%lf %lf", &num1, &num2);

    // Perform the operation
    switch (operator) {
        case '+':
            result = num1 + num2;
            break;
        case '-':
            result = num1 - num2;
            break;
        case '*':
            result = num1 * num2;
            break;
        case '/':
            if (num2 != 0)
                result = num1 / num2;
            else {
                printf("Error! Division by zero is not allowed.\n");
                return 1;
            }
            break;
        default:
            printf("Error! Invalid operator.\n");
            return 1;
    }

    // Output the result
    printf("Result: %.2lf\n", result);

    return 0;
}
