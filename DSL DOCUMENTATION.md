
![image](https://s3.amazonaws.com/hr-assets/0/1497424157-e614e16f24-hr.png)

Welcome to [HackerRank](https://www.hackerrank.com) DSL (Domain Specific Language) Documentation! You can use our the DSL to generate code stubs that read test case data from standard input in hackerrank challenges.

* [Datatypes Supported](#datatypes-supported)
* [Reading Variables](#reading-variables)
* [Writing Loops](#writing-loops)
* [Reading 1-D Array](#reading-1-d-array)
* [Reading 2-D Array](#reading-2-d-array)
* [Putting Comments](#putting-comments)
* [Generating Functions](#generating-functions)
* [Invoke a Function](#invoke-a-function)
* [Print a Variable](#print-a-variable)
* [DSL In Action](#dsl-in-action)
* [Bug Report or Need help?](#support)


### Datatypes Supported

- Integer: `integer`
- Float: `float`
- String: `string`
- Boolean: `boolean`
- Long Integer: `long_integer`
- Character: `character`
  

### Reading variables 


| **Syntax**  | **Example** |
| ------------- | ------------- |
| `Datatype(variable_name)`  | integer(a)  |
| At most 4 variables per line is supported | integer(n) integer(k) |


### Writing Loops

You can use loops to read multiple test cases.

| **Syntax**  | **Example** |
| ------------- | ------------- |
| ``loop(variable_name)``<br>``{code}``<br>``endloop``  | loop(t)<br>integer(n)<br>endloop  |

### Reading 1-D Array

| **Syntax**  | **Example** |
| ------------- | ------------- |
| ``Array(Datatype,name,size,single)``   | Array(integer,a,n,single) |
| ``Array(Datatype,name,size,multi)`` | Array(float,b,m,multi) |

Note: Type is ``single`` if the array elements are on the same line. Otherwise, it should be ``multi``.
Warning: Don't leave any extra space.

### Reading 2-D Array

| **Syntax**  | **Example** |
| ------------- | ------------- |
| ``2DArray(Datatype,name,size1,size2)``   | 2DArray(integer,a,n,m)   |


### Putting Comments

| **Syntax**  | 
| ------------- | 
| ``#Your own comment``   |

A special comment is ``#StartCode``, this will generate the text "your code goes here" as a comment.


## Generating Functions

| **Syntax**  | **Example** |
| ------------- | ------------- |
| ``Function(return_type, function_name, param_type1 name1, param_type2 name2, …)``   | function(integer_array, solve, integer x, integer_array board) |

* Return type/Param type supported:

    * integer
    * long_integer
    * string
    * integer_array/long_integer_array/string_array
    * 2d_integer_array/2d_long_integer_array/2d_string_array (**param only**)
    * void (return type only)

## Invoke a Function

| **Syntax**  | **Example** |
| ------------- | ------------- |
| ``INVOKE(return_type, variable_name,function_name,  param1, param2…)``   |  INVOKE(integer_array, result, solve, n, board[n]) |

* If the invoked function is void, return_type and variable_name should be “void”.
* If the param is a 1-d array, format is param[size]

## Print a variable


| **Syntax**  | **Example** |
| ------------- | ------------- |
| ``PRINT(data_type, variable_name)``| PRINT(integer, result)|
| ``PRINT(data_type, separator)``| PRINT(integer_array, result, +)<br>PRINT(integer_array, result, NEWLINE)<br>PRINT(integer_array, result, COMMA)|

* The third parameter is optional. The default separator is space. The separator can be NEWLINE, SPACE, COMMA or any character.

* Data_type supported are single integer/long_integer/string and 1-d integer/string/long_integer array.  


### DSL In Action  

| **Challege**  | **DSL** |
| ------------- | ------------- |
| https://www.hackerrank.com/challenges/mark-and-toys     | ``integer(n) integer(k)``<br>``Array(integer,a,n,single)`` |
| https://www.hackerrank.com/challenges/two-arrays     | ``integer(t)``<br>``loop(t)``<br>``integer(n) integer(k)``<br>``Array(integer,a,n,single)``<br>``endloop`` |
| https://www.hackerrank.com/challenges/breaking-best-and-worst-records | ``FUNCTION(INTEGER_ARRAY, getRecord, INTEGER_ARRAY s)``<br>``Integer(n)``<br>``Array(integer,s,n,single)``<br>``INVOKE(INTEGER_ARRAY, result, getRecord, s[n])``<br>``PRINT(INTEGER_ARRAY, result)`` |
| https://www.hackerrank.com/challenges/cavity-map   | ``integer(n)``<br>``2DArray(character,grid,n,n+1)  ``|

### Support

If you have any doubt, contact [HackerRank support](http://hackerrank.com/support), our engineers will reach you.
