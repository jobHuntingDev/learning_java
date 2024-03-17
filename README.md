# Reference material for writing java code

# First and Second year

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

System.out.println("double" +  rPrice);
```
**Double 2 decimal places:**

```java
//import java.text.DecimalFormat;
DecimalFormat df = new DecimalFormat("0.00");

double rPrice;

rPrice = 5.258374819473289147;

// Writing to 2 decimal places
System.out.println("double" +  df.format(rPrice));
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

**A property of methods:**

Funny enough it seems java methods are quite different from function in other programs in that it would seem assigned values can be carried but I'm not sure how or why this works but here's an example of it.

```java
import java.util.Random;

public class TestAssignMethods{

  public static void populateRandomInts(int[] values){
    Random randomizer = new Random();

    for(int i=0;i<values.length;i++){
      values[i] = randomizer.nextInt(100);
    }
  }

  public static void main(String[] args){
    int[] randomInts = new int[10];

    populateRandomInts(randomInts);

    for(int i=0;i<randomInts.length; i++){
      System.out.println(randomInts[i]);
    }
  }
}
```


## Methods: Character methods


A collection of methodes that can be used on char types.

### Test Characters:

**Character is digit:**

```java
char c = input.charAt(0); // get input character

// display character info
System.out.printf("is defined: %b%n", Character.isDigit(c));
```

**Character is a letter:**

```java
char c = input.charAt(0); // get input character

// display character info
System.out.printf("is part of a Java identifier: %b%n",Character.isLetter(c));
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
System.out.printf("is letter or digit: %b%n", Character.isLowerCase(c));
```

**Character is upper case:**

```java
char c = input.charAt(0); // get input character

// display character info
System.out.printf("is upper case: %b%n", Character.isUpperCase(c));
```

**Character is white space:**

```java
char c = input.charAt(0); // get input character

// display character info
System.out.printf("is upper case: %b%n", Characcter.isWhitespace(c));
```

**Character is defined:**

```java
char c = input.charAt(0); // get input character

// display character info
System.out.printf("is defined: %b%n", Character.isDefined(c));
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

### Change character:

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


## Methods: String methods


Note: strings have index values for each character, so in a sense strings are just an array of characters.

**Get String length:**

```java
int lengthOfString;
String example = "Example string";

int lengthOfString = example.length();

System.out.prinln("The length of the string is " + lengthOfString);
```

**Get character at index:**

```java
String example = "Example string";

char index3 = example.charAt(3);

System.out.prinln("The character at index 3 is " + index3);
```

**Get a string from the string:**

```java
String example = "Cut Out Hello from me";

String newString = example.substring(8,12);

System.out.prinln(newString + " World");
```

**Convert a string to upper case:**

```java
String example = "hello world";

example.toUpperCase();

System.out.println(example);
```

**Convert a string to lower case:**

```java
String example = "hello world";

example.toLowerCase();

System.out.println(example);
```

**Replace character in a string:**

```java
String example = "Vello World this is my Vouse";

example = example.replace('V','H');

System.out.println(example);

# output: Hello World this is my House
```

**Compaire two strings:**

```java
String sName1 = "John";
String sName2 = "Joanne";

if (sName1.compareTo(sName2) == 0){
  System.out.println(sName1 + " is the same as " + sName2);
}

if (sName1.compareTo(sName2) < 0){
  System.out.println(sName1 + " is smaller than " + sName2);
}

if (sName1.compareTo(sName2) > 0){
  System.out.println(sName1 + " is bigger than " + sName2);
}
```

**Equality(case sensitive):**

```java
String example1 = "Hello World";
String example2 = "hello world";

if(example1.equals(example2)){
	System.out.println("These two are exactly the same");
}
```

**Equality(Ignore case sensitive):**

```java
String example1 = "Hello World";
String example2 = "hello world";

if(example1.equalsIgnoreCase(example2)){
	System.out.println("These two say the same thing");
}
```

**Convert String to digits:**

```java
String example1 = "1234";
String example2 = "2353.23";

int iExample1 = Integer.parseInt(example1);
double rExample2 = Double.parseDouble(example2);
```


## Math Class


The math class can be found in the java.lang.Math package but it's provided automatically.

**Getting the value Pie:**

```java
double rPie = Math.PI;
```

**Rounding methods:**

Round down to the nearest integer(returns a double value)

```java
double rNumbSmallBottles = Math.floor(rLiteresContainer / rSmallContainer);
// Or
int iNumbSmallBottles = (int) Math.floor(rLiteresContainer /rSmallContainer);
```

Round up to the nearest integer(returns a double value):

```java
double rNumbSmallBottles = Math.ceil(rLiteresContainer / rSmallContainer);
// Or
int iNumbSmallBottles = Math.ceil(rLiteresContainer / rSmallContainer);
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


The random class can be used to bet a random value.

**Random Int:**

```java
import java.util.Random;

Random randomizer = new Random();

int iRandValue = randomizer.nextInt(15); // 0 <= iRandValue < 15
```

**Random Double:**

```Java
import java.util.Random;

Random randomizer = new Random();

double rValue = randomizer.nextDouble(20); // 0 <= rValue < 20
```

**Random Boolean:**

```java
import java.util.Random;

Random randomizer = new Random();

boolean bValue = randomizer.nextBoolean(20); // 0 <= rValue < 20
```


## Arrays


**Int Arrays:**

```java
int[] iCount = new int[3];

iCount[0] = 1;
iCount[1] = 2;
iCount[2] = 3;
```

**Double Arrays:**

```java
Double[] rRange = new Double[3];

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

**Perfoming a bubble sort:**

```java
// Bubble sort
    int numbCompares = unsortedArray.length - 1;

    for(int i=0; i<unsortedArray.length; i++){
      for(int j=0; j< numbCompares; j++){
        int k = j +1;

        if(unsortedArray[j] > unsortedArray[k]){
          int temp = unsortedArray[j];
          unsortedArray[j] = unsortedArray[k];
          unsortedArray[k] = temp;
        }

      }
      --numbCompares;
    }
```

**Bubble sorting String:**

```java
for(int i=0;i<names.length;i++){

    for(int j=0;j<names.length-1;j++){

	if(names[j].compareTo(names[j+1]) < 0){
            String temp = names[j];
            names[j] = names[j+1];
            names[j+1] = temp;
	}

    }

}
```


## User defined class's

How to write a concrete class.A class without a main method

```java
// An example of a concrete class

public class Politician{
 private String surname;
 private String position;
 private String politicalParty;

 public Politician(){
  surname = "SURNAME";
  position = "NOT APPOINTED YET";
  politicalParty = "MUST MAKE UP YOUR MIND";
 }
 
 public Politician(String pSurname,String pPositon,String pPoliticalParty){
  surname = pSurname;
  position = pPositon;
  politicalParty = pPoliticalParty;
 }

 public void setSurname(String pSurname){
  surname = pSurname;
 }

 public void setPosition(String pPosition){
  position = pPosition;
 }

 public  void setPoliticalParty(String pPoliticalParty){
  politicalParty = pPoliticalParty;
 }

 public String getSurname(){
  return surname;
 }

 public String getPosition(){
  return position;
 }

 public String getPolititcalParty(){
  return politicalParty;
 }

 public static boolean goodPolitician(int budget, double moneySpend){
  boolean good = false;
  
  double spending = (moneySpend/budget) * 100.0;

  if( spending < 100){
   good = true;
  }

  return good; 
 }

}
```

# Third year

## Gui: Graphical user interfaces

### JOpionPane:

Confirm dialog.

```java
import java.swing.JOptionPane;

public class Main{

	public static void main(String[] args){
		// JOptionPane.showMessageDialog(parentComponent, messageStringExpression, boxTitleString, messageType);
		JOptionPane.showMessageDialog(null, "Hallo World!", "Greetings",JOptionPane.INFORMATION_MESSAGE);
	}
}
```

Other message types:
 - Error message: JOptionPane.**ERROR_MESSAGE**
 - Error message: JOptionPane.**INFORMATION_MESSAGE**
 - Error message: JOptionPane.**PLAIN_MESSAGE**
 - Error message: JOptionPane.**QUESTION_MESSAGE**
 - Error message: JOptionPane.**WARNING_MESSAGE**

Get input.

```java
import java.swing.JOptionPane;

public class Main{

	public static void main(String[] args){
		//String variable_name = JOptionPane.showInputDialog(<Message>);

		String input = JOptionPane.showInputDialog("Enter the day of the week.");
	}
}
```

Confirmation input. give the user a question and want a yes no or cancel answer

```java
import java.swing.JOptionPane;

public class Main{

	public static void main(String[] args){
		int option = JOptionPane.showConfirmDialog(null, "Question");

		if(option == JOptionPane.YES_OPTION):
			// yes button pressed
		else if(option == JOptionPane.NO_OPTION):
			// no button pressed
		else if(option == JOptionPane.CANCEL_OPTION):
			// cancel button pressed
	}
}
```

## ArrayList

An ArrayList is a resizable array from the java.util package.

```java
import java.util.ArrayList;

public class LearnArrayList{

	public static void main(String[] args){
		// Declaring an array list named cities of type String
		ArrayList<String> cities = new ArrayList<String>();

		// Array List Methods:
		// Adding a value to the array
		cities.add("Pretoria");
		cities.add("Johannesburg");
		cities.add("Durban");
		System.out.println(cities);

		// Get a specific value (the first value)
		System.out.println(cities.get(0));

		// Change a specific value
		cities.set(0,"Durban");	
		System.out.println(cities);

		// Remove a value
		cities.remove(0);
		System.out.println(cities);

		// Get the number of items in the array
		System.out.println(cities.size());

		// Empty out the array
		cities.clear();
		System.out.println(cities);
	}
}
```

Looping through an arraylist using the java for-each loop.

```java
import java.util.ArrayList;

public class LearnArrayList{

	public static void main(String[] args){
			
		ArrayList<String> cities = new ArrayList<String>();

		cities.add("Pretoria");
		cities.add("Johannesburg");
		cities.add("Durban");

		// java for-each loop
		for(String i : cities){
			System.out.println(i);
		}
	}
}
```
