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

rPrice = 5.25;
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

## Conditionals

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
