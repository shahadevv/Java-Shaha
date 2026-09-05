# Calculating With Numbers | 28Aug2026 | 9:00pm

Basic athematical operations: + - * /
```java
int first = 2;
System.out.println(first); // prints 2
int second = 4;
System.out.println(second); // prints 4

int sum = first + second; // The sum of the values
System.out.println(sum); // prints 6
```
## Precedence and parentheses
- Opearations within parentheses are performed before those outside them.

**Task**: Seconds in a day(ask the user for the number of days)
```java
import java.util.Scanner;
public class main{
	public static void main(String[] args){
		Scanner scanner = new Scanner(System.in);
		
		System.out.println("Enter the number of days: ");
		int number = Integer.valueOf(scanner.nextLine());
		
		System.out.println("You gave " + number);
		
		int dayInSeconds = number * 24 * 60 * 60;
		System.out.println("Your day in seconds is: " + dayInSeconds);
	
	}
}
```
## Calculating and Printing
```java
System.out.println("here is an integer --> " + 2); //op; here is an integer —> 2
System.out.println("Four: " + (2 + 2)); // op; Four: 4
```

**Task**: Sum of three numbers
```java
import java.util.Scanner;
public class Shaha{
	public static void main(String[] args){
	Scanner sc = new Scanner(System.in);
	
	System.out.println("Enter first number: ");
	int first = Integer.valueOf(sc.nextLine());
	System.out.println("Enter second number: ");
	int second = Integer.valueOf(sc.nextLine());
	System.out.println("Enter third number: ");
	int third = Integer.valueOf(sc.nextLine());
	
	int sum = first + second + third;
	
	System.out.println("The sum of the three numbers is " + sum);
	}
} //STOP FORGETING THE () IN SCANNER
```
Substraction and Multiplication are also the same.

**Division**: If you divide two integers, the result is also an integer, so any decimal part is removed. Example: `5 / 2 = 2` (not `2.5`).
```java
int first = 3;
int second = 2;
double result = first / second;
System.out.println(result); // op 1 
// division of two integers always produces an integer.


double whenDividendIsFloat = 3.0 / 2;
System.out.println(whenDividendIsFloat); // op 1.5
double whenDivisorIsFloat = 3 / 2.0;
System.out.println(whenDivisorIsFloat); // op 1.5
// If the dividend or divisor (or both) of the division is a floating point number, the result is a floating point number as well.


int first = 3;
int second = 2;

double result1 = (double) first / second;
System.out.println(result1); // op 1.5
double result2 = first / (double) second;
System.out.println(result2); // op 1.5
double result3 = (double) (first / second);
System.out.println(result3); // op 1.0
//An integer can be converted into a floating point number by placing a type-casting operation `(double)` before it.


int integer = (int) 3.0 / 2; // floating number got changed to integer-type variable.
System.out.println(integer); // op 1


int dividend = 3;
int divisor = 2;

double result = 1.0 * dividend / divisor;
System.out.println(result); // op 1.5
// the dividend chngd into a floating-point nmbr prior to xcuting the division. if the 1.0 was performed last after the division the op would have been 1.0 instead of 1.5.
```

---
