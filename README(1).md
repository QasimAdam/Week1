# PHP Programming Concepts

This folder contains PHP programming practice examples demonstrating fundamental concepts covered in the course **Web Application Development - PHP & MySQL**.

The project focuses on beginner-level PHP syntax, output statements, variables, constants, conditional statements, switch statements, and grade checking.

---

# PHP Beginner Concepts

This project covers the following PHP concepts:

* Echo
* Print
* Variables
* Constants
* If Statements
* Elseif Statements
* Else Statements
* Switch Statements
* Case
* Break
* Default
* Grade Checking

---

# 1. Echo Statement

## Concept

`echo` is used to display text or other output in the browser.

It is one of the most commonly used output statements in PHP.

## Syntax

```php
echo "Hello World";
```

Parentheses are optional:

```php
echo ("Hello World");
```

## Example

```php
<?php

echo "Welcome to PHP";

?>
```

## Output

```text
Welcome to PHP
```

---

# 2. Print Statement

## Concept

`print` is another PHP statement used to display output in the browser.

Unlike `echo`, `print` accepts only one argument and returns a value.

## Syntax

```php
print "Hello World";
```

Parentheses are also optional:

```php
print ("Hello World");
```

## Example

```php
<?php

print "Hello World";

?>
```

## Output

```text
Hello World
```

---

# 3. Echo and Print

## Description

Both `echo` and `print` can be used to display text.

### Echo

```php
<?php

echo "Welcome to PHP";

?>
```

### Print

```php
<?php

print "Welcome to PHP";

?>
```

Both produce:

```text
Welcome to PHP
```

## Multiple Arguments with Echo

`echo` can display multiple arguments separated by commas.

Example:

```php
<?php

echo "Hello", " World";

?>
```

## Output

```text
Hello World
```

`print` accepts only one argument.

Example:

```php
<?php

print "Hello World";

?>
```

---

# 4. Variables

## Concept

A variable is used to store data.

In PHP, variables always start with the `$` symbol.

## Syntax

```php
$variableName = value;
```

## Example

```php
<?php

$name = "Fuaad Abuukar";
$age = 20;

echo "My name is $name";
echo "<br>";
echo "My age is $age";

?>
```

## Output

```text
My name is Fuaad Abuukar
My age is 20
```

## Important

The `$` symbol is required when creating and using a variable.

```php
$name = "Fuaad";
$age = 20;
```

---

# 5. Constants

## Concept

A constant is a value that is intended to remain unchanged.

PHP constants can be created using the `define()` function.

## Syntax

```php
define("CONSTANT_NAME", value);
```

## Example

```php
<?php

define("AGE", 20);

echo AGE;

?>
```

## Output

```text
20
```

## Important

Variables use `$`:

```php
$age
```

Constants do not use `$`:

```php
AGE
```

---

# 6. If / Elseif / Else

## Concept

Conditional statements are used to make decisions in a PHP program.

PHP uses:

* `if` to check the first condition
* `elseif` to check another condition
* `else` when all previous conditions are false

## Syntax

```php
if (condition) {

    // code

}
elseif (condition) {

    // code

}
else {

    // code

}
```

## Example

```php
<?php

$age = 20;
$grade = 4;

if ($age > 20) {

    echo "Adult";

}
elseif ($grade < 2) {

    echo "Finished";

}
else {

    echo "End";

}

?>
```

## How It Works

First, PHP checks:

```php
$age > 20
```

The value is:

```text
20 > 20
```

This condition is `false`.

PHP then checks:

```php
$grade < 2
```

The value is:

```text
4 < 2
```

This is also `false`.

Therefore, PHP executes the `else` block.

## Output

```text
End
```

---

# 7. Switch Statement

## Concept

A `switch` statement is used when one value needs to be compared with multiple possible values.

It can be useful when there are many possible cases.

## Syntax

```php
switch ($value) {

    case value1:
        // code
        break;

    case value2:
        // code
        break;

    default:
        // code
        break;
}
```

---

# 8. Switch — Yes or No Example

## Example

```php
<?php

$answer = 'N';

switch ($answer) {

    case 'Y':
    case 'y':

        echo "The answer was yes";

        break;

    case 'N':
    case 'n':

        echo "The answer was no";

        break;

    default:

        echo "Invalid answer";

        break;
}

?>
```

## How It Works

The variable contains:

```php
$answer = 'N';
```

PHP checks each case.

First:

```php
case 'Y':
case 'y':
```

No match.

Then:

```php
case 'N':
case 'n':
```

This matches the value `N`.

Therefore:

```php
echo "The answer was no";
```

is executed.

## Output

```text
The answer was no
```

---

# 9. Break Statement

## Concept

`break` is used to stop the execution of a `switch` case.

Example:

```php
case 'N':

    echo "The answer was no";

    break;
```

After PHP executes the matching case, `break` prevents PHP from continuing to the next cases.

---

# 10. Default Statement

## Concept

`default` runs when none of the cases match.

Example:

```php
switch ($answer) {

    case 'Y':
        echo "Yes";
        break;

    case 'N':
        echo "No";
        break;

    default:
        echo "Invalid answer";
        break;
}
```

If `$answer` is:

```php
$answer = 'X';
```

the output will be:

```text
Invalid answer
```

---

# 11. Grade Checking with If / Elseif / Else

## Concept

Conditional statements can be used to determine a student's result based on their marks.

## Example

```php
<?php

$marks = 87;

if ($marks >= 90) {

    echo "Excellent";

}
elseif ($marks >= 80) {

    echo "Very Good";

}
elseif ($marks >= 70) {

    echo "Good";

}
else {

    echo "Fail";

}

?>
```

## Grade Logic

| Marks       | Result    |
| ----------- | --------- |
| 90 or above | Excellent |
| 80–89       | Very Good |
| 70–79       | Good      |
| Below 70    | Fail      |

## Example

The student has:

```php
$marks = 87;
```

PHP checks:

```php
$marks >= 90
```

False.

Then:

```php
$marks >= 80
```

True.

Therefore:

```text
Very Good
```

is displayed.

---

# 12. Switch — Grade Example

## Concept

A `switch` statement can also be used to check specific score values.

## Example

```php
<?php

$score = 80;

switch ($score) {

    case 100:

        echo "Grade A";

        break;

    case 90:

        echo "Grade A";

        break;

    case 80:

        echo "Grade B";

        break;

    case 70:

        echo "Grade C";

        break;

    case 60:

        echo "Grade D";

        break;

    default:

        echo "Fail";

        break;
}

?>
```

## How It Works

The value is:

```php
$score = 80;
```

PHP searches for:

```php
case 80:
```

It finds a match and executes:

```php
echo "Grade B";
```

## Output

```text
Grade B
```

---

# 13. PHP Line Break

## Concept

`<br>` is an HTML line-break element.

It can be used with PHP output to move the next output to a new line in the browser.

## Example

```php
echo "Hello";
echo "<br>";
echo "World";
```

## Output

```text
Hello
World
```

---

# 14. Complete PHP Example

The following example combines all the concepts covered in this project.

```php
<!DOCTYPE html>
<html lang="en">

<head>

    <meta charset="UTF-8">

    <meta name="viewport"
          content="width=device-width, initial-scale=1.0">

    <title>PHP Beginner</title>

</head>

<body>

<?php

// Echo
echo "Welcome to PHP";

echo "<br>";

// Print
print "Hello World";

echo "<br>";

// Variables
$name = "Fuaad Abuukar";
$age = 20;

echo "My name is $name";

echo "<br>";

echo "My age is $age";

echo "<br>";

// Constant
define("AGE", 20);

echo "Constant AGE is " . AGE;

echo "<br>";

// If / Elseif / Else
$age = 20;
$grade = 4;

if ($age > 20) {

    echo "Adult";

}
elseif ($grade < 2) {

    echo "Finished";

}
else {

    echo "End";

}

echo "<br>";

// Switch
$answer = 'N';

switch ($answer) {

    case 'Y':
    case 'y':

        echo "The answer was yes";

        break;

    case 'N':
    case 'n':

        echo "The answer was no";

        break;

    default:

        echo "Invalid answer";

        break;
}

echo "<br>";

// Grade
$marks = 87;

if ($marks >= 90) {

    echo "Excellent";

}
elseif ($marks >= 80) {

    echo "Very Good";

}
elseif ($marks >= 70) {

    echo "Good";

}
else {

    echo "Fail";

}

echo "<br>";

// Switch Grade
$score = 80;

switch ($score) {

    case 100:

        echo "Grade A";

        break;

    case 90:

        echo "Grade A";

        break;

    case 80:

        echo "Grade B";

        break;

    case 70:

        echo "Grade C";

        break;

    case 60:

        echo "Grade D";

        break;

    default:

        echo "Fail";

        break;
}

?>

</body>

</html>
```

---

# 15. Project Structure

```text
PHP-Beginner/
│
├── Home.php
├── README.md
└── screenshots/
    ├── 01_php_echo_tags.png
    ├── 02_php_print_output.png
    └── 03_php_multiple_echo.png
```

---

# 16. Screenshots / Practice Evidence

The following screenshots show the PHP practice work completed in VS Code. They demonstrate basic PHP tags, output statements, line breaks, and multiple `echo` statements.

## Screenshot 1 — PHP Tags and Echo

This screenshot demonstrates how PHP code is placed inside the `<?php ... ?>` tags. It also shows an `echo` statement using `<br>` to create a line break in the browser output.

![PHP Tags and Echo](screenshots/01_php_echo_tags.png)

### What is demonstrated

- PHP opening and closing tags: `<?php ... ?>`
- `echo` statement
- HTML `<br>` line break
- Basic PHP syntax inside an HTML document

---

## Screenshot 2 — Print Statement

This screenshot demonstrates the PHP `print` statement. The code prints several messages and uses `<br>` between the lines so the output appears on separate lines in the browser.

![PHP Print Output](screenshots/02_php_print_output.png)

### What is demonstrated

- `print` statement
- Printing text from PHP
- `<br>` for line breaks
- Combining HTML and PHP in one page

---

## Screenshot 3 — Multiple Echo Statements

This screenshot demonstrates several `echo` statements used to display different technology names. Each line uses `<br>` to create a new line.

![PHP Multiple Echo Statements](screenshots/03_php_multiple_echo.png)

### Output shown in the example

- Data Science
- PHP
- Oracle
- UI/UX Mobile
- Linux

### Concepts demonstrated

- Multiple `echo` statements
- Text output in PHP
- HTML `<br>` line breaks
- Basic PHP practice in VS Code

---

# 16. How to Run the PHP Project

## XAMPP

Place the project inside:

```text
C:\xampp\htdocs\
```

For example:

```text
C:\xampp\htdocs\CA2313\
```

Make sure the PHP file is saved as:

```text
Home.php
```

Start **Apache** from XAMPP Control Panel.

Then open the browser:

```text
http://localhost/CA2313/Home.php
```

---

# 17. Practice

## Practice 1 — Echo

Create an `echo` statement that displays:

```text
I am learning PHP
```

---

## Practice 2 — Variables

Create:

```php
$name = "Your Name";
$age = 20;
```

Display both values.

---

## Practice 3 — Constant

Create a constant:

```php
define("COUNTRY", "Somalia");
```

Display the constant.

---

## Practice 4 — Age Checker

Create a program that checks:

```text
18 or above → Adult
Below 18   → Minor
```

---

## Practice 5 — Grade Checker

Create a program using:

```php
$marks = 75;
```

Use:

```text
90+ → Excellent
80+ → Very Good
70+ → Good
Below 70 → Fail
```

---

## Practice 6 — Switch

Create:

```php
$answer = "Y";
```

Use `switch` to display:

```text
Y/y → The answer was yes
N/n → The answer was no
Other → Invalid answer
```

---

# 18. Topics Covered

* [x] PHP Introduction
* [x] PHP Syntax
* [x] Echo
* [x] Print
* [x] Variables
* [x] Constants
* [x] If
* [x] Elseif
* [x] Else
* [x] Switch
* [x] Case
* [x] Break
* [x] Default
* [x] Grade Checking
* [x] HTML `<br>` with PHP

---

# 19. Next Topics

After completing these concepts, the next PHP topics are:

1. Comparison Operators
2. Logical Operators
3. Arithmetic Operators
4. Assignment Operators
5. Nested If Statements
6. Ternary Operator
7. Loops
8. Arrays
9. Functions
10. Forms
11. GET and POST
12. Form Validation
13. Sessions
14. Cookies
15. MySQL Database
16. CRUD Operations
17. PHP & MySQL Project

---

# 📌 Summary

```text
Echo / Print  → Display output

Variables     → Store data

Constants     → Store fixed values

If / Elseif   → Make decisions

Switch        → Compare one value with multiple cases

Case          → Define a possible match

Break         → Stop the switch

Default       → Run when no case matches

Grade Logic   → Determine a student's result
```

---

# 👨‍💻 Course

**Web Application Development - PHP & MySQL**

**Level:** Beginner

**Language:** PHP

**Environment:** XAMPP / Apache

**Practice:** VS Code
