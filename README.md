# String Calculator
[A kata from Roy Osherove](http://osherove.com/tdd-kata-1/)

## 1. First step

Create a StringCalculator class with a method

    int add(String number)

* The method can take 0,1 or 2 numbers separated by comma and return their sum,

* "" should return 0
* "1" should return 1
* "1,2,3" should return 6

## 2. Allow the add method to handle an unknown number of arguments

* "1\n2" should return 3.
* "1\n2,3" should return 6.

## 3. Allow the add method to handle a different delimiter

To change the delimiter, the beginning of the string will contain a separate line that looks like this :

    "//[delimiter]\n[numbers]

Example :

    "//;\n1;2"   => 3
    "//|\n1|2|3" => 6

All existing scenarios should work as before.

## 4. Negatives numbers

Calling add with negatives numbers will throw an exception "Negative not allowed : " listing all negative numbers that were in the list of numbers

    "-1,2"    => Negative not allowed : -1
    "2,-4,-6" => Negative not allowed : -4,-6

## 5. Big numbers

Numbers over 1000 are silently ignored.

## 6. Others operations

Write a function for multiply with same rules
