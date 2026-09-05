## Reading User Input
```java
// Making the scanner available in the program
import java.util.Scanner;

public class Program {
    public static void main(String[] main) {
        // Creating the scanner
        Scanner reader = new Scanner(System.in);

        // Examples of reading different types of user input
        String text = reader.nextLine();
        int number = Integer.valueOf(reader.nextLine());
        double numberWithDecimals = Double.valueOf(reader.nextLine());
        boolean trueOrFalse = Boolean.valueOf(reader.nextLine());

    }
}
```

## Calculating
**3 simple steps for any calculation:**
1. **Inputs** – make variables for the values you need
2. **Calculate** – do the math, save it in a result variable
3. **Use it** – print the result (or use it in another calculation)
Example: Product, with user input
```java
import java.util.Scanner;

public class Program {
    public static void main(String[] args) {
        Scanner reader = new Scanner(System.in);

        int first = Integer.valueOf(reader.nextLine());   // step 1: get input
        int second = Integer.valueOf(reader.nextLine());

        int product = first * second;   // step 2: calculate

        System.out.println("Product: " + product);   // step 3: show result
    }
}
```

**Task**: Squared: Write a program that reads an integer from the user and prints the square of the given integer, i.e. the integer multiplied by itself.
```java
import java.util.Scanner;
public class main{
	public static void main(String[] args){
		Scanner sc = new Scanner(System.in);
		System.out.println("Enter a number: ");
		int number = Integer.valueOf(sc.nextLine());
		int squared = number * number;
		
		System.out.println("Square of the number you gave is " + squared );
	}
}
```

## Conditional Logic
- **`if`** → runs code when a condition is **true**.
- **`else if`** → checks another condition if the previous one is false.
- **`else`** → runs when **all conditions are false**.
- Conditions evaluate to **true or false**.
```java
...
if (value > 5) {
    // if true
} else if (value < 0) {
    // if second condition is true
} else {
    // otherwise
}
```
**Key point:** Conditions are checked **from top to bottom**, and only the **first true** block runs.

**Task**: Comparing Numbers: Write a program that reads two integers from the user. If the first number is greater than the second, the program prints "(first) is greater than (second)." If the first number is less than the second, the program prints "(first) is smaller than (second)." Otherwise, the program prints "(first) is equal to (second)." The (first) and (second) should always be replaced with the actual numbers that were provided by the user.
```java
import java.util.Scanner;
public class ComparingNumbers{
	public static void main(String[] args){
		Scanner sc = new Scanner(System.in);
		
		System.out.println("Enter first number: ");
		int first = Integer.valueOf(sc.nextLine());
		System.out.println("Enter second number: ");
		int second = Integer.valueOf(sc.nextLine());
		
		if(first>second){
			System.out.println(first+" is greater than "+second);
		} else if(first<second){
			System.out.println(first+" is less than "+second);
		} else {
			System.out.println(first+" is equal to "+second);
		}
	
	}		
}		
```

---

