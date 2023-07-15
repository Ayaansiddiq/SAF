cpp
#include <iostream>
#include <cmath>

int main() {
    int choice;
    double operand1, operand2, result;
    char option;

    do {
        // Display menu
        std::cout << "Menu:\n";
        std::cout << "1. Addition\n";
        std::cout << "2. Subtraction\n";
        std::cout << "3. Multiplication\n";
        std::cout << "4. Division\n";
        std::cout << "5. Exponentiation\n";
        std::cout << "6. Square Root\n";
        std::cout << "7. Logarithm\n";

        // Read user's choice
        std::cout << "Enter your choice (1-7): ";
        std::cin >> choice;

        if (choice < 1 || choice > 7) {
            std::cout << "Invalid choice! Please try again.\n";
            continue;
        }

        // Read operand1
        std::cout << "Enter operand1: ";
        std::cin >> operand1;

        // Perform operation
        switch (choice) {
            case 1:  // Addition
                std::cout << "Enter operand2: ";
                std::cin >> operand2;
                result = operand1 + operand2;
                break;
            case 2:  // Subtraction
                std::cout << "Enter operand2: ";
                std::cin >> operand2;
                result = operand1 - operand2;
                break;
            case 3:  // Multiplication
                std::cout << "Enter operand2: ";
                std::cin >> operand2;
                result = operand1 * operand2;
                break;
            case 4:  // Division
                std::cout << "Enter operand2: ";
                std::cin >> operand2;
                if (operand2 != 0) {
                    result = operand1 / operand2;
                } else {
                    std::cout << "Error: Division by zero!\n";
                    continue;
                }
                break;
            case 5:  // Exponentiation
                std::cout << "Enter operand2: ";
                std::cin >> operand2;
                result = pow(operand1, operand2);
                break;
            case 6:  // Square Root
                result = sqrt(operand1);
                break;
            case 7:  // Logarithm
                result = log(operand1);
                break;
        }

        // Display result
        std::cout << "Result: " << result << std::endl;

        // Ask if the user wants to continue
        std::cout << "Do you want to perform another calculation? (y/n): ";
        std::cin >> option;

    } while (option == 'y' || option == 'Y');

    std::cout << "Calculator closed.\n";

    return 0;
}
