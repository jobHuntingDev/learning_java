# Reference material for writing java code

## Data types

**Interger:**

```java
int iAge;

iAge = 5;
```

**Long:**

```java
long lCount;

lCount = 1234235153143215231431;
```

**Double:**

```java
double rPrice;

rPrice = 5.258374819473289147;

// Writing to 2 decimal places
System.out.format("double : %.2f", rPrice);
```

**Char:**

```java
char cGender;

cGender = 'M';
```

***String:***

```java
String sName;

sName = "Brian";
```

## Basic AgeGreeter.java file

```java
public class AgeGreeter{

	public static void main(String[] args){
	 System.out.println("Hello world");	
	}
}
```

## Get input from the user

```java
import java.util.Scanner;

public class PrintInput{

	public static void main(String[] args){
	  // Declaring varables
	  Scanner keyboard  = new Scanner(System.in);
	  String sInput;

	// Get input from user and print it out:
	Input = keyboard.nextLine(); 
	}
}
```
### Reading different types:
- String(multple words): keyboard.nextLine();
- String(single word): keyboard.next(); 
- Int: keyboard.nextInt();
- Double: keyboard.nextDouble();
- Char: keyboard.next().charAt(0);

## Conditionals(Selection control structures)

**If statements:**

```java
 if(iAge >= 18){
  System.out.println("What can I do for you?"); 
 }
 else if(iAge >= 15){
  Sytem.out.println("What do yo want kid?");
 }
 else{
  System.out.println("What do you want brat?");
 }
```
**Comparing data types**
- Int: (iValue >= 12)
- double: (rValue == 2.3)
- Char: (cInput == 'h')
- Strings: sName1.compareTo(sName2) / sName1.compareToIgnoreCase(sName2)
	- equal: (sName1.compareTo(sName2) == 0)
	- 1 > 2(alphabeticaly): (sName1.compareTo(sName2) > 0)
	- 1 < 2(alphabeticaly): (sName1.compareTo(sName2) < 0)
- Strings (another): sName1.equals(sName2) / sName.equalsIgnoreCase(sName2)
	- equal: (sName1.equals(sName2) == true)

**Switch case:**

```java
switch(code){
	case 's':
	case 'S':
		status = "Single";
		break;
	case 'm':
	case 'M':
		status = "Married";
	default:
		status = "Invalid code";
}
```

## Loops(Iteration control structures)

**While loops:**

```java
while (cAnswer == 'Y'){
 System.out.println("This is a while loop");
}
```

**Do while loops:**

```java
do
{
 System.out.println("This is a do while loop");
}while (cAnswer == 'Y');
```

**for loops:**

```java
for (iCounter = 1; iCounter <= iHowmany; iCounter ++){
 System.out.println("This is a for loop");
}
```

## Methods: Static Methods

**Value returning methods:**

```java
public static double CelcToFahr(double rCelc){
 double rFahr;
 rFahr = rCelc * (9 / 5.0) + 32;
 return rFahr;
}
``` 

**Void methods:**

```java
public static void checkAge(int iAge){
 if (iAge < 18){
  System.out.println("You can't register , you are not old enough!");
 }
 else{
  System.out.println("You can register!");
}
}
```

**Overload methods:**

Writing more than one method with the same name, when you want to solve the same problem but with different data types.The return type and input type will determine which method is used.

```java
public class MethodOverload{

	// test overloaded square methods
	public static void main(String[] args){
		System.out.printf("Square of integer 7 is %d%n", square(7));
		System.out.printf("Square of double 7.5 is %f%n", square(7.5));
	}

	// square method with int argument
	public static int square(int intValue){
		System.out.printf("%nCalled square with int argument: %d%n",intValue);
		return intValue * intValue;
	}

	// square method with double argument
	public static double square(double doubleValue){
		System.out.printf("%nCalled square with double argument: %f%n",doubleValue);
		return doubleValue * doubleValue;
	}
}
```

## Methods: Character methods

A collection of methodes that can be used on char types.

**Character is defined:**

```java
char c = input.charAt(0); // get input character

// display character info
System.out.printf("is defined: %b%n", Character.isDefined(c));
```

**Character is digit:**

```java
char c = input.charAt(0); // get input character

// display character info
System.out.printf("is defined: %b%n", Character.isDigit(c));
```

**Character is first character in a java identifier:**

```java
char c = input.charAt(0); // get input character

// display character info
System.out.printf("is first character in a Java identifier: %b%n",Character.isJavaIdentifierStart(c));
```

**Character is part of a Java identifier:**

```java
char c = input.charAt(0); // get input character

// display character info
System.out.printf("is part of a Java identifier: %b%n",Character.isJavaIdentifierPart(c));
```

**Character is a letter:**

```java
char c = input.charAt(0); // get input character

// display character info
System.out.printf("is part of a Java identifier: %b%n",Character.isJavaIdentifierPart(c));
```

**Character is letter or digit:**

```java
char c = input.charAt(0); // get input character

// display character info
System.out.printf("is letter or digit: %b%n", Character.isLetterOrDigit(c));
```

**Character is lower case:**

```java
char c = input.charAt(0); // get input character

// display character info
System.out.printf("is letter or digit: %b%n", Character.isLetterOrDigit(c));
```

**Character is upper case:**

```java
char c = input.charAt(0); // get input character

// display character info
System.out.printf("is upper case: %b%n", Character.isUpperCase(c));
```

**Character to upper case:**

```java
char c = input.charAt(0); // get input character

// display character info
System.out.printf("to upper case: %s%n", Character.toUpperCase(c));
```

**Character to lower case:**

```java
char c = input.charAt(0); // get input character

// display character info
System.out.printf("to lower case: %s%n", Character.toLowerCase(c));
```

**Converting digit to character:**

```java
// convert digit to character
System.out.println("Enter a digit:");
int digit = scanner.nextInt();

System.out.printf("Convert digit to character: %s%n",Character.forDigit(digit, radix));
```

**Converting character to digit:**

```java
// convert character to digit
System.out.println("Enter a character:");
char character = scanner.next().charAt(0);

System.out.printf("Convert character to digit: %s%n",Character.digit(character, radix));
```

## Math Class

The math class can be found in the java.lang.Math package but it's provided automatically.

**Getting the value Pie:**

```java
doube rPie = Math.PI;
```

**Rounding methods:**

Round down to the nearest integer(returns a double value)

```java
rNumbSmallBottles = Math.floor(rLiteresContainer / rSmallContainer);
// Or
iNumbSmallBottles = (int) Math.floor(rLiteresContainer / rSmallContainer);
```

Round up to the nearest integer(returns a double value):

```java
rNumbSmallBottles = Math.ceil(rLiteresContainer / rSmallContainer);
// Or
iNumbSmallBottles = Math.ceil(rLiteresContainer / rSmallContainer);
```

Simply just round off:

```java
int iValue1 = Math.round(4.6f); //returns the value 4
long iValue2 = Math.round(12.5; //returns the value 13
```

**Exponent methods:**

Calculate the square root of a value:

```java
double rRoot = Math.sqrt(25); //return the value 5.0
```

Calculate exponential equations

```java
double rExp = Math.pow(4.2, 2); // returns the value 17.64 = (4.2)^2
```

**Random method:**

Return a pseudo-random number of data type double within a range:

```java
double x = Math.random(); // 0 <= x < 1.0
double x = Math.random() * 25; // 0 <= x < 25.0
double x = 7 + Math.random() * 58; // 7 <= x < 65.0
```

## Random Class

import java.util.Random;

The random class can be used to bet a random value.

**Random Int:**

```java
Random randomizer = new Random();

int iRandValue = randomizer.nextInt(15); // 0 <= iRandValue < 15
```

## Arrays

**Int Arrays:**

```java
new Int[] iCount = new Int[3];

iCount[0] = 1;
iCount[1] = 2;
iCount[2] = 3;
```

**Double Arrays:**

```java
new Double[] rRange = new Double[3];

rRange[0] = 1.20;
rRange[1] = 2.40;
rRange[2] = 3.35;
```

**Book Object Arrays:**

```java

Book[] shelf1 = new Book[2]

shelf[0] = new Book();
shelf[1] = new Book();

shelf[0].title = "Moby Dick";
shelf[0].author = "Herman Melville";

shelf[1].title = "The Fellowship of the ring";
shelf[1].author = "J.R.R Tolkien";
```
