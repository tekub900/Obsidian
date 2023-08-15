# What is the difference between [[C]] and [[C++]]?

| [[C]]                                                      | [[C++]]                                                      |
| ---------------------------------------------------------- | ------------------------------------------------------------ |
| [[C]] is a procedure-oriented(műveletorientált) programming language         | [[C++]] is a partially object-oriented programming language  |
| It follows a top-down approach                             | It follows a bottom-up approach                              |
| [[C]] doesn’t support function or operator overloading     | [[C++]] supports function as well as function overloading    |
| [[C]] language doesn’t support virtual and friend function | [[C++]] language supports both virtual and friend functions. |
| [[C]] language has 32 keywords                             | [[C++]] language contains 52 keywords                        |
# What are #class(es) and objects in [[C++]]?

A #class is like a blueprint of an object. It is a user-defined data type with data members and member functions and is defined with the keyword #class.
```cpp
class class_name
{
	Access specifier;
	data members;
	member functions()
};
```
You define objects as an instance of a #class. Once it creates the object, then it can operate on both data members and member functions.
# What are access modifiers?

You use access modifiers to define accessibility for the #class members. It defines how to access the members of the #class outside the #class scope.

There are three types of access modifiers:

- Private
- Public
- Protected
# Difference between equal to (\==) and assignment operator(=)?

The equal to operator == checks whether two values are equal or not. If equal, then it’s true; otherwise, it will return false.

The assignment operator = allots the value of the right-side expression to the left operand.
# What is the difference between a while loop and a do-while loop?

| while                                                                                                            | do-while                                                                                               |
| ---------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------ |
| The while loop verifies the condition; if it’s true, then it iterates the loop till the condition becomes false. | The do-while loop first iterates the loop body once, then it checks for the condition.                 |
| Syntax:<br><br>while (condition)<br><br>{<br><br>       statements  <br><br>}                                    | Syntax:   <br><br>   do{<br><br>        statements     <br><br>       }<br><br>      while(condition); |
| If the condition is false in a while loop, then not a single statement will execute inside the loop.             | If the condition in a do-while loop is false, then the body will also execute once.                    |
# What is the size of the int data type?
1. 4 bytes
2. 1 byte
3. 8 bytes
4. 2 bytes

1 - 4 bytes, the integer data type is 4 bytes.
# Which among the following operators cannot be overloaded?

1. -
2. +
3. ?:
4. %

3 - ?: operator cannot be overloaded because it is not syntactically possible.
# What among these is used to return the number of characters in the string?

1. Size
2. Length
3. Both size and length
4. Name

3 - Both size and length are used to return the number of characters in the string.
# Discuss the difference between prefix and postfix?

In prefix (++i), first, it increments the value, and then it assigns the value to the expression.

In postfix (i++), it assigns the value to the expression, and then it increments the variable's value.
# Can you compile a program without the main function?

Yes, you can compile a program without the main function, but you cannot run or execute the program because the main() function is the entry point, from where all the execution begins. And without the entry point, then you can execute the program.
# What is std in C++?

1. std is a standard #class in C++
2. std is a standard file reading header
3. std is a standard header file
4. std is a standard namespace

4 - std is a standard namespace in C++
# What are the four different data types in C++?

- Primitive/Basic: Char, int, short, float, double, long, bool, void, wide character, etc.
- Derived(származtat): Array, pointer, function, reference, etc.
- User-defined: #Structure, class, enum, union, typedef, etc.
# How is struct different from #class?   

|  #Structure |  #Class |
|---|---|
|Its members are public by default.|Its members are private by default.|
|The default access specifiers are public when deriving a struct from a class/struct.|The default access specifiers are private when deriving a class.|
# What do you understand about polymorphism in C++? 

The term polymorphism refers to the presence of multiple forms. Polymorphism usually occurs when there is a hierarchy of classes that are linked by inheritance.

C++ polymorphism means that depending on the type of object that invokes the function, a different function will be executed.
# Compare compile time and runtime polymorphism.

| Compile-time Polymorphism  | Runtime Polymorphism  |
|---|---|
|The method to be executed is known at compile time. And the call is resolved by the compiler.|The method to be executed is known at run time. The compiler does not resolve the call.|
|Provides quicker execution because it is known at the compile time.|Provides slower execution because it is known at the run time.|
|Achieved by operation or function overloading.|Achieved by function overriding.|
# What is a constructor in [[C++]]?

In [[C++]], a function Object is a particular "MEMBER FUNCTION" that shares the same title as the class it belongs to and is used to initialize specific values to an object's data members.
```cpp
#include <iostream>

using namespace std;

class student
{

	int rno;

	public:

	    student()
	    {
	        cout << "Enter the RollNo:";
	        cin >> rno;
		}

	    void display()
	    {
	    
        cout << endl << rno << "\t";
	    }
};

int main()
{
    student s; // constructor gets called automatically when
               // we create the object of the class
    s.display();

    return 0;

}```
# What is a virtual function?

A member function in the base class redefined in a derived class is a virtual function. It is declared using the virtual keyword. It ensures that the correct function is called for an object, irrespective of the type of reference/pointer used for the function call. Virtual functions are mainly used for runtime polymorphism.
# What do you understand about friend class and friend function?

Like a friend function, a friend class can access personal and guarded variables of the type in which it is declared. All member functions for classes specified as friends to another class are friend functions for the friend class.
```cpp
class Node
{

	private:
		int key;

	Node* next;
	
	/* Other members of Node Class */
	
	// Now class LinkedList can
	
	// access private members of Node

	friend class LinkedList;
};
```
# What is an abstraction in C++?

Abstraction means displaying the essential details to the user while hiding the irrelevant or particular details that you don’t want to show to a user. It is of two types:

- Control abstraction
- Data abstraction
# What are destructors in C++?

A destructor member function is instantly called when an object exits its scope or is specifically deleted by a call to delete.
```cpp
class X
{
	public:

	// Constructor for class X

	 X();

	 // Destructor for class X

	 ~X();

};
```
# Is it possible to overload a deconstructor? Give reasons for your answer. 

No, it is impossible as destructors do not take arguments or return anything. There has to be only one empty destructor per class. It should have a void parameter list.
# What is an abstract class? When is it used? 

An abstract class is a class whose objects cannot be created. It serves as a parent for the derived classes. Placing a pure virtual function in the class makes it an abstract class.
# What do you understand about static members and static member functions?

A variable in a class declared as static has its space allocated for the lifetime of the program. Regardless of the number of objects of that class created, there is only a single copy of the static member. The same static member is accessible to all the objects of that class.

A static member function can be called even if no class objects exist. It is accessed using only the class name and the scope resolution operator (::).
The static data member of a class is a normal data member but preceded with a static keyword. It executes before main() in a program and is initialized to 0 when the first object of the class is created. It is only visible to a defined class but its scope is of a lifetime.

Syntax:
```cpp
static Data_Type Data_Member;
```
The static member function is the member function that is used to access other static data members or other static member functions. It is also defined with a static keyword. We can access the static member function using the class name or class objects.

Syntax:
```cpp
classname::function name(parameter);
```
# What is the C++ OOPs concept?

[OOPs concept in C++](https://www.simplilearn.com/tutorials/cpp-tutorial/oops-concepts-in-cpp "OOPs concept in C++"):                                                                               

- Object
- Class
- Inheritance
- Polymorphism                                       
- Encapsulation
- Abstraction

Object: Anything that exists physically in the real world is called an object.

Class: The collection of objects is called class.

Inheritance: Properties of parent class inherited into child class is known as inheritance.

Polymorphism: It is the ability to exist in more than one form.

Encapsulation: Binding of code and data together into a single unit.

Abstraction: Hiding internal details and showing functionality to the user.
# When is void() return type used?

You use the void() return type when you don’t want to return any value. It specifies that the function doesn’t return a value. A function with a void return type completes its task and then returns the control to the caller.
# What is call by value and call by reference in C++?

In the call-by-value method you pass the copies of actual parameters to the function's formal parameters. This means if there is any change in the values inside the function, then that change will not affect the actual values.

In the call-by-reference method, the reference or address of actual parameters is sent to the function's formal parameters. This means any change in values inside the function will be reflected in the actual values.
# What is an inline function?

An [inline function](https://www.simplilearn.com/tutorials/cpp-tutorial/inline-function-in-cpp "inline function") when called expands in line. When you call this function, the whole code of the inline function gets inserted or substituted at the inline function call.
```cpp
Inline return-type function-name(parameters)
{

}
```
# What are pointers in C++?

[Pointers](https://www.simplilearn.com/tutorials/cpp-tutorial/pointers-in-cpp "Pointers") are the variables that store the memory address of another variable. The type of the variable must correspond with the type of pointer.

Syntax: type *name*
# What is a scope resolution operator?

A scope resolution operator is represented as ::

This operator is used to associate function definition to a particular class.

The scope operator is used for the following purposes:

- To access a global variable when you have a local variable with the same name.
- To define a function outside the class.
# What is a constructor?

A [constructor is defined](https://www.simplilearn.com/tutorials/cpp-tutorial/constructor-in-cpp "constructor is defined") as a member function that is invoked whenever you create an object; it has the same name as that of the class.

There are two types of constructors:

- Default constructor: This auto-generated constructor doesn’t take any arguments.
- Parameterized constructor: In this constructor, it can pass arguments.
# Discuss the difference between new and malloc

| new  |  malloc |
|---|---|
|new is an operator|malloc() is a function|
|It calls the constructor|The malloc function doesn’t call the constructor|
|There is no need to specify memory size while using new()|You have to specify the memory size|
|new operator can be overloaded|malloc() can never be overloaded|
# What is operator overloading?

Operator overloading is a mechanism in which a special meaning is given to an operator.

For example, you can overload the ‘+’ operator in a class-like string to concatenate two strings by only using ‘+.’
# What is the output of the below C++ program?
```cpp
#include <iostream>

using namespace std;
int main()
{
	enum { blue, green = 5, GREAT };

	cout << blue << " " << GREAT;
}
```

1. 0 3
2. 0 8
3. 0 6
4. 0 2

3 - 0 6. In enum, the element's value is one greater than the previous element. The value of blue is 0 by default, and the value of green is five, so the value of GREAT will become six automatically.
# What is STL?

STL stands for standard template library. It is a library of container templates that provide generic classes and functions.

STL components are containers, algorithms, iterators, and function objects.
# What is inheritance?

[Inheritance is the mechanism](https://www.simplilearn.com/tutorials/cpp-tutorial/inheritance-in-cpp "Inheritance is the mechanism") in which you can create a new class i.e. child class from the existing class i.e. parent class. This child class is also known as a derived class and the parent class is also called Base class.
# How are virtual functions different from pure virtual functions?

A virtual function is a base class member function that a derived class can modify. A member function of a base class that is a pure virtual function must be defined in the derived type; otherwise, the derived class will become abstract as well.
```cpp
interface Woo
{    

	void print();    

}    

class Bat implements Woo
{    

	public void print(){System.out.println("Woo!");}    

	public static void main(String args[]){    

		Bat obj = new Bat();    

		obj.print();    

	 }    

}
```

|Virtual Function|Pure Virtual Function|
|---|---|
|A Virtual Function is a member function of a base class that can be redefined in another derived class.|A Pure Virtual Function is a member function of a base class that is only declared in a base class and defined in a derived class to prevent it from becoming an abstract class.|
|A virtual Function has its definition in its respective base class.|There is no definition in Pure Virtual Function and is initialized with a pure specifier **(= 0).**|
|The base class has a virtual function that can be represented or instanced; In simple words, its object can be made.|A base class having pure virtual function becomes abstract that cannot be represented or instanced; In simple words, it means its object cannot be made.|
# Class D is derived from a base class B. If creating an object of type D, what order will the constructors of these classes get called?

The derived class consists of two parts: the base part and the derived part. C++ constructs derived objects in phases. The process begins with constructing the most-base class (at the top of the inheritance tree), followed by each child class construction in order, and then the most-child class. Thus, first, the Constructor of class B will be called, and then the constructor of class D.
# C++ \#define
Preprocessor commands that begin with a pound or hash symbol (#) are known as directives. There should be no white space before the #, and a semicolon is not required at the end of the statement beginning with "#."

Many things that can be done during the preprocessing phase include:

- Inclusion of other files through the \#include directive
- Definition of symbolic constants and macros through the \#define directive

Through some preprocessor directives, you can also conditionally compile or execute some preprocessor directives.
The \#define preprocessor allows us to define symbolic names and constants. For example,
```cpp
#define PI 3.14159
```
#  [Header files](https://learn.microsoft.com/en-us/cpp/cpp/header-files-cpp?view=msvc-170)
