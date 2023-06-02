#datatype
<img src="https://github.com/SenWang53/myCPP/assets/97141078/51e24e4b-5050-4c02-bdf6-1ce845c4320a" height="300" width="500">

```
// test 1
// datatype test

#include <iostream>
using namespace std;

int main(void)
{
  cout << "size of int:    " << sizeof(int)    << endl;
  cout << "size of char:   " << sizeof(char)   << endl;
  cout << "size of float:  " << sizeof(float)  << endl;
  cout << "size of double: " << sizeof(double) << endl;
  cout << "size of bool:   " << sizeof(bool)   << endl;

  return 0;
}
```

datatype modifiers
short, long, unsigned, sigend
Above values may vary from compiler to compiler. 

Macro Constants
CHAR_MIN, CHAR_MAX, and so on.

# Input and Output
https://www.geeksforgeeks.org/basic-input-output-c/
In C++ input and output are performed in the form of a sequence of bytes or more commonly known as streams.
![C-basic-input-output](https://github.com/SenWang53/myCPP/assets/97141078/ef68b0ba-744a-40c4-98ba-0d5831399366)

Un-buffered standard error stream (cerr)
The main difference between cerr and cout comes when you would like to redirect output using “cout” that gets redirected to file if you use “cerr” the error doesn’t get stored in file.(This is what un-buffered means ..It cant store the message)

buffered standard error stream (clog)

# C/C++ Preprocessors
Types of C/C++ Preprocessors
There are 4 Main Types of Preprocessor Directives:  

Macros
File Inclusion
Conditional Compilation
Other directives

## specific syntaxes
```
#include <iostream>
using namespace std;

void func1();
void func2();

void __attribute__((constructor)) func1();
void __attribute__((destructor)) func2();

void func1()
{
	printf("Inside func1()\n");
}

void func2()
{
	printf("Inside func2()\n");
}

// Driver code
int main()
{
	printf("Inside main()\n");

	return 0;
}

// This code is contributed by Shivani
```
# operator
![image](https://github.com/SenWang53/myCPP/assets/97141078/04c16af3-7343-4a3d-9c10-26a603ce4f41)

# loops
![image](https://github.com/SenWang53/myCPP/assets/97141078/9fee3aa4-d36b-44c8-8b35-f9cc1e43f311)

# Decision Making in C / C++
![image](https://github.com/SenWang53/myCPP/assets/97141078/fd4999bf-e881-4c01-8532-33f331aea7c6)

Jump Statements: 
break
continue
goto
return

# Functions in C++
![image](https://github.com/SenWang53/myCPP/assets/97141078/434489f8-6c1b-4334-a78d-973c62e7cce3)

![image](https://github.com/SenWang53/myCPP/assets/97141078/9d349254-a183-48a8-b1d5-bef38f083cab)

![image](https://github.com/SenWang53/myCPP/assets/97141078/cc51a1a0-39e7-4216-95c3-7494acc45f20)

![image](https://github.com/SenWang53/myCPP/assets/97141078/ee1a651d-aeca-49ab-8816-e5e9cb50ace1)

| Call by value | Call by reference |
| ----------- | ----------- |
| A copy of value passed to the function | An address of value is passed to the function |
| Changes made inside the function is not reflected on other functions | Changes made inside the function is reflected outside the function also |
| Actual and formal arguments will be created in different memory location | Actual and formal arguments will be created in same memory location. |

## C++ Overloading (Function)
If we create two or more members having the same name but different in number or type of parameter, it is known as C++ overloading. In C++, we can overload:
methods,
constructors and
indexed properties
It is because these members have parameters only.

### Types of overloading in C++ are:
Function overloading
Operator overloading

#### Function overloading
Causes of Function Overloading:
Type Conversion.
Function with default arguments.
Function with pass by reference.

Type Conversion.
```
#include <iostream>
using namespace std;
void fun(int);
void fun(float);
void fun(int i) { cout << "Value of i is : " << i << endl; }
void fun(float j)
{
    cout << "Value of j is : " << j << endl;
}
int main()
{
    fun(12);
    fun(1.2);
    return 0;
}
 
// Code Submitted By Susobhan Akhuli
```
error: call of overloaded ‘fun(double)’ is ambiguous

#### Operator overloading
Operator overloading is a compile-time polymorphism.
