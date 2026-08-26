Date: 24/08/2026
Reading Input  
  

```java
//1.import the scanner to read input from user
import java.util.Scanner;

public class T03-Reading input {

	public static void main(String[] args) {

		//2.create a tool and name it scanner
		Scanner scanner = new Scanner(System.in);
		
		//3.print a command on the users screen for response
		System.out.println("Write a message: ");

//read the string written by the user, and assign it
// execution pauses at nextLine() until the user presses Enter
		String message = scanner.nextLine();

		// print the users input
		System.out.println(message);

	}
}
```

### FUNDAMENTAL OF STRINGS:
in programming instead of "text" we call it "strings" which is a shorthand for 'String of charactes' which is seen by computer as a sequence of individual characters. 

**Variables** are named containers that contain info of some specified type and have a name. Typically a variable is assigned a value during its declaration. A value saved to a variable can be used repeatedly.
```java
String msg = "How r u?";
System.out.println(msg); //right: prints "How r u?", never put quotation around variable
System.out.println("msg"); //wrong: prints "msg", this is called a string literal which is enclosed by quotation
```
### Concatenation - joining strings together 
Form multiple string literal and string variable using the + operator. We can do the below with any number of strings.

```java
public class main{
	
	public static void main(String[] args) {
		String msg1 = "I am ";
		
		System.out.println(msg1 + "Shaha");
	}
}
```
**Task**:Write a program that asks the user to write a string. When the user has given a string (that is, written some text and pressed enter), the program must print the user's string three times (you can use the `System.out.println` command multiple times).
```java
import java.util.Scanner;

public class main{

	public static void main(String[] args){
		Scanner scanner = new Scanner(System.in);
		
		System.out.println("Enter a msg which will be printed thrice: ");
		String msg = scanner.nextLine();
		
		System.out.println(msg);
		System.out.println(msg);
		System.out.println(msg);
	
	}
	
}
```
For multiple string variable they must have different names(e,g. first, second, third)

We can form more complicated text using these types. Shown below;
```java
import java.util.Scanner;

public class Program {

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.println("Write the first string:");
        String first = scanner.nextLine();
        System.out.println("Write the second string:");
        String second = scanner.nextLine();
        System.out.println("Write the third string:");
        String third = scanner.nextLine();

        System.out.println("Last string you wrote was " + third + ", which ");
        System.out.println("was preceded by " + second+ ".");
        System.out.println("The first string was " + first + ".");

        System.out.println("All together: " + first + second + third);
    }
}
```