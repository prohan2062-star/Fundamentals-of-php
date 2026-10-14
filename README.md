PHP Web Development — Complete Notes
Subject: PHP Programming | Language: English | Level: Beginner

Module 1: Introduction to PHP (10 Hours)
1. Introduction to PHP
Definition: PHP stands for PHP: Hypertext Preprocessor. It is an open-source, server-side scripting language used to develop dynamic websites and web applications.
Uses of PHP:
1. Developing dynamic websites.
2. Creating login and registration systems.
3. Connecting websites to databases.
4. Processing HTML form data.
5. Developing e-commerce websites.
2. Client-Side vs Server-Side Scripting
Client-Side Scripting	Server-Side Scripting
Executes mainly in the user's browser.	Executes on the web server.
Used for user interface and interactions.	Used for business logic and database operations.
Example: JavaScript	Example: PHP
Code runs on the client device.	Code runs on the server.
3. Installation and Configuration
PHP can be installed and executed using local server environments.
- XAMPP: A development package containing Apache, MariaDB, PHP, and other tools.
- WAMP: A Windows-based web development environment.
- LAMP: A web development environment consisting of Linux, Apache, MySQL/MariaDB, and PHP.
Steps to run PHP using XAMPP:
1. Download and install XAMPP from Apache Friends.
2. Open the XAMPP Control Panel.
3. Start the Apache server.
4. Create a folder named php-course inside C:\xampp\htdocs\.
5. Create a file named index.php inside that folder.
6. Open the following URL in your browser:
http://localhost/php-course/


4. Writing and Executing a Simple PHP Script
Example:
<?php
echo "Hello World!";
?>


Output:
Hello World!


Explanation:
- <?php starts the PHP code.
- echo displays output.
- "Hello World!" is a string.
- ; terminates the statement.
- ?> closes the PHP block.
5. PHP Syntax
PHP syntax refers to the rules used to write PHP programs.
Example:
<?php
// This is a single-line comment
echo "Welcome to PHP";
?>


Important points:
- PHP code is written inside <?php ... ?> tags.
- Statements usually end with a semicolon (;).
- Variables begin with the $ symbol.
- PHP statements generally end with a semicolon.
- Comments can be written using //, #, or /* ... */.
6. Variables and Constants
Variables
A variable is a named storage location used to store data.
Example:
<?php
$name = "Rohan";
$age = 19;

echo $name;
echo "<br>";
echo $age;
?>


Output:
Rohan
19


Rules for PHP variables:
1. A variable must begin with $.
2. A variable name must start with a letter or underscore after $.
3. Variable names are case-sensitive.
4. A variable can store different types of data.
Constants
A constant is a name for a value that cannot be reassigned after it has been defined.
Example:
<?php
define("COLLEGE", "Tulshi College");
echo COLLEGE;
?>


Output:
Tulshi College


7. Data Types in PHP
A data type defines the kind of value a variable can hold.
Data Type	Description	Example
String	A sequence of characters	"Hello"
Integer	Whole numbers	100
Float	Decimal numbers	10.5
Boolean	True or false	true
Array	Collection of values	[10, 20, 30]
NULL	Represents no value	null
Object	Instance of a class	$student
Example:
<?php
$name = "Rohan";
$age = 19;
$percentage = 85.5;
$isStudent = true;

var_dump($name);
var_dump($age);
var_dump($percentage);
var_dump($isStudent);
?>


The var_dump() function displays the data type and value of a variable.
8. Type Casting
Type casting is the process of converting a value from one data type to another.
Example:
<?php
$num = "100";
$num = (int)$num;

var_dump($num);
?>


Output:
int(100)


Common type casting operators:
- (int) — Converts to integer.
- (float) — Converts to float.
- (string) — Converts to string.
- (bool) — Converts to Boolean.
- (array) — Converts to array.

Module 2: Operators and Control Structures (10 Hours)
1. Operators in PHP
Operators are symbols used to perform operations on variables and values.
A. Arithmetic Operators
Operator	Operation	Example	Result
+	Addition	10 + 5	15
-	Subtraction	10 - 5	5
*	Multiplication	10 * 5	50
/	Division	10 / 5	2
%	Modulus	10 % 3	1
**	Exponentiation	2 ** 3	8
B. Comparison Operators
Comparison operators compare two values and return a Boolean result.
Operator	Meaning
==	Equal in value
===	Equal in value and type
!=	Not equal
>	Greater than
<	Less than
>=	Greater than or equal to
<=	Less than or equal to
C. Logical Operators
Logical operators combine or reverse conditions.
| Operator | Meaning |
|---|---|
| && | Logical AND |
| || | Logical OR |
| ! | Logical NOT |
Example:
<?php
$age = 20;
$hasID = true;

if ($age >= 18 && $hasID) {
    echo "Allowed";
}
?>


Output:
Allowed


2. Conditional Statements
Conditional statements execute code based on specified conditions.
A. if Statement
Executes a block when the condition is true.
<?php
$age = 20;

if ($age >= 18) {
    echo "Eligible to vote";
}
?>


Output: Eligible to vote
B. if-else Statement
Executes one block if the condition is true and another if it is false.
<?php
$marks = 35;

if ($marks >= 40) {
    echo "Pass";
} else {
    echo "Fail";
}
?>


Output: Fail
C. switch-case Statement
The switch statement selects a code block based on the value of an expression.
<?php
$day = 2;

switch ($day) {
    case 1:
        echo "Monday";
        break;

    case 2:
        echo "Tuesday";
        break;

    default:
        echo "Invalid day";
}
?>


Output: Tuesday
3. Looping Structures
Loops execute a block of code repeatedly.
A. for Loop
Used when the number of iterations is known or controlled by a counter.
<?php
for ($i = 1; $i <= 5; $i++) {
    echo $i . " ";
}
?>


Output: 1 2 3 4 5
B. while Loop
Repeats a block while the condition is true.
<?php
$i = 1;

while ($i <= 5) {
    echo $i . " ";
    $i++;
}
?>


C. do-while Loop
Executes the block at least once before checking the condition.
<?php
$i = 1;

do {
    echo $i . " ";
    $i++;
} while ($i <= 5);
?>


D. foreach Loop
Used to iterate through arrays.
<?php
$colors = ["Red", "Green", "Blue"];

foreach ($colors as $color) {
    echo $color . "<br>";
}
?>


Output:
Red
Green
Blue


4. Break and Continue
break Statement
The break statement immediately terminates a loop or exits a switch statement.
<?php
for ($i = 1; $i <= 5; $i++) {
    if ($i == 3) {
        break;
    }

    echo $i;
}
?>


Output: 12
continue Statement
The continue statement skips the current loop iteration and proceeds to the next iteration.
<?php
for ($i = 1; $i <= 5; $i++) {
    if ($i == 3) {
        continue;
    }

    echo $i;
}
?>


Output: 1245

Module 3: Functions and Arrays (10 Hours)
1. Functions in PHP
A function is a reusable block of code designed to perform a specific task.
Advantages of functions:
1. Reduce code repetition.
2. Improve code readability.
3. Make programs easier to maintain.
4. Support code reusability.
Defining and Calling a Function
<?php
function greet() {
    echo "Welcome to PHP";
}

greet();
?>


Output: Welcome to PHP
2. Function Parameters and Return Values
Parameters allow a function to receive input values.
Return values allow a function to send a result back to the calling code.
Example:
<?php
function add($a, $b) {
    return $a + $b;
}

$result = add(10, 20);
echo $result;
?>


Output: 30
In this example:
- $a and $b are parameters.
- 10 and 20 are arguments.
- return sends the result back.
- $result stores the returned value.
3. Built-in vs User-Defined Functions
Built-in Functions	User-Defined Functions
Provided by PHP.	Created by the programmer.
Ready to use.	Must be defined before use in the normal workflow.
Example: strlen()	Example: add()
Example: count()	Example: calculateTotal()
Example: sort()	Example: displayMessage()
Built-in function example:
<?php
echo strlen("Hello");
?>


Output: 5
The strlen() function returns the length of a string in bytes.
4. Arrays in PHP
An array stores multiple values in a single variable.
A. Indexed Array
An indexed array uses numeric indexes, usually starting from zero.
<?php
$fruits = ["Apple", "Mango", "Banana"];

echo $fruits[0];
echo "<br>";
echo $fruits[1];
?>


Output:
Apple
Mango


B. Associative Array
An associative array stores values using named keys.
<?php
$student = [
    "name" => "Rohan",
    "age" => 19,
    "course" => "BCS"
];

echo $student["name"];
?>


Output: Rohan
5. Array Functions
A. Sorting — sort()
Sorts indexed array values in ascending order and reindexes the keys.
<?php
$numbers = [30, 10, 20];

sort($numbers);
print_r($numbers);
?>


Output:
Array ( [0] => 10 [1] => 20 [2] => 30 )


B. Merging — array_merge()
Combines two or more arrays.
<?php
$a = [1, 2];
$b = [3, 4];

$result = array_merge($a, $b);
print_r($result);
?>


Output:
Array ( [0] => 1 [1] => 2 [2] => 3 [3] => 4 )


C. Searching — in_array()
Checks whether a specified value exists in an array.
<?php
$fruits = ["Apple", "Mango", "Banana"];

if (in_array("Mango", $fruits)) {
    echo "Found";
} else {
    echo "Not Found";
}
?>


Output: Found
Other Important Array Functions
Function	Purpose
count()	Returns the number of elements.
rsort()	Sorts values in descending order.
array_search()	Searches for a value and returns its key if found.
array_push()	Adds elements to the end of an array.
array_pop()	Removes the last element.

Module 4: PHP and MySQL — Introduction
PHP and MySQL are commonly used together to develop database-driven web applications.
MySQL is a relational database management system used to store and manage data.
Applications:
1. Student management systems.
2. Login and registration systems.
3. Online shopping websites.
4. Employee management systems.
5. Library management systems.
Basic Database Operations (CRUD)
Operation	Meaning
Create	Insert new records
Read	Retrieve records
Update	Modify existing records
Delete	Remove records
PHP can connect to MySQL using MySQLi or PDO.

Important Questions for the Examination
Short-answer questions
1. What is PHP?
2. Define client-side scripting.
3. What is server-side scripting?
4. What is a PHP variable?
5. Define a constant.
6. What is type casting?
7. What is an array?
8. Define a function.
9. What is the use of break?
10. What is the use of continue?
Long-answer questions
1. Explain PHP and its features.
2. Differentiate between client-side and server-side scripting.
3. Explain the installation and configuration of XAMPP.
4. Explain PHP variables, constants, and data types with examples.
5. Explain arithmetic, comparison, and logical operators.
6. Explain conditional statements with suitable examples.
7. Explain the different looping structures in PHP.
8. Differentiate between break and continue.
9. Explain functions, parameters, and return values.
10. Differentiate between indexed and associative arrays.
11. Explain sorting, merging, and searching array functions.
12. Explain the role of PHP and MySQL in web development.
Recommended References
- Official PHP Documentation
- Learning PHP, MySQL & JavaScript — Robin Nixon, O'Reilly Media.
- PHP and MySQL Web Development — Luke Welling and Laura Thomson, Addison-Wesley
