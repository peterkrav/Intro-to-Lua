**Introduction to Loops in Lua**

Being able to automate routine tasks using a computer programming language is an invaluable skill which every programmer should master in order to improve their coding skills and achieve a clearer, more efficient code syntax. With the help of loops syntax, we can achieve the tasks automation.

In this lesson, I&#39;ll explain for and while loop techniques that each can take a slightly different approach to problem solving. You&#39;ll learn how to write your own code and understand when to apply one technique instead of the others.

In Lua, loops can be implemented by:

- &#39;For&#39; Loops
- &#39;While&#39; Loops

**For Loop**

A loop is a repetition of a single task or multiple tasks. If you need to execute something a several times you use a loop. So, after executing a statement once, the execution goes back to the top of the loop and runs the statement again, but the conditions or the loop count value changes with each execution cycle, thus getting closer to the end of the loop. With a loop we can choose a starting point and the finish point. For example, we can print numbers starting from 1 until 10 and stop the loop. We can create and print a countdown starting from 5 and end the loop when we reach 0 (zero).

Loops are useful to simplify the steps by significantly cutting down on number of lines of code and to add greater control of syntax by seeing the exact number of loops or exact range. Loops make code cleaner, and simpler to read and easier to control. The most common types of loop uses are: cycling through values, adding sums of numbers, going through items in a list, repeating a statement and repeating functions.

**Known Value**

If we know already how many times we need to loop, we use a for loop to repeat a specific block of code a known number of times. For example, if we want to check the grade of every student in the class, we loop from one to the known number of students.

**Initialization and Condition statements**

A loop has at least a start value, and an end value, but as an option, you can also add skipping step points as: start, stop, step.

In the syntax example below, the variable initialization, sets the for loop control variable to an initial value (var=exp1). Condition is an expression that is tested each time the loop repeats (exp2). As long as the condition is true, the loop keeps running. Step statement (exp3) skips a number(s) a set number of times.

A `for` loop syntax:

for var=exp1,exp2,exp3 do

something

end

**Example 1: Display a count from 1 (start) to 10 (stop), skipping every 2****nd **** number (step).**

for i=2, 11, 2 do

print(i-1)

end

**Output:** 1 3 5 7 9

**Example 1 Observation:**
Notice that skipping every second number also gives us all the odd numbers between 1 and 10.

**Example 2: Ten multiples of 5. Might be used as the increments count used as a bonus score in a game. Initialize variables &#39;start&#39; and &#39;max&#39; with values 1 and 10 respectively:**

start = 1

max = 10

for i = start, max do

print(i \*5)

end

**Output** : 5, 10, 15, 20, 25, 30, 35, 40, 45, 50

**User Input Values**

Let&#39;s say we want to create a program that receives two input numbers from a user, then adds and displays the sum of the numbers. To receive an input from a user we use an input/output standard function: io.write() and to store the input into a variable we use an input/output standard function: io.read() as in: num1 = io.read(&quot;\*n&quot;). The read function reads number from the current input file. Its arguments control what is read as in the Example 3 program below &quot;\*number&quot; or &quot;\*n&quot; reads a number.

The &quot;\*n&quot; (\*n in double quotes) denotes the function that reads a numeral and returns it as a number.

The \* (a star) is called an opaque pointer, a data type whose concrete data structure is not defined in an interface (hence waiting for an unknown user input), passed (after the user input) to Lua as a new variable state, afterward, receiving numbers from the user, we continue to compute the next task in the program which in this case is adding the numbers and print the results as in:

**Example 3:**

io.write(&#39;Enter the first number: &#39;) -- write a number

num1 = io.read(&quot;\*n&quot;) -- read a number

io.write(&#39;Enter the second number: &#39;) -- write a number

num2 = io.read(&quot;\*n&quot;) -- read a number

sum = num1 + num2

io.write(&#39;Sum is &#39;, sum, &#39;\n&#39;) -- or use: print(&#39;Sum is &#39;, sum, &#39;\n&#39;)

**Output** :

Enter the first number: 20

Enter the second number: 55

Sum is 75

**Exercises:**

**1. Write a program to print all the even numbers from 1 to 10.**

**Output:** 2 4 6 8 10

**Answer:**

for i=1, 10, 2 do

print(i+1)

end

**2. Write a program to display a countdown from 5 to 0.**

Output: 5 4 3 2 1 0

Answer:

for i = 5, 0, -1 do

print(i)

end

**3. Write a program that receives three input numbers from a user and displays the average. Additionally, to round a number use math.floor() function.**

**Output:**

Enter the first number: 5

Enter the second number: 14

Enter the third number: 234

The average is 84

**Answer:**

io.write(&#39;Enter the first number: &#39;)

num11 = io.read(&quot;\*n&quot;)

io.write(&#39;Enter the second number: &#39;)

num22 = io.read(&quot;\*n&quot;)

io.write(&#39;Enter the third number: &#39;)

num33 = io.read(&quot;\*n&quot;)

avr = (num11 + num22 + num33) / 3

io.write(&#39;Average is &#39;, math.floor(avr), &#39;\n&#39;)

**While Loop**

**Initialization and Condition statements**

In the while loop syntax below, you have the variable declaration (var=exp1) outside the loop, the condition (conditionalCheck), and the increment (exp1) within the loop.

The syntax of a &#39;while&#39; loop:

var=exp1

while(conditionalCheck) do

execute statement(s)

exp1 = exp1 + 1

end

In the &#39;while&#39; loop syntax, we first initialize a variable exp1 as our starting point. Lua starts the loop by first testing the exp1 with the conditionalCheck condition; if the condition is false, then the loop stops immediately; otherwise, Lua executes the body of the loop and repeats the process.

**Purpose of the &#39;While&#39; loop**

The purpose of a while loop is to display, change or repeat a section of code until a specific condition is met. We can use a &quot;while&quot; loop if the exact number of times is not known beforehand or if you don&#39;t necessarily need a counter. On the other hand, going through items in a list, it is better to use &#39;for&#39; loop because it clearly conveys the intent.

**Example 1: A while loop that displays the recurring value of a variable &#39;a&#39;, counting from 5 to 10.**

a = 5

while( a \&lt; 11 ) do

print(&quot;Recurring value of a: &quot;, a)

a = a + 1

end

**Output:**

Recurring value of a: 5

Recurring value of a: 6

Recurring value of a: 7

Recurring value of a: 8

Recurring value of a: 9

Recurring value of a: 10

**Example 2: A while TRUE loop without a counter.**

n = 20

while true do

if n % 2 ~= 0 then -- if divisible by 2 and not equal to 0

print(&quot;This number is ODD.&quot;)

break end

print(&quot;This number is EVEN.&quot;)

break -- without this break the loop is infinite!

end

**Output:** This number is EVEN.

**Example 3: A while loop without a counter.**

received\_letter = &quot;a&quot;

new\_letter = &quot;f&quot;

while received\_letter == &quot;a&quot; do

if received\_letter == &quot;c&quot; then

break

end

print(&quot;Received letter: &quot;, received\_letter)

received\_letter = new\_letter

end

print(&quot;Changed letter to: &quot;, received\_letter)

**Output:**

Received letter: a

Changed letter to: f

**Exercise 1: Display a count of 1 to 5 numbers using the while loop.**

a = 1

while a \&lt; 6 do

print( a )

a = a + 1

end

**Output:** 1 2 3 4 5

**Exercise 2:** Write a while loop to print the first 10 Fibonacci numbers. The Fibonacci numbers are the numbers 0,1,1,2,3,5,8,13,21,... where each is the sum of the previous two. Initialize range to 0 and x, y to be the first two Fibonacci numbers as in:

x = 0

y = 1

range = 0

**Answer:**

x = 0

y = 1

range = 0

while range \&lt; 10 do

print(x)

x, y = y, x + y

range = range +1

end

**Output:**

0

1

1

2

3

5

8

13

21

34