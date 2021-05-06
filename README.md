# String calculator

This classic kata guides you step by step through the implementation of a calculator that receives a String as input. It
is a good exercise on refactoring and incremental implementation.  
It is also a good candidate for practicing TDD.

## Step 1

Create a function add that takes a String and returns a String:

```python
    def add(numbers):
        pass
```

* The method can take up to two numbers, separated by commas, and will return their sum.
* For an empty string it will return 0.
* When the string is invalid it will raise "Number expected but <value> found." (for example, "thermo,fisher", "1 2 3", "1,,2" are invalid inputs)

## Step 2

Allow to pass an unknown amount of numbers.

## Step 3

Allow the add method to handle newlines as separators:

 * "1\n2,3" should return "6".
 * "175.2,\n35" is invalid and should return the message "Number expected but '\n' found at position 6."

## Step 4

Don’t allow the input to end in a separator.

"1,3," is invalid and should return the message "Number expected but EOF found."

## Step 5

Support different delimiters:

* To change a delimiter, the beginning of the string will contain a separate line that looks like
  this: ``"//[delimiter]\n[numbers…]"``.   
  For example ``"//;\n1;2"`` should return three where the default delimiter is
  ``';'``.
* The first line is optional.
* All existing scenarios should still be supported.

## Step 5

Calling add with negative numbers will return the message "Negative not allowed : " listing all negative numbers that were in the list of numbers.

 * "-1,2" is invalid and should return the message "Negative not allowed : -1"
 * "2,-4,-5" is invalid and should return the message "Negative not allowed : -4, -5"
