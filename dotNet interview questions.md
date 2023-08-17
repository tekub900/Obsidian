# https://www.c-sharpcorner.com/UploadFile/puranindia/C-Sharp-interview-questions/

# What is Boxing and Unboxing in C#? 

Boxing and Unboxing are both used for type conversions.

Converting from a value type to a reference type is called boxing. Boxing is an implicit conversion. Here is an example of boxing in C#.

```csharp
// Boxing
int anum = 123;
Object obj = anum;
Console.WriteLine(anum);
Console.WriteLine(obj);
```

Converting from a reference type to a value type is called unboxing. Here is an example of unboxing in C#.

```csharp
// Unboxing
Object obj2 = 123;
int anum2 = (int)obj;
Console.WriteLine(anum2);
Console.WriteLine(obj);
```
# What is the difference between a struct and a class in C#? 

Class and struct are both user-defined data types but have some major differences:

**Struct**

- The struct is a value type in C# and inherits from System.Value Type.
- Struct is usually used for smaller amounts of data.
- Struct can’t be inherited from other types.
- A structure can't be abstract.
- No need to create an object with a new keyword.
- Do not have permission to create any default constructor.

**Class**

- The class is a reference type in C#, and it inherits from the System.Object Type.
- Classes are usually used for large amounts of data.
- Classes can be inherited from other classes.
- A class can be an abstract type.
- We can create a default constructor.

Read the following articles to learn more about structs vs. classes, [Struct, and Class Differences in C#](https://www.c-sharpcorner.com/blogs/difference-between-struct-and-class-in-c-sharp).
# What is the difference between Interface and Abstract Class in C#? 

Here are some common differences between an interface and an abstract class in C#.

- A class can implement any number of interfaces, but a subclass can, at most, use only one abstract class.
- An abstract class can have non-abstract methods (concrete methods), while in the case of interface, all the methods have to be abstract.
- An abstract class can declare or use any variables, while an interface cannot do so.
- In an abstract class, all data members or functions are private by default, while in an interface, all are public; we can’t change them manually.
- In an abstract class, we need to use abstract keywords to declare abstract methods; in an interface, we don’t need that.
- An abstract class can’t be used for multiple inheritance, while the interface can be used for multiple inheritance.
- An abstract class uses a constructor, while we don’t have any constructor in an interface.

To learn more about the difference between an abstract class and an interface, visit [Abstract Class vs. Interface](https://www.c-sharpcorner.com/uploadfile/prasoonk/abstract-class-vs-interface/).
# What is an enum in C#? 

An enum is a value type with a set of related named constants, often called an enumerator list. The enum keyword is used to declare an enumeration. It is a primitive data type that is user-defined.

An enum type can be an integer (float, int, byte, double, etc.). But if you use it beside int, it has to be cast.

An enum is used to create numeric constants in the [[dotNET]] framework. All the members of the enum are enum type. Therefore, there must be a numeric value for each enum type.

The underlying default type of the enumeration element is int. By default, the first enumerator has the value 0, and the value of each successive enumerator is increased by 1. 

```csharp
enum Dow {Sat, Sun, Mon, Tue, Wed, Thu, Fri};
```
Some points about enum,

- Enums are enumerated data types in c#.
- Enums are not for the end-user. They are meant for developers.
- Enums are strongly typed constant. They are strongly typed, i.e., an enum of one type may not be implicitly assigned to an enum of another type even though the underlying value of their members is the same.
- Enumerations (enums) make your code much more readable and understandable.
- Enum values are fixed. Enum can be displayed as a string and processed as an integer.
- The default type is int, and the approved types are byte, sbyte, short, ushort, uint, long, and ulong.
- Every enum type automatically derives from System.Enum, and thus, we can use System.Enum methods on enums.
- Enums are value types created on the stack, not the heap.

For more details, follow the link, [Enums in C#](https://www.c-sharpcorner.com/uploadfile/puranindia/enums-in-C-Sharp/).
# What is the difference between constant and readonly in C#?

Const is nothing but "constant," a variable whose value is constant but at compile time. Therefore, it's mandatory to assign a value to it. By default, a const is static, and we cannot change the value of a const variable throughout the entire program.

Readonly is the keyword whose value we can change during runtime or assign it at run time but only through the non-static constructor.
[Difference Between Const, ReadOnly, and Static ReadOnly in C#](https://www.c-sharpcorner.com/UploadFile/c210df/difference-between-const-readonly-and-static-readonly-in-C-Sharp/).
# What is the difference between ref and out keywords?

The ref keyword passes arguments by reference. Therefore, any changes made to this argument in the method will be reflected in that variable when the control returns to the calling method.

The out keyword passes arguments by reference. This is very similar to the ref keyword.

*When an argument is passed as a ref, it must be initialized before it can be passed to the method. An out parameter, on the other hand, need not to be initialized before passing to a method.*


| **Ref**                                                                                                                              | **Out**                                                                                                                                        |
| ------------------------------------------------------------------------------------------------------------------------------------ | ---------------------------------------------------------------------------------------------------------------------------------------------- |
| The parameter or argument must be initialized first before it is passed to ref.                                                      | It is not compulsory to initialize a parameter or argument before it is passed to an out.                                                      |
| It is not required to assign or initialize the value of a parameter (which is passed by ref) before returning to the calling method. | A called method is required to assign or initialize a value of a parameter (which is passed to an out) before returning to the calling method. |
| Passing a parameter value by Ref is useful when the called method is also needed to modify the pass parameter.                       | Declaring a parameter to an out method is useful when multiple values need to be returned from a function or method.                           |
| It is not compulsory to initialize a parameter value before using it in a calling method.                                            | A parameter value must be initialized within the calling method before its use.                                                                |
| When we use REF, data can be passed bi-directionally.                                                                                | When we use OUT data is passed only in a unidirectional way (from the called method to the caller method).                                     |
| Both ref and out are treated differently at run time and they are treated the same at compile time.                                  |                                                                                                                                                |
| Properties are not variables, therefore it cannot be passed as an out or ref parameter.  ||
# Can “this” be used within a static method?

We can't use 'this' in a static method because the keyword 'this' returns a reference to the current instance of the class containing it. Static methods (or any static member) do not belong to a particular instance. They exist without creating an instance of the class and are called with the name of a class, not by instance, so we can’t use this keyword in the body of static Methods. However, in the case of Extension Methods, we can use the parameters of the method.
# What are properties in C#?

In C#, a property is a member of a class that provides a way to read, write or compute the value of a private field. It exposes a public interface to access and modify the data stored in a class while allowing the class to maintain control over how that data is accessed and manipulated.
```csharp
class Person
{
	private string name;
	public string Name
	{ 
		get { return name; }
		set { name = value; } 
	} 
}
```
# What is an extension method in C#?

In C#, an extension method is a static method used to extend the functionality of an existing type without modifying the original type or creating a new derived type. Extension methods allow developers to add methods to existing types, such as classes, structs, interfaces, enums, etc., not originally defined in those types.

Extension methods are declared in a static class and are defined as static methods with a special first parameter called the "this" parameter. The "this" parameter specifies the type being extended and allows the extension method to be called as if it were an instance method of that type.

For example, consider the following extension method that extends the string type by providing a method to capitalize the first letter of the string:

```csharp
public static class StringExtensions
{
    public static string CapitalizeFirstLetter(this string str)
    {
        if (string.IsNullOrEmpty(str))
            return str;
        return char.ToUpper(str[0]) + str.Substring(1);
    }
}
```

With this extension method, the CapitalizeFirstLetter method can be called on any string object like this:

```csharp
string s = "hello world";
string capitalized = s.CapitalizeFirstLetter(); // "Hello world"
```
# What is the difference between Dispose and Finalize in C#?

In C#, both the Dispose and Finalize methods are used to release resources, but they serve different purposes and behaviors.

The Dispose method releases unmanaged resources, such as file handles or database connections, not automatically managed by the .NET runtime. It is typically implemented in a class that implements the IDisposable interface, which defines the Dispose method.

The Dispose method is called explicitly by client code to release resources when they are no longer needed. It can be called implicitly using the statement, which ensures that the Dispose method is called when the object goes out of scope.

On the other hand, the Finalize method is used to perform cleanup operations on an object just before it is garbage collected. Therefore, it is typically implemented in a class that overrides the Object.Finalize method.

The garbage collector calls the Finalize method, which automatically manages the memory of .NET objects, to release unmanaged resources that have not been explicitly released by the Dispose method.

The main difference between the two methods is that the Dispose method is deterministic and can be explicitly called by client code. In contrast, the Finalize method is non-deterministic and is called by the garbage collector at an undetermined time.

It is important to note that objects that implement the Dispose method should also implement the Finalize method as a backup mechanism in case the client code does not call the Dispose method.

In summary, the Dispose method is used to release unmanaged resources deterministically. In contrast, the Finalize method is used as a backup mechanism to release unmanaged resources when the object is garbage collected.
# What is the difference between static, public, and void?
Public declared variables can be accessed from anywhere in the application. Static declared variables can be accessed globally without needing to create an instance of the class. Void is a type modifier which states the method and is used to specify the return type of a method in C#.
# What is the benefit of ‘using’ statement in C#?
The 'using' statement can be used in order to obtain a resource for processing before automatically disposing it when execution is completed.
# Differentiate between Break and Continue Statement.
Continue statement - Used in jumping over a particular iteration and getting into the next iteration of the loop.

Break statement - Used to skip the next statements of the current iteration and come out of the loop.
# Name all the C# access modifiers.

The C# access modifiers are -

- Private Access Modifier - A private attribute or method is one that can only be accessed from within the class.
- Public Access Modifier - When an attribute or method is declared public, it can be accessed from anywhere in the code.
- Internal Access Modifier - When a property or method is defined as internal, it can only be accessible from the current assembly point of that class.
- Protected Access Modifier - When a user declares a method or attribute as protected, it can only be accessed by members of that class and those who inherit it.