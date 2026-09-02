# Conditional statements and conditional operation | 30Aug2026 | 6:30 pm

To branch the execution of a program based on user input, we gotta use **Conditional Statement**.
## if
A conditional statement uses **if** to check a condition.
- The condition is written inside ( ) and gives true or false.
- The code inside { } runs only if the condition is true.
- Example: if (true) { statement; } → the statement runs.
```java
int number = 11;
if (number > 10) {
    System.out.println("The number was greater than 10");
} 
// `if` statement does not end with a semicolon (;) because the statement includes the whole block.
```

**Task**: Speeding Ticket { Write a program that asks the user for an integer and prints the string "Speeding ticket!" if the input is greater than 120 }
```java
import java.util.Scanner;
public class main{
	public static void main(String[] args){
		Scanner sc = new Scanner(System.in);
		System.out.println("Give speed: ");
		int speed = Integer.valueOf(sc.nextLine());
		
		System.out.println(speed);
		if(speed > 120){
		System.out.println("Speeding ticket!");
		}
	}
}
```
### Code Indentation and Blocks
- A **code block** is code inside `{ }`.
- Every `{` must have a matching `}`.
- `public class` and `main()` each create a block.
- An `if` statement also creates a block.
- Code inside a block is **indented** (usually 4 spaces) to make it easier to read.
- When the block ends with `}`, the indentation returns to the previous level.
- Blocks organize the **structure and readability** of a program.
```java
if (number > 10) {
number = 9; // incorrectly indented
}

if (number > 10) {
    number = 9; // correctly indented
}
```

### Comparison Operators
- `>` greater than
- `>=` greater than or equal to
- `<` less than
- `<=` less than or equal to
-  ==  equal to
- `!=` not equal to
**Task**: Orwell; Write a program that prompts the user for an integer and prints the string "Orwell" if the number is exactly 1984.
**Task**: Ancient; Write a program that prompts the user for a year. If the user inputs a number that is smaller than 2015, then the program prints the string "Ancient history!".

## else
- `else` gives an **alternative action** when the `if` condition is **false**.
- If the condition is **true**, the `if` block runs.
- If the condition is **false**, the `else` block runs.
- `else` comes literally after the `if` block’s closing `}`.
```java
int age = 20;

if (age >= 18) {
    System.out.println("Adult");
} else {
    System.out.println("Not an adult");
}
```

**Task**: Positivity; Write a program that prompts the user for an integer and informs the user whether or not it is positive (greater than zero).
```java
import java.util.Scanner;
public class main{
	public static void main(String[] args) {
		Scanner sc = new Scanner(System.in);
		System.out.println("Give a number: ");
		
		int number = Integer.valueOf(sc.nextLine());
		
		if (number > 0){
		System.out.println("The number is positive.");
		} else {
		System.out.println("The number is negative.");
		}
	}
}
```

**Task**: Adulthood; Write a program that prompts the user for their age and tells them whether or not they are an adult (18 years old or older).

## else if
- `else if` is used when you have **multiple conditions** to check.
- The program checks conditions **from top to bottom**.
- The first condition that is **true** is executed.
- If none are true, the `else` block runs.
```java
int age = 7;

if (age < 0) {
    System.out.println("Not borned yet");
} else if (age < 13) {
    System.out.println("Child");
} else if (number < 18) {
    System.out.println("Teenager");
} else {
    System.out.println("Adult");
}
```

**Task**: Larger Than or Equal To ; Write a program that prompts the user for two integers and prints the larger of the two. If the numbers are the same, then the program informs us about this as well.
```java
import java.util.Scanner;
public class Main{
	public static void main(String[] args){
		Scanner sc = new Scanner(System.in);
		
		System.out.println("Give first number: ");
		int number1 = Integer.valueOf(sc.nextLine());
		System.out.println("Give Second number: ");
		int number2 = Integer.valueOf(sc.nextLine());
		
		if(number1 > number2) {
			System.out.println("Greater number is: " + number1);
		} else if(number2 > number1) {
			System.out.println("Greater number is: " + number2);
		} else {
			System.out.println("The numbers are equal!");
		}
	}
}
```

**Task**: Grades and Points ; 
![[Screenshot 2026-08-30 at 7.57.12 PM.png]]

## Conditional Statement Expression and the Boolean Variable
- A conditional statement needs an expression that results in **`true` or `false`**.
- A **boolean variable** stores either `true` or `false`.
- The boolean variable can be used directly in an `if` statement.
```java
boolean isRaining = true;
if (isRaining) { 
	System.out.println("Take an umbrella.");
}

// Comparison operators like `<` and `>` also produce boolean values.
int first = 1;
int second = 3;
boolean isLessThan = first < second;

if (isLessThan) {
	System.out.println("1 is less than 3!");
} // isLessThan true so msg gets printed
```

## Remainder
**Modulo Operator** `%` : The modulo operator `%` gives the remainder after division.
```java
int remainder = 7 % 2;
System.out.println(remainder); // op 1
System.out.println(5 % 3); // op 2
System.out.println(7 % 4); // op 3
System.out.println(8 % 4); // op 0
System.out.println(1 % 2); // op 1


// To check if a number is divisible by 400, use `%` and check if the remainder is 0
Scanner sc = new Scanner(System.in);

int number = Integer.valueOf(sc.nextLine());
int remainder = number % 400;

if (remainder == 0) { // if (number % 400 == 0){ -->skip above line using this as it can be part of expression.
    System.out.println("The number " + number + " is divisible by four hundred.");
} else {
    System.out.println("The number " + number + " is not divisible by four hundred.");
}
```

**Task**: Odd or even; Write a program that prompts the user for a number and informs us whether it is even or odd.
```java
import java.util.Scanner;
public class main{
	public static void main(String[] args){
		Scanner sc = new Scanner(System.in);
		
		System.out.println("Enter a number: ");
		int number = Integer.valueOf(sc.nextLine());
		
		if (number % 2 == 0){
			System.out.println("Number " + number + " is even.");
		} else {
			System.out.println("Number is odd.");
		}
	}
}
```

## Conditional Statements and Comparing Strings
- For **numbers** (`int`, `double`) and **boolean**, use == to compare values.
- For **Strings**, do NOT use ==  to check if their contents are equal.
- Use the **`.equals()`** method instead:
```java
import java.util.Scanner;
public class main{
	public static void main(String[] args){
		Scanner sc = new Scanner(System.in);

		System.out.println("Input two strings");
		String first = sc.nextLine();
		String second = sc.nextLine();
//If comparing two String variables, put the variable name inside `equals()`
		if (first.equals(second)) {
		    System.out.println("The strings were the same!");
		} else {
		    System.out.println("The strings were different!");
		}
//If comparing with a fixed String, put the text in qutoation marks:
		if (first.equals("two strings")) {
		    System.out.println("Clever!");
		}

		if (second.equals("two strings")) {
		    System.out.println("Sneaky!");
		}
	}
}
```

**Task**: Password: Write a program that prompts the user for a password. If the password is "Caput Draconis" the program prints "Welcome!". Otherwise, the program prints "Off with you!"
**Task**: Same: Write a program that prompts the user for two strings. If the strings are the same, then the program prints "Same". Otherwise, it prints "Different".

## Logical Operators
Logical operator are used to **combine or change conditions** in **if** statements.
- AND `&&` → `true` only if **both conditions are true**.
```java
if (number >= 5 && number <= 10) {Stmt}
//Means: number must be 5 or more AND 10 or less.
```
- OR `||` → `true` if **at least one condition is true** (or both).
```java
if (number < 0 || number > 100) {Stmt}
//Means: number is less than 0 or greater than 100.
```
- NOT `!` → **reverses** a boolean result: `true → false`, `false → true`.
```java
if (!(number > 4)) {Stmt}
//Means: number is NOT greater than 4.
```

**Task**: Checking the age: Write a program that prompts the user to input their age and checks whether or not it is possible(at least 0 and at most 120). Only use a single if-command in your program.
```java
import java.util.Scanner;
public class main{
	public static void main(String[] args){
		Scanner sc = new Scanner(System.in);
		
		System.out.println("How old are you? ");
		int age = Integer.valueOf(sc.nextLine());
		
		if(age>=0 && age<=120){
			System.out.println("OK");
		} else {
			System.out.println("Impossible!");
		}
	}
}
```

## Execution Order of Conditional Statements
- In an `if - else if - else` statement, conditions are checked **from top to bottom**.
- Once the program finds the **first true condition**, it executes that block and **stops checking the remaining conditions**.
- Therefore, the **most specific/demanding condition should come first**, followed by simpler conditions.
```java
import java.util.Scanner;
public class main{
	public static void main(String[] args){
		Scanner sc = new Scanner(System.in);

		int number = Integer.valueOf(sc.nextLine());

		if (number % 3 == 0 && number % 5 == 0) {
		    System.out.println("FizzBuzz");
		} else if (number % 3 == 0) {
		    System.out.println("Fizz");
		} else if (number % 5 == 0) {
		    System.out.println("Buzz");
		} else {
		    System.out.println(number);
		}
	} 
} //Key rule: In `if-else if-else`, order matters a lot so put more specific conditions before more general conditions.
```

**Task**: Leap year: A year is a leap year if it is divisible by 4. However, if the year is divisible by 100, then it is a leap year only when it is also divisible by 400.
Write a program that reads a year from the user, and checks whether or not it is a leap year.
**Task**: Gift tax: [https://www.vero.fi/en/individuals/property/gifts/](https://www.vero.fi/en/individuals/property/gifts/): A gift is a transfer of property to another person against no compensation or payment. If the total value of the gifts you receive from the same donor in the course of 3 years is €5,000 or more, you must pay gift tax.
When a gift is given by a close relative or a family member, the amount of gift tax is determined by the following table (source [vero.fi](https://www.vero.fi/en/individuals/property/gifts/gift-tax-calculator/#gifttaxtables)):![[Screenshot 2026-09-02 at 6.27.41 PM.png]]

---

