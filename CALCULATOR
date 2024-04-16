#include <iostream>
#include <stdexcept>

using namespace std;

class Calculator {
private:
    int x, y;
    double z;
    char operation;

public:
    void setdata() {
        cout << "Enter the first number: ";
        cin >> x;
        cout << "Enter the second number: ";
        cin >> y;
        cout << "Enter the mathematical operation you want to perform (+, -, *, /, %): ";
        cin >> operation;
    }

    void getdata() {
        try {
            if (operation == '+') {
                z = x + y;
                cout << "The addition of the numbers is: " << z << endl;
            } else if (operation == '-') {
                z = x - y;
                cout << "The subtraction of the numbers is: " << z << endl;
            } else if (operation == '*') {
                z = x * y;
                cout << "The product of the numbers is: " << z << endl;
            } else if (operation == '/') {
                if (y == 0) {
                    throw runtime_error("Division by zero is not possible");
                }
                z = static_cast<double>(x) / y;
                cout << "The quotient is: " << z << endl;
            } else if (operation == '%') {
                z = x % y;
                cout << "The remainder is: " << z << endl;
            } else {
                throw runtime_error("Invalid operation");
            }
        } catch (const runtime_error& e) {
            cout << "Error: " << e.what() << endl;
        } catch (...) {
            cout << "An unknown error occurred." << endl;
        }
    }
};

int main() {
    Calculator calculatorObject;
    calculatorObject.setdata();
    calculatorObject.getdata();

    return 0;
}
