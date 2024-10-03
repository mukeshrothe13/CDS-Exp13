# AIM
To learn function overloading in C++.

## Software Used
- VS Code

## Problem Statement
1. Write a C++ program to demonstrate function overloading.
2. Write a C++ program to demonstrate operator overloading.

## Theory
Function overloading is a feature of object-oriented programming that allows two or more functions to have the same name but different parameters. When a function name is reused for different functionalities, it is referred to as function overloading. In this case, the function names remain the same while the arguments differ. Function overloading is an example of polymorphism in C++.

Operator overloading is a form of compile-time polymorphism. It allows us to give special meaning to an existing operator in C++ without altering its original functionality.

This article will explore operator overloading in C++ with examples, detailing which operators can and cannot be overloaded.

## Program Codes
```javascript
//Mukesh Rothe 23070123089
#include<iostream>
using namespace std;
int add(int a, int b){
    return a+b ;
}
float add(float a, float b)
{
    return a+b;
}
int add(int a, int b , int c){
    return a+b+c;
}
int main() {
    cout<<"Addition of 2 integers- "<<add(3,4)<< endl;
    cout<<"Addition of 2 floats- "<<add(3.5f, 4.5f)<<endl;
    cout<<"Addition of 3 integers- "<< add(1,2,3)<<endl;
    return 0;
    }
```
```javascript
//Mukesh Rothe 23070123089
#include<iostream>
using namespace std;
class Complex {
    private:
    float real;
    float imag;
     public:
     Complex(float r =0 , float i = 0)
     {
        real = r;
        imag =i;
     }
Complex operator + (const Complex &obj)
{
    Complex temp;
    temp.real = real + obj.real;
    temp.imag = imag + obj.imag;
    return temp;
}
void display()const {
    cout<< real<<" + "<< imag<< "i"<<endl;
}
};
int main() {
    Complex c1(3.5,2.5);
    Complex c2(1.6,3.7);
    Complex c3 = c1 +c2;
    cout << "First complex number- ";
    c1.display();
    cout << "Second complex number- ";
    c2.display();
    cout << "Sum of complex numbers- ";
    c3.display();
    return 0;
}
```
## Output
Function Overloading

![Screenshot 2024-10-03 145132](https://github.com/user-attachments/assets/3b131668-d789-42a7-8624-1e18ba711c79)

Operator Overloading

![Screenshot 2024-10-03 145051](https://github.com/user-attachments/assets/c0d1c523-cae0-4d72-aae7-ffc504afa3a9)

## Conclusion
We have learned how to implement both function and operator overloading in C++.
