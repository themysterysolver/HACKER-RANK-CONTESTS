
### HACKERRANK-CONTESTS🚀
---
### ABOUT 📘
- The below documentation will guide you how to create a coding contest
- what's given the below is a part of `DSL`(*Domain Specific Language*) which is like a pesudo code that will create code blocks of your defenition.
  - `DSL` helps you create code stubs like **main function** and **solution function**
  - You can decide the input types and parameters.  
---
### STEPS TO CREATE A CONTEST 🛠️
- **STEP-1:** Siginin and login into *hackerrank* got to [Dashboard](https://www.hackerrank.com/dashboard)
- **STEP-2:** Click the top right corner which contains the logo,you will get to see the `profile->dark mode->leaderboard->settings->bookmarks->network_>submission_>administration->logout`
   - Choose the `administration`
- **STEP-3:** Click ***create contest button*** and exploration is up to you.
#### TIPS 💡
- `Moderators` are the one who is like admin in whatsapp group,they have acess to your contest and they can manage them
  - If you are going to make an official contest with large number of people do it as a team,do it with moderators.
- `Challenges` are the place where you create ***your own question*** or (***in-built***)make use of already made question form hacerrank.
---
### STEPS TO CREATE A CHALLENGE 🧪
- You will come across the word *challenges* these are custom made problems.
  - You can build your own question
- Go to `administration` page [click here](https://www.hackerrank.com/administration/challenges)
- Choose `Manage chalanges` 
- **STEP-1:**  Click `Create challenge`
- **STEP-2:** You can always change this *create page* later. so make it as a simple dummy page(fill rubbish),just give a proper ***Challenge Name*** as of now and *minimal description* u can change it later.
- **STEP-3:** In `details` you can change the entire description,you can modify *problem statement*,etc.
  - Note everything is a `MarkDown` so you can style it,it is saved as **.md**
  - You can *preview* the content
- **STEP-4**: here comes the fun part
  - Go to `Code stubs`,this is the place where you will create stub which will generate template code in all languages you have selelcted in `Langugaes`
  - Paste the below code and click `Generate Code stubs` then you are ready to go.
###### EXAMPLE1 ✏️
```DSL []
function(boolean,isPower,integer n)
integer(n)
invoke(boolean,result,isPower,n)
print(boolean,result)
```
###### EXAMPLE2 ✏️
```DSL []
function(2d_integer_array, findMe2, integer l, integer m, integer n, integer target, integer_array arr)
integer(l) integer(m) integer(n) integer(target)
Array(integer, arr, l, single)
invoke(2d_integer_array, result, findMe2, l, m, n, target, arr)
print(2d_integer_array, result)
```
##### How it works? ⚙️
- `function` creates a function with syntax given below
- *inputs* are given in the next few lines with synatx given below
- `invoke` calls it
- `print` makes the user get to see the output.
---
### TEST CASES 🧪
- **NOTE:** The `input` is given in the format how you gdefined the code in your stubs(DSL)
- `output` is just the answer for the input what you gave.
- You can give it as *sample* and explain it. This is visible once you click the *pencil* option
- Also You can change *strength* for each test case.
- To create a large number of test cases you can write a *custom script* that will define files as
```
testcases.zip
├── input00.txt
├── output00.txt
├── input01.txt
├── output01.txt
└── ...
```
- You can code solution for you code and create a script(py code,java code) to create a new file under a *empty folder* with proper matching name.
  - Then you can zip it
  - Upload it 
#### TIPS 💡
- [How Do I Upload All Test Cases at Once?](https://customersupport.hackerrank.com/hc/en-us/articles/115007826547-How-Do-I-Upload-All-Test-Cases-at-Once)
- For creating arrays input give spacing properly.
- For boolean output give `1` or `0`.
---
### DSL 🧠
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

---


