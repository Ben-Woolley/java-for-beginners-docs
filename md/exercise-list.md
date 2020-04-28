# Java For Beginners - Exercises

* [Topic 2 Exercises](#exercise-list-topic-2)
* [Topic 3 Exercises](#exercise-list-topic-3)

Each exercise has a 4-character code. This corresponds to a folder in the `java-for-beginners` project under `src/main/java/eca/exercises`. This folder contains the class or classes in which you can implement your solution to the exercise.
Some of the exercises even have automated tests! These are under `src/test/java/eca/exercises` in the same corresponding codes.

# Exercise List Topic 2
## Variables and Basic Operators
### \[PVAR] Printing Variables
In a `main`, define a `String`, `Integer`, and `Boolean` variable.
1. `System.out.println` (print) each of them separately.
2. Print them together in a sentence (which may or may not make sense).

### \[MAOP] Math Operations
Write a program that takes 2 integer variables `a` and `b` and prints the result of applying each of these calculations using `a` and `b`: addition, subtraction, division, multiplication, and modulus.

e.g given a = 10 and b = 2, print:
```
12
8
5
20
0
```

### \[MCMP] Math Comparisons
Write a program that takes 2 integer variables `a` and `b` and prints the result of applying each of the following comparisons using `a` and `b`: equal, greater than, less than, greater than or equal to, and less than or equal to.

e.g given a = 10 and b = 2, print:
```
false
true
false
true
false
```

### \[HINH] Hello, *Insert name here*!
Write your own "Hello, world!" program, then extend it to take a name as input from the console and say hello to the inputted name instead.

You should use `UserInputUtil` in the `eca.util` package, you will have to `import` it.

### \[VOWL] Is this character a vowel?
Write a program that determines whether a character is a vowel or not and prints the result to the console.

Your solution only needs to be correct for lower case letters. You can make use of the `.toUpperCase()` or `.toLowerCase()` methods on Strings if you want to make your program work for both. e.g. `"Test".toLowerCase()` converts "Test", to "test".

e.g. inputting "a" would result in
```
'a' is a vowel
```

inputting "b" would instead result in
```
'b' is a consonant
```

### \[LOTN] Biggest of three numbers
Write a program that determines which of 3 numbers is the largest and prints the result. You can represent these numbers as 3 variables in your solution.

e.g. for the numbers [5, 2, 6], the output should be:
```
The largest number of 5, 2, 6 is 6
```

### \[SETE] Sum is equal to Expected
Write a Java program to calculate the sum of two integers and determine if their sum is equal to a third integer.

e.g for:
* `a` = 10
* `b` = 5
* `c` = 15
The result would be `true`

### \[BILL] How much do I owe you?
Write a program to calculate the total cost of a restaurant meal. It should include:
* VAT
* Your Tip
* The amount owed per person

Print out a breakdown (i.e. pre-tax, VAT amount, and tip), the total owed, and the amount owed per person.

e.g. for a 2 person meal came to a £30 bill, with 20% VAT, plus a £5 tip would result in:
```
Subtotal: 30
VAT: 6
Tip: 5
Total: 41
Cost per person: 20.5
```

**Extension**
You don't always want to tip, add functionality to either include or not include a tip. (Similar to a card machine's "Would you like to add gratuity")

### \[OOEV] Odd Or Even
Write a Java program to accept a number and check the number is odd. You may print the result however you like.

e.g for a number a = 10 you could print `10 is even`

### \[GWNT] Guess What Number I'm Thinking
Write a program that thinks of a random number between 1 and 10.
Let the user enter a number, if it is correct print "You win!" otherwise print "You lose!".

You will need some way to get a random number within a range: 
```java
var aRandomNumberFrom1To5 = new Random().nextInt(4) + 1;
```
`Random.nextInt` generates a random Integer between 0 and the passed-in number. Adding `+ 1` bumps this up to a random number between 1 and 5.

You should also use `UserInputUtil` in the `eca.util` package, you may have to `import` it.

### \[PYCA] Pythagoras Calculation
In a `main`, define 2 `Integer` variables for the `side`s of a right-angled triangle.
Use [Pythagoras' theorem](https://en.wikipedia.org/wiki/Pythagorean_theorem) to calculate the length of the third side and print a message to the console,
such as `A right angle triangle with first side length 1 and second side length 2 has third side length 2.2360679775`.

You will have to use `Math.sqrt()` to get the square root of a value.
You may want to use `Math.pow()` to square the numbers.

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

```
1 X 2 = 2
2 X 2 = 4
...
```

### \[RPSG] Rock, Paper, Scissors
Write rock, paper scissors.
* Your can choose how to represent your input (e.g. entering "rock", "paper", "scissors", or 1, 2, 3)
* Your opponent is the program, which will choose an option at random
* Your solution must complete once either you or the program has won, **a draw must result in a rematch**.

**Extension**
The winner of your game is now based off the best-of-three.

### \[HOLG] Higher or lower game
There are several variants of this game, using playing cards, dice, etc.  
The game is played as follows:
1. The dealer rolls a dice and shows the number to the player
2. The player will guess whether the next dice roll will be higher or lower than the first roll
3. If the player guessed correctly:
   * The player earns a point
   * The second roll becomes the new "first number" and the game repeats from step 2
4. If the player guessed incorrectly, then the game is over

Implement the game according to the above rules.  
Make sure you print useful information for the user throughout.

### \[SELI] Searching Lists
Given a list of integers, find and print the largest, find and print the smallest, find and print a specified value (or null if it doesnt exist).
Do this by implementing `findMin`, `findMax`, and `contains` in `SearchingLists`.

## Advanced and Extra
### \[TUCO] Time Unit Conversion
Write a Java program to convert a number of seconds to hours, minutes and seconds.

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

## \[ANML] Animals
Create an `Animal` class. The class needs the following properties:
* A `species`
* A `numberOfLegs`
* A `noise` the animal makes

The class should also have the following methods:
* `call` - prints the animal's `noise` followed by an exclaimation mark (!)
* `facts` - prints information about the animal using its `species`, `number of legs`, and `noise`. e.g. `The Dog has 4 legs and makes a bark noise`

In a main, create 2 different animals e.g. `dog` and `bird`. For both animals, call their `call` and `facts` methods.

## \[CIRC] Circles
Create a `Circle` class. The class will have the property `radius` and must implement the following methods:
* `getArea` - which returns the area of the circle.
* `getCircumference` - which returns the circumference of (distance around) the circle

In a main, create an instance of your Circle with a radius of 5. 
Print the result of `getArea` and `getCircumference` for your circle. e.g.
```
A circle with radius 5 has an area of 78.53981633974483 and a circumference of 31.41592653589793
```

## \[HOTL] Hotels
Create a `Hotel` class. The class needs the following properties:
* A `name`
* A `pricePerNight`

The class should have the following methods:
* `hotelSummary` - which prints a summary message about the hotel using the `name` and `price`. e.g. "The hotel Corinthia costs £200 per night".
* `calculatePrice` - which takes an **argument** `numberOfNights` and calculates the total cost of the hotel over the number of nights.

Create an instance of Hotel for a hotel of your choice. Call its `hotelSummary` and print out its `calculatePrice` for 3 nights.

## \[PROD] Products
Complete the `Product` class. The class will have the properties:
* `name` of the product
* `price` of the product
* `quantity` of the product purchased
* `tax` being a percentage tax that applies to the product on purchase

To finish the class, create:
* The fields described above
* The constructor to populate those fields

Then complete the `InvoicePrinter` class by implementing `printInvoice`.
This function takes a `List<Product>` and prints a receipt to the console. The receipt must contain:
* Each item's price with and without tax
* A summary at the bottom, with at least the total *with and without tax*

You can enhance the receipt however you want after this, for example you could add:
* Running totals
* Tax percentage/amount on its own for each product
* An argument to add a percentage tip
* ...or anything else you can think of


## \[BANK] Banking
### Part 1

Finish the `BankAccount` class, it represents a person's bank account, and enables withdrawal and deposit from their balance.
It has the following properties:
* **accountHolder** - the name of the account owner as a `String`
* **balance** - the current balance as a `Double`
* **accountNumber** - the bank account number as an `Integer`

1. Implement the above properties
2. Implement a constructor for `BankAccount` which takes in a `String`, `Double`, and `Integer`, to create the bank account.
3. Implement the `deposit` method.
This method deposits money into the account.
4. Implement the `withdraw` method.
This method takes money out of the account, however:
   * The balance must not go below zero
   * Print an error message to the user if they attempt to withdraw to below zero
5. Implement `toString` to return a useful `String` representation of the account.
6. Implement `compare`, which prints comparison information of your account compared to someone else's
   * My name and balance
   * Their name and balance
   * The money difference between the accounts

### Part 2

You will now use your completed `BankAccount` to implement `AccountHolder` - a class representing the owner of the account.

An `AccountHolder` has the following properties:
* **account** - the `BankAccount` held by the account holder
* **phoneNumber** - the contact number for the account holder
* **postCode** - the post code for the account holder's home address

1. Implement the above fields in `AccountHolder`
2. Implement the constructor for `AccountHolder`, which takes in a `BankAccount`, `String`, and another `String`, to create the account holder.
3. Implement the getter methods for each property
4. Implement `deposit` and `withdraw`, using the **account's** corresponding methods
5. Implement `transfer` - which performs a bank transfer from one account to the other
   * It should not permit the transfer if the sender has insufficient funds
   * It should print an error message telling the user they have insufficient funds

# Credits
Some exercises inspired/sourced from:
* https://www.w3resource.com/java-exercises/
* https://adriann.github.io/programming_problems.html
