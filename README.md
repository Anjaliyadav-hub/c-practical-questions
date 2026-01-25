# c-practical-questions

<h2> Write a program to swap two numbers using pointers</h2>

#include <iostream>
using namespace std;
int main(){
    int a, b;
    int *p1, *p2;
    cout << "Enter two numbers: ";
    cin >> a >> b;

    p1 = &a;
    p2 = &b;

    int temp = *p1;
    *p1 = *p2;
    *p2 = temp;

    cout << "After swapping:\n";
    cout << "a = " << a << endl;
    cout << "b = " << b << endl;

    return 0;
}

-------

<h2>Write a C++ program that: Declares one global variable Declares one local variable inside main() Dynamically allocates one integer using new Print the addresses of all three and identify which memory region each belongs to.</h2>

#include <iostream>
using namespace std;

int globalVar = 100;

int main() {
   
    int localVar = 200;

    int *dynamicVar = new int(300);

    cout << "Address of global variable: " << &globalVar << " (Global/Static Memory)" << endl;
    cout << "Address of local variable: " << &localVar << " (Stack Memory)" << endl;
    cout << "Address of dynamically allocated variable: " << dynamicVar << " (Heap Memory)" << endl;

    // Free the dynamically allocated memory
    delete dynamicVar;

    return 0;
}
--------
<h2>Write a function square(int) and call it:Normally
Using a function pointer</h2>

#include <iostream>
using namespace std;

int square(int n) {
    return n * n;
}

int main() {
    int num = 25;

    cout << "Normal call: " << square(num) << endl;

    // Using function pointer
    int (*funcPtr)(int) = square;   
    cout << "Using function pointer: " << funcPtr(num) << endl;

    return 0;
}
-----------

<h2>Write a program to print:Value of a variable
Address of the variable
Value stored in the pointer </h2>

#include <iostream>
using namespace std;

int main() {
    int x = 10;      // variable
    int *p = &x;     // pointer storing address of x

    cout << "Value of variable x: " << x << endl;
    cout << "Address of variable x: " << &x << endl;
    cout << "Value stored in pointer p: " << p << endl;

    return 0;
}

---------

<h2>Write a program where a pointer stores the address of another variable and copies its value into a third variable using dereferencing.</h2>

#include <iostream>
using namespace std;

int main() {
    int a = 10;      // first variable
    int *p = &a;     // pointer stores address of a
    int b;           // third variable

    b = *p;          // copy value using dereferencing

    cout << "Value of a: " << a << endl;
    cout << "Address of a (stored in p): " << p << endl;
    cout << "Value copied into b: " << b << endl;

    return 0;
}










