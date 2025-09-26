# Coddy-Code-
I post my coddy code https://coddy.tech/journeys/csharp/fundamentals
Modifying Arrays


In addition to accessing the elements of an array, you can also modify them. To modify a specific element in an array, you can assign a new value to it using its index.

Here's an example:

string[] my_array = {"apple", "banana", "cherry"};
my_array[1] = "orange";
System.Console.WriteLine(my_array[0] + ", " + my_array[1] + ", " + my_array[2]);
Output:

apple, orange, cherry
banana was changed to an orange

Arrays are collections of items created using square brackets [] with items separated by commas:

int[] numbers = {1, 2, 3, 4, 5};
Check array length using the .Length field:

int length = numbers.Length;
Create arrays with the new keyword specifying type and size:

int[] numbers = new int[5]; // Creates array of 5 integers, all initialized to 0
A void method performs actions without returning a value:

public static void MethodName(parameters) {
    // Code to be executed
}
Use void methods for tasks like printing output, modifying object states, or executing operations that don't need to return a result.

Optional parameters in C# allow you to define default values in method signatures. If no argument is provided when calling the method, the default value is used.

Basic syntax:

access_modifier return_type method_name(parameter_type parameter_name = default_value) {
    // Method body
}
Example:

public void Greet(string name = "Guest") {
    Console.WriteLine("Hello, " + name + "!");
}

// Usage:
Greet("Alice"); // Output: Hello, Alice!
Greet(); // Output: Hello, Guest!
Important rules:

Optional parameters must appear after all required parameters
Once you define an optional parameter, all subsequent parameters must also be optional
The return statement specifies the value a method produces as output:

public static int FunctionName() {
    return 100;
}
To capture the returned value in a variable:

int number = FunctionName();
The return type of the method must match the data type of the variable storing the returned value.

Method arguments are values passed into a method when calling it. Define arguments inside parentheses with their data types:

return_type method_name(data_type arg1, data_type arg2, ...) {
    // code
}
Call a method by passing values as arguments:

method_name(value1, value2, value3, ...);
Example:

public static void IsEven(int number) {
    if (number % 2 == 0) {
        Console.WriteLine(number + " is even");
    } else {
        Console.WriteLine(number + " is odd");
    }
}

IsEven(15); // Call method with argument 15
Note: Passing too many arguments to a method will cause the program to fail.

A method is a sequence of code that has a name, used to reuse code multiple times.

Method syntax:

access_modifier return_type method_name(parameters) {
    // code
}
Example method declaration:

public static void Greet() {
    Console.WriteLine("Welcome to Coddy");
}
To call/execute a method:

Greet();
Important: The method code must come before its call/execution.

An infinite loop is a loop that never stops because its condition always evaluates to true.

Intentional infinite while loop:

while (true) {
    Console.WriteLine("This will print forever!");
}
Infinite for loop with omitted parts:

for (;;) {
    Console.WriteLine("This also prints forever!");
}
Unintentional infinite loop (missing increment):

int i = 0;
while (i < 10) {
    Console.WriteLine("i is: " + i);
    // Missing i++ to increment i
}
A nested loop is a loop inside another loop. The inner loop completes all its iterations for each single iteration of the outer loop.

Example of nested loops:

for (int x = 0; x < 2; x++) {
    for (int y = 0; y < 2; y++) {
        Console.WriteLine(x + " " + y);
    }
}

// Output:
// 0 0
// 0 1
// 1 0
// 1 1
The outer loop runs twice, and for each iteration, the inner loop runs twice completely.

The continue statement stops the current iteration and continues to the next iteration:

for (int i = 3; i < 9; i++) {
    if (i == 5) {
        continue;
    }
    Console.WriteLine(i);
}
This will skip the iteration when i=5 and output:

3
4
6
7
8
The break statement stops the loop instantly when it's encountered.

for (int i = 0; i < 10; i++) { 
    if (i == 6) {
        break;
    }
    Console.WriteLine(i);
}
This loop exits when i equals 6, printing numbers 0 through 5.

The do-while loop executes the code block at least once before checking the condition:

do {
    // Code to be executed
} while (condition);
Example:

int count = 0;
do {
    Console.WriteLine("Count: " + count);
    count++;
} while (count < 5);
The loop body runs first, then the condition is checked. The loop continues as long as the condition is true.

A while loop executes code as long as a condition is true:

while (condition) {
    code
}
Unlike for loops that iterate over a specific range, while loops continue based on a condition being met.

The for loop allows you to repeat code multiple times with the following syntax:

for (initialization; condition; update) {
    code
}
Example - loop from 0 to 5 (not including):

for (int i = 0; i < 5; i++) {
    Console.WriteLine(i);
}
This outputs:

0
1
2
3
4
Example - sum numbers from 1 to 100:

int sumNumbers = 0;
for (int i = 1; i <= 100; i++) {
    sumNumbers += i;
}
Console.WriteLine(sumNumbers);
Use Parse methods to convert strings to other data types:

string numberString = "42";
int number = int.Parse(numberString); // Converts "42" to integer 42
Parse throws a FormatException if the conversion fails:

string invalidNumberString = "abc";
int number = int.Parse(invalidNumberString); // Throws FormatException
Common Parse methods:

Data Type	Parse Method	Example
int	int.Parse()	int number = int.Parse("42");
double	double.Parse()	double number = double.Parse("42.5");
float	float.Parse()	float number = float.Parse("42.5");
bool	bool.Parse()	bool isTrue = bool.Parse("true");
To get input from a user, use Console.ReadLine(). This method reads a line of text and returns it as a string:

string name = Console.ReadLine();
Console.WriteLine("Your name is: " + name);
The program waits for the user to enter text and press Enter before continuing.

To insert variable values into strings, use string interpolation with $ and {}:

int age = 30;
string name = "Alice";
System.Console.WriteLine($"Name: {name}, Age: {age}");
Alternatively, use the + operator to concatenate strings:

System.Console.WriteLine("Name: " + name + " Age: " + age);
To display output to the console in C#, use the Console.WriteLine method:

Console.WriteLine("Hello, world!");
Console.WriteLine(42);
The Console.WriteLine method prints text or values and moves to a new line afterward. It can handle different data types including strings, numbers, and variables.

Include the System namespace at the start of your program:

using System;
This allows you to use Console.WriteLine without writing System.Console every time.

You can nest if-elif-else statements within each other to create hierarchical decision-making structures:

if (age > 18) {
    if (hasLicense) {
        System.Console.WriteLine("You can drive");
    } else {
        System.Console.WriteLine("Get a license first");
    }
} else {
    System.Console.WriteLine("Too young to drive");
}

Nesting can be done infinitely:

if (condition1) {
    if (condition2) {
        if (condition3) {
            // if condition1, condition2 and condition3 are true
            ...
        }
    }
}
The ternary operator is a one-line if-else statement with the syntax:

variable = (condition) ? value_if_true : value_if_false;
It evaluates the condition and assigns value_if_true if the condition is true, otherwise assigns value_if_false.

Example:

int age = 20;
string message = (age >= 18) ? "Adult" : "Minor";
The switch statement is a multi-way conditional that checks a variable against multiple cases:

switch (variable) {
    case value1:
        // Code to execute if variable equals value1
        break;
    case value2:
        // Code to execute if variable equals value2
        break;
    default:
        // Code to execute if no case matches
        break;
}
Key components:

case: represents a possible value to match
break: exits the switch after a case executes (prevents fall-through)
default: optional case executed when no other case matches
You can combine multiple cases:

switch (day) {
    case 1:
    case 2:
    case 3:
        dayName = "Start of week";
        break;
    default:
        dayName = "Invalid day";
        break;
}
Use else to execute code when the if condition is not met:

if (age >= 18) {
    status = "Adult";
} else {
    status = "Young";
}
Use else if to check multiple conditions:

if (age < 18) {
    status = "Young";
} else if (age >= 18 && age <= 65) {
    status = "Adult";
} else {
    status = "Old";
}
You can chain multiple else if statements:

if (condition1) {
    code;
} else if (condition2) {
    code;
} else if (condition3) {
    code;
}
If statements allow us to execute code with conditions using the following syntax:

if (condition) {
    code;
    code;
    code;
}
If the condition is true, the code block inside the curly braces will be executed.

Example:

int age = 20;
string status = "Child";
if (age > 18) {
    status = "Adult";
}
age += 1;
In this example, if age is greater than 18, the status variable will be set to "Adult". The line age += 1; executes regardless of the condition.

Short-circuit evaluation means the computer stops checking conditions as soon as it knows the final answer.

With && (AND), if the first condition is false, the second won't be evaluated:

int x = 0;
int y = 5;
bool result = x != 0 && y / x > 2; // y / x > 2 is not evaluated
With || (OR), if the first condition is true, the second won't be evaluated:

bool result = (a > 0 && b < 2) || (c < -5 && d < 10);
// If a > 0 is false, then b < 2 won't be evaluated
// If the first part is false but c < -5 is also false, then d < 10 won't be evaluated
This optimization prevents unnecessary calculations and can avoid errors like division by zero.

Truth tables show the results of logical operator combinations:

AND operator (&&): Returns true only when both operands are true

a	b	a && b
false	false	false
false	true	false
true	false	false
true	true	true
OR operator (||): Returns true when either operand is true

a	b	a || b
false	false	false
false	true	true
true	false	true
true	true	true
NOT operator (!): Reverses the boolean value

a	!a
false	true
true	false
Logical operators are used to combine or modify boolean expressions:

Operator	Meaning	Example
&&	And - true if all operands are true	a && b
||	Or - true if any operand is true	a || b
!	Not - true if the operand is false	!a
Examples:

bool b1 = (5 > 3) && (1 == 1); // true - both operands are true
bool b2 = !(5 == 4) || (5 == 2); // true - first operand is true
bool b3 = !(1 == 1) || false; // false - both operands are false
bool b4 = !(3 > 4); // true - negates false to true
bool b5 = !(5 > 10 || 5 > 1); // false - negates true to false
Comparison operators are used to compare between two operands and return true or false:

Operator	Meaning	Example
==	Equal	1 == 2 returns false
!=	Not Equal	1 != 2 returns true
>	Greater Than	1 > 2 returns false
<	Lower Than	1 < 2 returns true
>=	Greater or Equal	1 >= 2 returns false
<=	Lower or Equal	1 <= 2 returns true
Example usage:

int var1 = 13;
int var2 = 12;
bool var3 = var1 != var2; // var3 will hold true
C# provides shortcut operators for self-arithmetic operations:

Operator	Shortcut
+	+=
-	-=
*	*=
/	/=
%	%=
Instead of writing:

int a = 5;
a = a + 3; // a holds 8
You can use the shortcut:

int a = 5;
a += 3; // a holds 8
Increment (++) and Decrement (--) operators can be used in two ways:

Pre-increment/decrement (++x or --x):

Operator goes BEFORE the variable
Value changes IMMEDIATELY
New value is used in the expression
int x = 5;
int y = ++x;
// x is increased to 6 first, then y becomes 6
Post-increment/decrement (x++ or x--):

Operator goes AFTER the variable
Original value is used first
Value changes AFTER the expression
int x = 5;
int y = x++;
// y becomes 5 first, then x increases to 6
Increment and decrement operators are used to increase or decrease the value of a variable by 1.

The increment operator ++ increases a variable by 1:

int count = 5;
count++; // count is now 6
The decrement operator -- decreases a variable by 1:

int value = 10;
value--; // value is now 9
The modulo operator % returns the remainder of a division:

result = dividend % divisor;
Example with integers:

result = 10 % 3; // result is 1
Common use case - checking if a number is even or odd:

Even numbers: number % 2 == 0
Odd numbers: number % 2 == 1
Modulo works with floating-point numbers too:

double result = 5.2 % 2.0; // result is 1.2
double result2 = 7.8 % 3.5; // result2 is 0.8
Arithmetic operators perform mathematical operations on values:

Operator	Operation	Example
+	Addition	3 + 2 = 5
-	Subtraction	3 - 2 = 1
*	Multiplication	3 * 2 = 6
/	Division	4 / 2 = 2
Using arithmetic operators with integers:

int a = 3;
int b = 5;
int c = a + b; // c holds 8
Using arithmetic operators with decimal numbers (double):

double x = 3.3;
double y = 4.1;
double z = x + y; // z holds 7.4
Type casting converts values from one data type to another. There are two types:

Implicit casting (automatic) - smaller to larger types:

int number = 5;
double decimal_implicit = number; // automatically becomes 5.0
Explicit casting (manual) - larger to smaller types:

double decimal_explicit = 9.7;
int number_explicit = (int) decimal_explicit;  // becomes 9 (truncated)
C# naming conventions help keep code organized and maintainable:

PascalCase: For class names, method names, and property names
MyClass, CalculateTotal, FirstName
camelCase: For local variables and method parameters
myVariable, customerName, calculateTotal
_underscorePrefix: For private fields (underscore + camelCase)
_myPrivateField, _customerAge
UPPER_CASE: For constants (uppercase with underscores)
MAX_VALUE, PI, DEFAULT_TIMEOUT
Additional tips:

Use descriptive names that clearly indicate purpose
Avoid abbreviations unless widely understood
Be consistent throughout your project
A constant is a special type of variable whose value cannot be changed once it is initialized. Use the const keyword followed by the data type and constant name:

const int MAX_VALUE = 100;
const double PI = 3.14159;
const string MESSAGE = "Hello, Coddy!";
Constants cannot be modified after initialization - attempting to change their values will result in a compilation error.

The var keyword allows you to declare variables without explicitly specifying their type. The compiler uses type inference to determine the type based on the assigned value:

var age = 30;        // inferred as int
var price = 99.99;   // inferred as double
var name = "Alice";  // inferred as string
var isActive = true; // inferred as bool
In C#, variables are strongly typed - once declared with a specific type, they can only hold values of that type.

Variable declaration examples:

int age = 25;        // Can only hold whole numbers
string str = "abc";  // Can only hold text
double total = 150.75;  // Can hold decimal numbers
char grade = 'A';    // Can hold single characters
bool isActive = false;  // Can hold true/false values
Type mismatches cause errors:

age = "defg";  // Error: can't put text in an int variable
str = 25;      // Error: can't put a number in a string variable
Valid reassignments with same type:

age = 26;      // OK: assigning a new integer
str = "Jane";  // OK: assigning a new text string
A boolean type has only 2 possible values: true or false.

To declare a boolean variable, use the keyword bool followed by the variable name:

bool variableTrue = true;
bool variableFalse = false;
The string type consists of multiple characters. To initialize a string variable, enclose the value within double quotation marks:

string s1 = "This is a string";
A char is a single character (numbers, letters, symbols, etc.)

To initialize a char variable, enclose the character in single quotation marks:

char c1 = 'h';
Variables are containers that hold data values. To initialize a variable, use the format:

variableType variableName = value;
int is used for whole numbers:

int age = 30;
int temperature = -5;
double is used for numbers with decimal points:

double price = 99.99;
double pi = 3.14159;
In C#, you must specify the variable type before the variable name (type declaration). Once declared, a variable can only hold values of that type.

In C#, code must be inside a class. The Main method is the entry point where program execution begins.

Basic C# program structure:

public class Program {
    public static void Main(string[] args) {
        System.Console.WriteLine("Hello, Coddy!");
    }
}
Each statement must end with a semicolon (;). Code blocks with curly braces {} don't need semicolons.

Comments are lines of text ignored by the compiler and used to explain code.

Single-line comments: Start with // and continue to the end of the line.

// This is a single-line comment
System.Console.WriteLine("Hello, Coddy!"); // Comment at end of line
Multi-line comments: Start with /* and end with */.

/*
   This is a multi-line comment.
   It can span multiple lines.
   All of this is ignored by the compiler.
*/
To print to the console in C# use System.Console.WriteLine():

public class Program {
    public static void Main(string[] args) {
        System.Console.WriteLine("Hello World!");
    }
}
C# is a modern, object-oriented programming language developed by Microsoft used for web, desktop, mobile, and game development.
