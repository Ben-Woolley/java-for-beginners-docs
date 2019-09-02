# Java For Beginners - Exercises

* [Topic 2 Exercises](#exercise-list-topic-2)
* [Topic 3 Exercises](#exercise-list-topic-3)

# Exercise List Topic 2

This exercise list is to practice the content presented in [lecture 2](../lessons/lesson2)

## \[VABO] Variables and Basic Operators
### Printing Variables
In a `main`, define a `String`, `Integer`, and `Boolean` variable.
1. `System.out.println` (print) each of them separately.
2. Print them together in a sentence (which may or may not make sense).

### \[MAOP] Math Operations
Write a program that takes 2 integer variables `a` and `b` and prints the result of applying each of these calculations using `a` and `b`: addition, subtraction, division, multiplication, and modulus.

e.g given a = 10 and b = 2, print:

```java
//print 12 (a+b)
//print 8 (a-b)
//etc
```

### \[MCMP] Math Comparisons
Write a program that takes 2 integer variables `a` and `b` and prints the result of applying each of the following comparisons using `a` and `b`: equal, greater than, less than, greater than or equal to, and less than or equal to.

e.g given a = 10 and b = 2, print:
```java
a equals b // false
a > b // true
a < b // false
```

### \[HINH] Hello, *Insert name here*!
Write your own "Hello, world!" program, then extend it to take a name as input from the console and say hello to the inputted name instead.

You should use `UserInputUtil` in the `eca.util` package, you will have to `import` it.

### \[OOEV] OddOrEven
Write a Java program to accept a number and check the number is even or not. Output the `Boolean` value of the result

e.g for a number a = 10 print `true`

### \[SETE] Sum is equal to Expected
Write a Java program to calculate the sum of two integers and return true if the sum is equal to a third integer

e.g for:
```java
a = 10
b = 5
c = 15
print true (a + b = c)
```

### \[GWNT] Guess What Number I'm Thinking
Write a program that thinks of a random number between 1 and 10.
Let the user enter a number, if it is correct print "You win!" otherwise print "You lose!".

You will need some way to get a random number within a range, [java has many ways and developers are still arguing over which are the best](https://stackoverflow.com/questions/363681/how-do-i-generate-random-integers-within-a-specific-range-in-java).
`new Random().nextInt(*your upper bound*)` is the shortest (but not necessarily the best) way to get a random Integer.

You should also use `UserInputUtil` in the `eca.util` package, you will have to `import` it.

### \[PYCA] Pythagoras Calculation
In a `main`, define 2 `Integer` variables for the `side`s of a right-angled triangle.
Use [Pythagoras' theorem](https://en.wikipedia.org/wiki/Pythagorean_theorem) to calculate the length of the third side and print a message to the console,
such as `A right angle triangle with first side length 1 and second side length 2 has third side length 2.2360679775`.

You will have to use `Math.sqrt()` to get the square root of a value.
This must be **imported** (pulled in from Java) to use, which is done by adding `import java.util.Math;` to the top of your Java file (below the `package`).

### \[BACA] Basic Calculator
Create a program that takes 3 inputs (using `UserInputUtil` again) individually:
* A first number
* A second number
* A **mathematical operator** as a `String`

Pretty-print the mathematical calculation requested, and then the result.

e.g. an input of:
```
1
2
+
```
would result in printing `1 + 2 = 3`

**Bonus** - if the operator entered is not supported, print `Unsupported operator *operator*`.

## Lists and Loops
### \[PRLI] Printing Lists
Make a `List` of the names of your favourite foods (in order of most to least favourite). With this list:
1. Print them out on a line each.
2. Then use it in a sentence e.g. `If I could, I would eat ice cream for every meal`.
3. Then add the rank of each food to the beginning of each line e.g. `1) If I could...`.

### \[NTTA] N Times Table
Write a program that prints out the `n` times table in a pretty format e.g

```java
1 X 2 = 2
2 X 2 = 4
...
```

### \[SELI] Searching Lists
Given a list of integers, find and print the largest, find and print the smallest, find and print a specified value (or null if it doesnt exist)

e.g given the following list of integers `[1,2,3,4,5]` and a specified value m = 3 print:
```java
Min: 1
Max: 3
M: 3
```

## Advanced and Extra
### \[TUCO] Time Unit Conversion
Write a Java program to convert a number of seconds to hours, minutes and seconds.

### \[SWAV] Swap Variable Values
Write a program that swaps the values of two variables.

___Hint___: Easy read integer:
```java
public Integer readInteger() {
	Integer someInput = Integer.parseInt(new Scanner(System.in).nextLine());
	return someInput;
}
```

### \[PDTI] Pretty Date/Time
Use `LocalDate` and `LocalTime` to retrieve information about the current date/time. Print out some of their information in a useful way to you (e.g. "Today is 19 October 2018 and the time is 10:30")

You will need to *import* these 2 Classes:

```java
import java.time.LocalDate;
import java.time.LocalTime;
```

### \[SOFD] Sum Of Digits
Write a Java program and compute the sum of the digits of an integer.

e.g for a number a = 1234, print: `10` (1 + 2 + 3 + 4)

___Hint___: You will need to make use of `.toString()`, and `.split()` on a `String`

# Exercise List Topic 3

This is the exercise list for [lesson 3](../lessons/lesson3) - __Classes and Methods__

## \[CIRC] Circles
### Exercise 1
Create a `Circle` class. The class will have the property `diameter` and must implement the following methods:
* `getArea` - which returns the area of the circle.
* `getCircumference` - which returns the circumference of (distance around) the circle

### Exercise 2
Create a `Product` class. The class will have the properties:
* `name` of the product
* `price` of the product
* `quantity` of the product purchased
* `tax` being a percentage tax that applies to the product on purchase

Then create a `InvoicePrinter` class with a function called `printInvoice` function.
This function will take a `List<Product>` and print a receipt to the console. The receipt must contain:
* Each item's price with and without tax
* A summary at the bottom, with at least the total *with and without tax*

You can enhance the receipt however you want after this, for example you could add:
* Running totals
* Tax percentage/amount on its own for each product
* An argument to add a percentage tip
* ...or anything else you can think of


## \[BANK] Banking
### Exericse 1

* The `Java class` called `BankAccount` is started below. An object of type `BankAccount` represents the basics of a commercial account, it has the following instance variables to hold data:
   - __AccountHolder__ : String -> represents the name of the person who owns the bank account.
   - __Balance__ : Integer -> represents the current balance of the account as an integer (i.e no decimals)
   - __AccountNo__ : String -> represents the number of the account

```java
public class BankAccount {

  private String accountHolder;
  private Integer balance;
  private String accountNumber;

// rest of code goes here

}
```

a) Write a constructor for the class `BankAccount` which takes in two strings and an integer as arguments (for accountHolder, accountNumber and balance, respectively) and instantiates the instance variables to those values.

b) For the following function, based on the method's signature and name, implement its functionality:

```java

public void deposit(Integer amount) {
 // implement deposit function

}

```

c) Write a method called `toString` that returns the details of the bank account as a string, i.e the name of the account holder, name of the bank account and balance


d) Using the following getter methods, create another method that takes a bank account as an argument, and compares two bank accounts. The method should return the name and bank account number of the account with a higher balance

```java

public String getBalance() {
  return this.balance;
}

public String getHolderName() {
  return this.accountHolder;
}

public String getAccNumber() {
  return this.accountNumber;
}

// signature of compare method:
public String compareAccounts(BankAccount compareAccount);

```

e) Test your methods by instantiating two bank accounts in a class with a main method.


### Exercise 2

 Using the class and methods from above, create a class called `AccountHolder`. Your AccountHolder should:

* Have a bank account
* Have a name and contact details (Address/Phone Number etc)
* Have getter and setter methods for all fields
* Have methods used to withdraw and deposit. Note: withdrawal should not be possible if the bank account's balance falls below 0.
* Have a transfer method that takes in an AccountHolder object as an argument and an integer representing the sum to be transfered. That sum will be removed from the "source" account and added to the "destination" account (i.e the account holder who calls the method transfers to the one in the argument). E.g

```java
AccountHolder bob = new AccountHolder(); // assume Bob has $100 in his BankAccount object
AccountHolder alice = new AccountHolder(); // assume Alice has $200 in her BankAccount object
bob.transfer(alice, 100);
bob.getAccountBalance(); // would return $0
alice.getAccountBalance(); // would return $300

// think about constraints accordingly, such as using the transfer method when your bank account is negative.
```


Change the code accordingly in the BankAccount class to reflect your AccountHolder implementation.

* In the `HomeWorkMain.java` class, create two instances of an AccountHolder. Using the two instances you should successfully:
    - be able to get the balance of both account holders' accounts;
    - be able to use the withdraw method on both;
    - be able to use the deposit method on both and get the account balances;
    - be able to transfer money from one account holder to another;

### Tests

The folder `intro-to-java/test/eca/lessons/lesson3/` contains the tests for this exercise. To make sure you get the correct output and your program works as expected, you should run the tests for each exercise in order (`BankAccountTest`, `AccountHolderTest` and then `HomeWorkMainTest`)



# Credits
Some exercises inspired/sourced from:
* https://www.w3resource.com/java-exercises/
* https://adriann.github.io/programming_problems.html
