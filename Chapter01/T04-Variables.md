# Variables | 27Aug2026 | 4:27

A variable is like a container where information of a given type can be stored. E,g. types: 
```java
public class main{
	public static void main(String[] args){
		//variable names are unique
		String text = "contains text";
		int wholeNumber = 123;
		double floatingPoint = 3.141592653;
		boolean trueOrFalse = true;

		//A variable's value can be joined to a string using the + sign
		System.out.println("Text variable: " + text);
		System.out.println("Integer variable: " + wholeNumber);
		System.out.println("Floating-point variable: " + floatingPoint);
		System.out.println("Boolean: " + trueOrFalse);
	}	
}		
```

## Changing a value assigned to a variable
In Java, you state the data type only **once** when declaring a variable. Its initial value is preserved until another value is assigned to it.
```java
public class main{
	public static void main(String[] args){
		int value = 95;
		System.out.println(value);
		
		value = 7;
		System.out.println(value);
	}
//Declaring the type second time (e.g., `int value = 3;`) causes a compiler error because Java thinks you are trying to create a duplicate variable with the same name.
}
```
At the end of the program, notice how the original value of the variable has vanished. A variable can hold only one value at a time.

## Variable's type persists
Once a variable's type has been declared, it can no longer be changed.
```java
boolean intAssignmentWillWork = false;
intAssignmentWillWork = 42; // Does not work

int value = 10;
intAssignmentWillWork = value; // Neither does this
```
However, exceptions like an integer value can be assigned to a double variable. Cause java knows how to convert an int to a double during assignment.
```java
public class main{
	public static void main(String[] args){
		double floatingPoint = 9.5;
		floatingPoint = 1; //works

		int value = 10;
		floatingPoint = value; //also works
		System.out.println(floatingPoint);
	}
}
```
But, a floating-point value can't be assigned to an integer variable. Cause it leads to a loss of info.
```java
int value = 4.2; // Does not work

double floatingPoint = 0.42;
value = floatingPoint; // Neither does this
```
## Naming Variables
Naming variables is a fundamental aspect of describing a program.
```java
double pi = 3.14;
double radius = 22.0;
double surfaceArea = a * b * b;

System.out.println(surfaceArea); //op:1519.76
```
**Rules for Naming Variables**: No Special Symbols(!), No Space, No begining with number or Only numbers, No same variable name, No commands like Sout.
USE camelCase: The first letter of a variable name is always lower-cased then capital.
```java
int camelCaseVariable = 7; // Allowed

int 7variable = 4; // Not allowed!
int variable7 = 4; // Allowed, but is not a descriptive variable name

int System.out.print = 4; // Not Allowed
int camelCase! = 5; // Not allowed [!]
```
**Reading Different Variable Types from User Input:**
In text-based programs, a user's input is always read initially as a `String` (text) because the user types it as text. To read other data types, Java requires converting the string input into the target variable type.
Here is how you read and convert each type using a `Scanner` object:
```java
String valueAsString = "42";
int value = Integer.valueOf(valueAsString);
// double value = Double.valueOf(valueAsString);
System.out.println(value);
```

```java
import java.util.Scanner;
public class Program {
	public static void main(String[] args) {
		Scanner scanner = new Scanner(System.in);
		System.out.println("Write text and press enter");
		String text = scanner.nextLine(); // Reading Strings, basic one. But to transfer follow below rule.
		// Wrap the scanner command inside Whatever.valueOf(here);
		// int text = Integer.valueOf(scanner.nextLine());
		// double text = Double.valueOf(scanner.nextLine());
		// boolean text = Boolean.valueOf(scanner.nextLine());
		System.out.println("You wrote " + text);
	}
}

//_Note: For reading Int; If a user enters a non-numerical value (like text), the program will break because it doesn't know how to convert it to a number. For reading Boolean; To get the boolean value of true, the user must type the string "true" (this is case-insensitive, so "TRUE" "TRue" also work). Any other string input by the user will be converted to false.
```
---

