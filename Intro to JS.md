# Getting started with javascript Exercises - ModernDeveloper

---

## EXERCISE 1

### Q1.	Run console.log(5); in your browser’s console.

### Q2.	Run console.log(5); on the JSbin website. 

### Q3.	Print your name to the console. Hint: Put your name in double quotation marks

**Output/Anwser**

![image](https://cloud.githubusercontent.com/assets/16424306/17203480/64ab05f0-54bd-11e6-9ba8-35c6736e8b7d.png)



![image](https://cloud.githubusercontent.com/assets/16424306/17203512/97e56fa0-54bd-11e6-86ed-69fca8c29ac0.png)


## EXERCISE 2

### Q1.	From your understanding of expressions and statements, write the difference between them.

#### Output/Anwser 

### EXPRESSIONS
1.	An expression is combination of literals, variables, and operators that result in a value.

2.	Expression produces or evaluates some value.

3.	Examples of expressions:

* a)	New Date() – produces new date object without any other effect.

* b)	[1,2,3] - produces new array object.

* c)	5+6 - produces new value 11, it has no other effect.

###  STATEMENTS
1.	Any combination of keywords, comments, literals, variables, operators, and expressions construct a statement.

2.	Statements produces some behaviour that has some effect. Statements are executed and have some effect.

3.	Examples of statements:

* a)	X=5; – it’s a statement as it changes the value of x (it has effect on x)

* b)	SetTimeout(5) ; – starts the timer in the browser, so it has effect on the browser hence it is a statement

* c) 	X+=6; – expression statement

* A group of primary expressions is doing assignment that is a side effect, so it is called expression statement.


### Q2. Identify the keywords, comments, literals, variables, operators, and expressions in the following program. How many statements are there?

```
var sum = 32 + 23 + 26;
/*
The formula for calculating average is:
average = sum_of_all_items/total_number_of_items
*/
var avg = sum / 3;
console.log(avg); //prints the average
```

#### Output/Anwser

Number of keywords: 1 – “var” 

Number of comments: 2 – 1st is a multiline comment, 2nd is single line 
comment.

Number of Literals:4 – 32, 23, 26 and 3

Number of variables:2 – sum and avg 

Number of operators: 3 – first is “=” assignment operator & “+” and 
“/ ” are arithmetic operators.

Number of expressions: 2 – first is 32+23+26 and second is sum/3 

Number of statements: 3 because comments are not executed and 
Anything that can be executed is called statement explicitly.


## EXERCISE 3

### Q1. Without running the following program can you guess the output?
```
var a;
console.log(a);
```
#### Output/Anwser
> undefined

### Q2.	Divide 100 with 0 and print the result to the console. What is the data type of the output?

#### Output/Anwser

> INFINITY


> Datatype: Number

### Q3. Create an array with 3 items: "banana", "apple", "orange". Print all these items using index only.

#### Output/Anwser

```
var fruits = ['apple', 'orange', 'banana'];
console.log(fruits[0]);
        console.log(fruits[1]);
        console.log(fruits[2]);

```

### Q4.	Print the last element of an array. Make sure you test your program with arrays of different sizes.

#### Output/Anwser

```
var firstarray = ['1stitem', '2nditem', '3rditem', '4thitem', '5thitem'];
var secondarray = ['hello', 1, 3, 5, true, false, 'javascript'];
        console.log(firstarray.splice(-1)[0]);
        console.log(secondarray[secondarray.length - 1])

```

## EXERCISE 4

### Q1.	Experiment with the precedence of arithmetic and logical operators. Write a short report of your findings.

#### Output/Anwser

REPORT:
Operator precedence determines the order in which operators are evaluated. 
Operators with higher precedence are evaluated first.


**Precedence of Arithmetic operators:**

 The arithmetic operators (+, -, *, /, %) perform arithmetic operations.

| Precedence Value |   Operator    | Description      | 
| -----------------|:-------------:| ----------------:|
| 14               | *             | Multiplication   |
| 14               | /             |   Division       |
| 14               | %             | Modulus operator |
| 13               | +             | Addition         |
| 13               |  -            |  Subtraction     |



The addition and subtraction operators have the same precedence.

Similarly, the multiplication, division, and modulus operators have the same precedence, and the precedence of these operators is higher than the precedence for the addition and subtraction operators.


As it is evident from the table above, that in case of arithmetic operators, multiplication, division, and modulus operators have the same precedence. Similarly, addition and subtraction operators have the same precedence.

if an expression has multiple operators, then the operators are evaluated based on their precedence; an operator with higher precedence is evaluated before an operator with lower precedence. 

If two operators have the same precedence, then the expression is evaluated from left to right.

EXAMPLE:

![image](https://cloud.githubusercontent.com/assets/16424306/17206726/c70d5bf6-54ce-11e6-9a54-e460d5cbd846.png)


**Precedence of Logical operators:**

| Precedence Value |   Operator     | Description     | 
| -----------------|:--------------:| ---------------:|
| 15               | !              | Logical NOT     |
| 6                | &&             | Logical AND     |
| 5                | `||`           | `Logical OR`    |


The logical operators in JavaScript work on boolean values for which they return boolean values.

 There are three logical operators: And (&&), Or (||), and Not (!). 
 
The && operator results in a false if either of the operands is false; the || operator results in a true if either of the operands is true. 

The! operator is used for inverting the value of a boolean, i.e., !true is false and vice versa. 

The possible operations by the logical operators are as follows:

| value                |  result                  |
|:--------------------:|:------------------------:|
|a1 = true  && true    |   // t && t returns true |
|a2 = true  && false   |  // t && f returns false |
|a3 = false && true    |  // f && t returns false |
|a4 = false && (3 == 4)|  // f && f returns false |
|a5 = "Cat" && "Dog"   |  // t && t returns "Dog" |
|a6 = false && "Cat"   |  // f && t returns false |
|a7 = "Cat" && false   |  // t && f returns false |
 
 
| value                  |  result                      |
|-----------------------:|:----------------------------:|
|`o1 = true || true`     | `// t || t returns true`     |
|`o2 = false|| true`     |` // f || t returns true`     |
|`o3 = true || false`    |` // t || f returns true`     |
|`o4 = false|| (3 == 4)` | `// f || f returns false`    |
|`o5 = "Cat"|| "Dog"`    | `// t || t returns "Cat"`    |
|`o6 = false|| "Cat"`    | `// f || t returns "Cat"`    |
|`o7 = "Cat"|| false`    | `// t || f returns "Cat"`    |



| value                |  result                   |
|---------------------:|:-------------------------:|
|n1 = !true            |// it returns false        |
|n2 = !false           |// it returns true         |
|n3 = !"Cat"           |// it returns false        |

EXAMPLES:


![image](https://cloud.githubusercontent.com/assets/16424306/17207657/287ed91a-54d3-11e6-9167-9e966f80f994.png)




### Q2.	What happens when a Boolean is added with a number or a number is added with a string. Experiment on the arithmetic, logical, and comparison operations of different types, i.e., numbers, booleans, and strings. Write a short report of your findings:


#### Output/Anwser


When Boolean is added with a number; it is treated as a number. Hence adding boolean with a number will generate number or sum always. 
Means if the value of boolean variable is True; it is considered 1.

When the value of boolean variable is False; it is considered as 0

For example:

![image](https://cloud.githubusercontent.com/assets/16424306/17207730/80e360c6-54d3-11e6-998d-f8fabb1a428f.png)


Adding two numbers, will return the sum, but adding a number and a string will return a string:

for example:

```
x = 5 + 5;
y = "5" + 5;
z = "Hello" + 5;

10
55
Hello5
```

### Q3.Write a program that converts celsius temperature to fahrenheit and vice versa.
The formula for conversion is: c/5 = f-32/9 where c represents celsius and f represents fahrenheit.

#### Output/Anwser

```
<html>
     <body>

<script>

function convert(degree) {
if (degree == "celci") {
         faren = document.getElementById("celci").value * 9 / 5 + 32;
         document.getElementById("faren").value = Math.round(faren);
}
     else {
     celci = (document.getElementById("faren").value - 32 ) * 5 / 9;
          document.getElementById("celci").value = Math.round(celci);
        }
    };

</script>

<style>
        html,body{
            font-family:Arial;
            padding-top:10px;      
             }
        #div1 {
            width:100%;
       }

        div2{
           width:50%;
        }
    </style>
    <div id="div1">
        <div class="div2">
            <p>enter temprature in celcius:</p>
            <input id="celci" onkeyup="convert('celci')" />  degree celcius
        </div>
        <br />
        <p>OR</p>
        <div class="div2">
          <p> enter temprature in farenheite:</p>
           <input id="faren" onkeyup="convert('faren')" />  degree farenheite
        </div>

    </div>    
</body>
</html>
```

![celci](https://cloud.githubusercontent.com/assets/16424306/17208012/9a8cbd00-54d4-11e6-8d10-2c91a4526ecd.png)



### Q4.	Find the maximum of two numbers using the ternary operator. You can assume that the numbers are not equal.

#### Output/Anwser

```
<body>
       <style>
html, body {
font-family: Arial;
padding-top: 10px;
}

    #div1 {
      width: 100%;
}

   div2 {
width: 50%;
}
</style>
<div id="div1">
<div class="div2">
<p>enter 1st number:<input type="text" id="first1" /></p>
</div>
<br />
<div class="div2">
       <p> enter 2nd number: <input type="text" id="second2" /></p>
</div>
<button onclick="check();">max</button>
<br />
</div>
<script>
function check() {
var first = document.getElementById('first1').value;
var second = document.getElementById('second2').value;
var result = first > second ? first : second;
console.log(result);
}
</script>
</body>
```

![image](https://cloud.githubusercontent.com/assets/16424306/17208041/bddd2150-54d4-11e6-9661-cc29ccf897b1.png)


### Q5.Multiply three numbers together and output whether the result is positive or negative. 

For example, if the input is 1, 2, 3 your program should output positive. 

Similarly, for 1, -2, 3 it should output negative. Hint: You can use the ternary operator.

#### Output/Anwser

```
<body>
<!--Multiply three numbers together and output whether the result is positive or negative. For example,
if the input is 1, 2, 3 your program should output positive.
Similarly, for 1, -2, 3 it should output negative. Hint: You can use the ternary operator.-->
<style>
html, body {
font-family: Arial;
padding-top: 10px;
}

#div1 {
width: 100%;
}

div2 {
width: 50%;
}
</style>

<div id="div1">
<div class="div2">
<p>enter 1st number: <input type="text" id="first1" /></p>
</div>


<div class="div2">
<p> enter 2nd number: <input type="text" id="second2" /></p>
</div>

<div class="div2">
<p> enter 3rd number: <input type="text" id="third3" /></p>
</div>


<button onclick="check();">find</button>
<br />


</div>

<script>
function check() {
var first = document.getElementById('first1').value;
var second = document.getElementById('second2').value;
var third = document.getElementById('third3').value;
var forth = first * second * third;
console.log("answer of multiplication is: " +forth);
var result = forth > 0 ? "positive" : forth == 0 ? "it is neither positive nor negative!" : "negative";
console.log(" and the result is: " + result);
}
</script>
</body>
```
Screen 1: with zero as input:
![image](https://cloud.githubusercontent.com/assets/16424306/17208168/fb1c2bec-54d4-11e6-9eb9-d4d6d076f4dc.png)


Screen 2: with 1 input as negative value:
![image](https://cloud.githubusercontent.com/assets/16424306/17208194/1ef3c124-54d5-11e6-8d61-8cec044cbf86.png)


Screen 3: with 3 inputs as negative values:
![image](https://cloud.githubusercontent.com/assets/16424306/17208208/3ad4c7b2-54d5-11e6-9688-0b5ed11dba63.png)


## EXERCISE 5

### Q1.Find if a year is a leap year or not using the if...else statements described above. Validate your program for the following input: 2104 (true), 2100 (false), 2000 (true), 2001 (false). 
Hint: A leap year is evenly divisible by 4; however, if a year is evenly divided by 100, it is not a leap year, unless the year is also evenly divisible by 400.

#### Output/Anwser

```
<body>
<script>
function check_leapyear() {
var year;
var year = document.getElementById("year").value;
if ((year % 4 == 0) && (year % 100) || (year % 400 == 0)) {
console.log(year + " is a leap year")
}
       else {
console.log(year + " is not a leap year");
}
}
</script>
   <p>enter the year: </p>
<input type="text" id="year" />
<button onclick="check_leapyear();">check</button>
</body>
```

![image](https://cloud.githubusercontent.com/assets/16424306/17208314/d3a342c0-54d5-11e6-9aa6-143fbd14d7fe.png)


### Q.2 Find the minimum of three numbers using the if...else statements described above.


#### Output/Anwser
```
<body>
    <!--Find the minimum of three numbers using the if...else statements described above.-->
    <style>
        html, body {
            font-family: Arial;
            padding-top: 10px;
        }

        #div1 {
            width: 100%;
        }

        div2 {
            width: 50%;
        }
    </style>

    <script>
        function minimum() {
            var first = document.getElementById('first1').value;
            var second = document.getElementById('second2').value;
            var third = document.getElementById('third3').value;

            //using if else if....else 

            if((first<second) && (first<third)){
                console.log(first + " is minimum");
            }
            else if((second<first) && (second<third)) {
                console.log(second + " is minimum");
            }
            else{
                console.log(third + " is minimum");
            }


                if ((first < second) && (first<third)) {

                    console.log(first + " is minimum");

                    }
                    else{
                    console.log(third + " is minimum");
                    if ((second < first) && (second < third)) {
                        console.log(second + "is minimum");
                    }
                    }
            }
    </script>

    <div id="div1">
        <div class="div2">
            <p>enter 1st number: <input type="text" id="first1" /></p>
        </div>
        <br />
        <div class="div2">
            <p> enter 2nd number: <input type="text" id="second2" /></p>
        </div>
        <br />
        <div class="div2">
            <p> enter 3rd number: <input type="text" id="third3" /></p>
        </div>
        <button onclick="minimum();">find minimum of these 3 numbers </button>
        <br />
    </div>
</body>

```


![image](https://cloud.githubusercontent.com/assets/16424306/17208364/117d6076-54d6-11e6-9fb1-2af0fc4d1b3c.png)


###Q3.	Given three numbers, print them in descending order using the if...else statements described above.
You are not allowed to use any logical operator to solve this problem, but you are welcome to use comparison operators.

#### Output/Answer

```
<body>
    <!--Given three numbers, print them in descending order using the if...else statements described above. 
    You are not allowed to use any logical operator to solve this problem, but you are welcome to use comparison operators.-->
    <script>
        var a = 3;
        var b = 1;
        var c = 2;

        if (c >= b) {
            if (c >= a) {
                if (b >= a) {
                    console.log(c, b, a);
                }
                else {
                    console.log(c, a, b);
                }
            }
            else {
                console.log(a, c, b);
            }
        }
        else if (c >= a) {
            console.log(b, c, a);
        }
        else if (b >= a) {
            console.log(b, a, c);
        }
        else {
            console.log(a, b, c);
        }
    </script>
</body>






Output:
3 2 1

```

## Q 4.	Using if...elseif...else, find the minimum of five numbers.

### Output/Answer

```
<body>
    <style>
        html, body {
            font-family: Arial;
            padding-top: 10px;
        }

        #div1 {
            width: 100%;
        }

        div2 {
            width: 50%;
        }
    </style>

    <script>
        function minimum() {

           
            var first = parseFloat(document.getElementById('first1').value);
            var second = parseFloat(document.getElementById('second2').value);
            var third = parseFloat(document.getElementById('third3').value);
            var forth = parseFloat(document.getElementById('forth4').value);
            var fifth = parseFloat(document.getElementById('fifth5').value);

            //using if else if....else
           

            if((first <= second) && (first <= third) && (first <= forth) && (first <= fifth)){
                console.log(first);
            }
            else if ((second <= first) && (second <= third) && (second <= forth) && (second <= fifth)) {
                console.log(second);
            }
            else if ((third <= first) && (third <= second) && (third <= forth) && (third <= fifth)) {
                console.log(third);
            }
            else if ((forth <= first ) && (forth <= second) && (forth <= third) && (forth <= fifth)){
                console.log(forth);
            }
            else {
                console.log(fifth);
            }
        }
    </script>

    <div id="div1">
        <div class="div2">
            <p>enter 1st number: <input type="text" id="first1" /></p>
        </div>
        <br />
        <div class="div2">
            <p> enter 2nd number: <input type="text" id="second2" /></p>
        </div>
        <br />
        <div class="div2">
            <p> enter 3rd number: <input type="text" id="third3" /></p>
        </div>
        <br />
        <div class="div2">
            <p> enter 4th number: <input type="text" id="forth4" /></p>
        </div>
        <br />
        <div class="div2">
            <p> enter 5th number: <input type="text" id="fifth5" /></p>
        </div>
        <button onclick="minimum();">find minimum of these 5 numbers </button>
        <br />
    </div>
</body>
```

![image](https://cloud.githubusercontent.com/assets/16424306/17208459/76579606-54d6-11e6-98d1-d6883ccf1e6f.png)



Exercise 6

1.	Use switch...case to rewrite the following code:
var customerType = "subscribed";
var cost = 250;
var discount = 0.1;
if(customerType === "regular"){
  discount = 0.1;
}
else if(customerType === "subscribed"){
  discount = 0.2;
}
else{
  discount = 0;
}
console.log("The cost of the product: " + (cost - cost * discount));


var customerType = "subscribed";
        var cost = 250;
        var discount = 0.1;

        switch (customerType) {

            case "regular":
                
                discount = 0.1;
                console.log("The cost of product: " + (cost - cost * discount));
                break;

            case "subscribed":
               
                discount = 0.2;
                console.log("The cost of product: " + (cost - cost * discount));
                break;

            default:
                discount = 0;
                console.log("The cost of product: " + (cost - cost * discount));
                break;
        }


Output:














