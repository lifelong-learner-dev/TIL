# Javascript Part 1

| ```<script>``` | | | |
|:---:|:---:|:---|:---|
| 1   | array | ```// 1. Create an array with a size of 5 let num = new Array(5);``` <br> ```// Store values in each element of the array all at once for (let i = 0; i < num.length; i++) {num[i] = i;}``` <br> ```// Print the values of each element in the array using a loop``` <br> (for loop) <br> ```document.write("num: ");``` <br> ```for (let i = 0; i < num.length; i++) {document.write(num[i] + " ");}```  <br> <br>  ```// 2. Declare an array without a predefined size let player = new Array();```  <br> <br>  ```// Input values for (let i = 0; i < 3; i++) {player[i] = "Player" + (i + 1);}```  <br> <br>  ```// Output values document.write("<br> player: "); for (let i = 0; i < player.length; i++) {document.write(player[i] + " ");} ``` <br> <br>  ```// 3. Declare an array and initialize it with values (method 1) let fish = new Array("Mackerel", "Yellowtail", "Alaska Pollock", "Cod"); ```  <br> <br>  ```// Output values document.write("<br> fish: "); for (let i = 0; i < fish.length; i++) {document.write(fish[i] + " ");}```  <br> <br>  ```// 4. Declare an array and initialize it with values (method 2) let score = [85, 90, 75, 99]; ```  <br> <br>  ```// Output values document.write("<br> score: "); for (let i = 0; i < score.length; i++) {document.write(score[i] + " ");} ```  <br> <br>  ```// 5. When elements in the array have different data types let student = ["John Doe", 4, 93.5, 'A'] ``` <br> <br>  ```// Output values document.write("<br> student: "); for (let i = 0; i < student.length; i++) {document.write(student[i] + " ");} ```|  |
| 2  | break | let i = 0; <br> while (true) <br> { // Infinite loop <br> i += 3; <br> //Since it's an infinite loop, a condition is needed to exit the loop. <br> console.log(i); <br><br> if (i > 20) break; <br>// Exit the loop if i becomes greater than 20. <br> It terminates when i reaches 21. <br> ```document.write(i + "<br>");``` } <br><br> // (1) Ending only the inner for loop  <br>for (let i = 1; i <= 5; i++) { <br> for (let j = 1; j <= 3; j++)<br> { ```document.write(i + " : " + j + "<br>");``` <br> if (j == 2) {break; <br>// Terminate only the inner for loop; <br>the outer for loop continues executing <br> } <br> } <br>} <br> ```document.write("<br>");``` <br><br> // (1) Ending only the inner for loop using a label <br>Outter: for (let i = 1; i <= 5; i++) { <br> for (let j = 1; j <= 3; j++) { <br>  ```document.write(i + " : " + j + "<br>");``` <br>  if (j == 2) {break Outter;  <br>// Terminate only the inner for loop;  <br>the outer for loop continues executing } }}   |  |
| 3  | confirm  | // Using variables to store input values <br>// Variable usage method: Declare with 'let' and store a value <br><br>  let isStudent = confirm("Are you a student?");  <br>// [OK] / [Cancel] buttons <br><br>  // If the [OK] button is pressed,  <br>'true' is returned and stored in the 'isStudent' variable <br><br>  <br>// If the [Cancel] button is pressed,  <br>'false' is returned and stored in the 'isStudent' variable <br><br>  // If the returned value is 'true',  <br>it means the person is a student with a 50% discount <br><br>  // If 'false', <br>it means the person is not a student and there is no discount <br><br>  if (isStudent == true) { <br>    result = "You are a student."; <br>    discount = "50%"; <br>} else { <br>    result = "You are not a student."; <br>    discount = "None"; <br>} <br><br>  document.write("Result: " + result + "<br>"); <br>document.write("Discount: " + discount);|   |
| 4   | const  | // const rate;  <br><br>// Initialization must be done at the time of declaration;  <br>if not, it will result in an error <br><br> const rate = 0.07; <br>rate = 0.17;  <br><br>  // Constants cannot be changed once assigned a value <br>// const.html:11 Uncaught TypeError:  <br>Assignment to constant variable. <br><br>  console.log(rate); |  |
| 5 | continue  | for (let i = 1; i <= 10; i++) { <br> // If 'i' is an odd number, <br> skip statement 1 and continue to the next iteration. <br> // Result: Only even numbers are printed. <br><br> if (i % 2 == 1) { <br> continue; <br> } <br> ``` document.write(i + "<br>");``` // Statement 1 <br>} | This one will be used often. |
| 6  | dataType | let num1 = 15;  <br>// Integer <br><br>  let num2 = 123.45;  <br>// Floating-point number <br><br>  let answer = "y";  <br>// Character <br><br>let name = "John Doe";  <br>// String <br><br>let address = "1 Main Street, City";  <br>// String (single or double quotes can be used) <br><br>  let result = true; // Boolean value <br><br>  let nothing; // Variable declaration without a value <br><br>  // When [Cancel] is clicked, it returns a null value <br>let input = prompt("Data Type Example", "Click the Cancel button"); <br><br>  // 1. Numeric Operations <br>```document.write("<br> Integer * Floating-point: " + num1 * num2);``` <br><br>  // 2. Type Conversion: Floating-point to Integer (123.45 -> 123) <br>document.write( <br>```"<br> Convert Floating-point to Integer: " + parseInt(num2)``` ); <br><br>  // 3. Converting Numbers to Strings:  <br>15 + 123.45 = "15123.45" (String concatenation) <br>document.write( <br>```"<br> Convert Numbers to Strings: " + String(num1) + num2.toString()``` <br>); <br><br>  // 4. String * String: NaN  <br>(Not a Number: not a valid numeric operation) <br>```document.write("<br> String Multiplication: (NaN output)" + name * address);``` <br><br>  // 5. When the 'nothing' variable is declared  <br>but not assigned a value <br>// 'undefined': Indicates the type is unknown,  <br>and there's no value. <br>```document.write("<br> 'nothing' Variable: " + nothing);``` <br> <br> // 6. When [Cancel] is clicked in the prompt() dialog <br>// 'null': Signifies the absence of a reference object  <br>or value when none is provided. <br> ```document.write("<br> 'input' Variable: " + input);``` |  |
| 7  | doWhile | let count = 0; // Initialize a counter variable to 0 <br><br> do { <br> count++; // Increment the counter <br><br> alert("Warning " + count); <br> // Display a warning message with the current count <br><br> answer = confirm( <br>"Do you want to continue showing the warning window?"); <br>// Ask the user if they want to continue <br><br> } while (answer); <br>// Continue looping as long as 'answer' is true (user wants to continue) <br><br>  document.write("Number of Warning Alerts Shown: " + count);  <br>// Display the total number of warning alerts shown |  |
| 8 | for | let fruits = ["apple", "grape", "peach"]; <br><br>+ for <br>let sum = 0; <br>// Initialize a variable 'sum' to store the cumulative sum <br>//When 'i' increases by 2, the for loop is written as ' <br>for(let i=1; i<=10; i+=2) <br><br>  for (i = 1; i <= 10; i++) { <br>    ```document.write("i =" + i + "<br>"); ``` <br>// Display the current value of 'i' <br>// 'sum = sum + i' or 'sum += i': <br>Add the current value of 'i' to the cumulative sum <br>    sum += i;  <br>// Using the cumulative assignment operator <br>} <br><br>  ```document.write("Final value of 'i': " + i + "<br>");```  <br>// Display the final value of 'i' <br>document.write("Final value of 'sum': " + sum);  <br>// Display the final cumulative sum+ forEach() <br>fruits.forEach(function (item, index, array) { <br> console.log(item, index, array);}); <br><br>  // First parameter: Items of the array <br>// Second parameter: Index of the array <br>// Third parameter: The array itself <br>// Parameter names can be chosen arbitrarily <br>// The order of passed parameters is predetermined. <br><br>  ```+ for in``` <br> ```for (let fruit in fruits) {document.write(fruits[fruit] + "<br>");``` <br><br>  // Print the values of each element in the array <br>// Iterate through each element in the 'fruits' array <br>// Store each element in the variable 'fruit' along with its index <br><br>  + for nested <br>for (let i = 1; i <= 3; i++) { <br>  for (let j = 1; j <= 5; j++) { <br> document.write(j + " "); <br> } <br> ```document.write("<br>")```<br> } |  |
| 9  | hoisting | Refers to using a variable before it's declared in the code. <br><br>'var' allows this in some cases, <br> but it's not recommended. <br><br>'let' results in an error. |  |
| 10 | if | let a = prompt("Enter number 1"); <br>let b = prompt("Enter number 2"); <br>let c = prompt("Enter number 3"); <br><br>  // Check which of the three numbers is the largest <br>let max = a; <br>if (b > max) max = b; <br>if (c > max) max = c; <br><br>  // Display the maximum value <br>document.write('Maximum value: ' + max); <br><br>  -------------------------------------------------------------------------------------------- <br><br> // Define a predefined ID and password for comparison <br>let id = "abcd"; <br>let password = "1234"; <br><br> // Prompt the user to input their ID and password <br>let input_id = prompt("Please enter your ID"); <br>let input_password = prompt("Please enter your password"); <br><br>  //Check if the input ID and password match the predefined values <br><br>  if (input_id === id && input_password === password) { <br>// If they match, display a success message <br> document.write("Login successful"); <br>} else { <br>// If they don't match, show an alert and display a failure message <br> alert("ID or password does not match."); <br> document.write("Login failed"); <br>} <br><br>  -------------------------------------------------------------------------------------------- <br><br> let id = "abcd"; <br>let password = "1234"; <br><br> let input_id = prompt("Please enter your username"); <br>let input_password = prompt("Please enter your password"); <br><br> if(input_id == id && input_password == password){ <br> alert("Welcome, " + id + "!"); <br><br> let answer = prompt("What is the capital of South Korea?"); <br> if (answer == "Seoul") { <br>        document.write("Correct answer."); <br>} else { <br>        document.write("Incorrect. The capital of South Korea is Seoul."); <br> } <br><br> } else { <br> alert("Username or password does not match."); <br> document.write("Exiting."); <br>} | |
| 11  | let-var | let sum = 0; <br><br> // Using 'var' to declare 'i' within the 'for' loop <br>for (var i = 0; i < 10; i++) { <br> sum = sum + i; <br>} <br><br>  console.log(i); // 'i' is accessible outside the 'for' block <br><br>  sum = 0; <br>// Using 'let' to declare 'j' within the 'for' loop <br>for (let j = 1; j <= 10; j++) { <br> sum = sum + j; <br>} <br><br>  console.log(j); <br>// Error: 'j' is not defined outside the 'for' block <br>// Uncaught ReferenceError: j is not defined <br><br>  --------------------------------------------------------------------------------------------- <br><br>  // Using 'var' - Allows redeclaration of the same variable name <br>var name = "Mr.Kim"; <br>```document.write(name + "<br>");``` <br><br>  var name = "Mr.Lee"; <br>```document.write(name + "<br>");``` <br>// Attempting to redeclare a 'let' variable with the same name resu <br> lts in an error <br>let name = "Ms.Kim"; <br>```document.write(name + "<br>");``` <br>// Uncaught SyntaxError: <br> Identifier 'name' has already been declared <br>// An error occurs because 'name' has already been declared <br><br> // Using 'let' - Does not allow redeclaration  <br> of the same variable name <br>let address = "Seoul"; <br>let address = "Jeju";// Error: Cannot redeclare 'address' <br>// An error occurs because 'address' has already been declared <br>console.log(address); <br><br>  var address = "Seoul"; // Hoisting moves 'var' declarations to the top <br>console.log(address); <br>let address = "Seoul"; // Error: Cannot redeclare 'address' <br>// An error occurs because 'address' has already been declared | |
| 12 | operators | // 1. Increment/Decrement Operators: ++, -- <br>let count = 0; <br><br>  // Can be used alone; position doesn't matter <br>// count++; <br>++count; <br>console.log(count); <br><br>  // Pay attention to position <br>let x = 10; <br><br>  // Post-increment: First assign x (10) to y, then increment x by 1 <br>// let y = x++; <br><br>  // Pre-increment: First increment x by 1,  <br>then assign the updated value to y <br>let y = ++x; <br><br>  console.log(y); <br>console.log(x); <br><br>  // 2. Logical NOT Operator: ! <br>let a = true; <br>let b = !a; <br><br>  console.log(b); <br><br>  // 3. Relational Operators (Comparison Operators) <br>let n1 = 10; <br>let n2 = 20; <br><br>  console.log(n1 > n2);  // false <br>console.log(n1 != n2); // true <br>console.log(n1 == n2); // false <br><br>  // 4. Logical Operators: &&, \|\| <br>let num = 17; <br><br>  console.log(num % 3 == 0 \|\| num % 4 == 0); <br>// true if divisible by 3 or 4 <br><br>  num = 15; <br>console.log(num > n1 && num > n2); // false <br><br>  // 5. Ternary Operator (Conditional Operator): ?: <br>let score = 95; <br>let result = (score > 60) ? 'PASS' : 'FAIL'; <br>console.log(result); <br><br>  // Nested Ternary Operator <br>score = 85; <br>let grade = (score > 90 ? 'A' : (score > 80) ? 'B' : 'C'); <br>console.log(grade); <br><br>  // 6. Compound Assignment Operators <br>let sum = 10; <br>let n = 20; <br><br>  // Equivalent to: sum = sum + n; <br>sum += n; <br>console.log(sum); // 30 | |
| 13 | prompt  | // Declare a variable  <br>and store the value entered in the prompt() function <br><br>  let answer = prompt("What is your favorite fruit?"); <br>document.write("Your favorite fruit is " + answer + "."); <br><br>  ------------------------------------------------------------------------------------------- <br><br>  /* <br>  Multiline comment <br>*/ <br>// Single-line comment <br>let pay_card = confirm("Would you like to pay with a card?"); <br><br>  if (pay_card == true) { <br>  let num_card = prompt("Please enter your card number.", "xxxx-xxxx-xxxx-xxxx"); <br>  document.write("Card number: " + num_card + "."); <br>} else { <br>  document.write("You are not paying with a card."); <br>} | |
| 14 | switch | let input = prompt("Please enter a number", "1 or 2 or 3"); <br><br>  // The value received from prompt() is treated as a string <br>switch (input) { <br> case "1": ```document.write("<img src='image/lizard.png'>");``` <br> case "2": ```document.write("<img src='image/lizardon.png'>");``` break; <br> case "3": ```document.write("<img src='image/megalizardon.png'>");``` break; <br> default: alert("You entered an incorrect value"); <br>// In case a value other than 1, 2, or 3 is entered <br>} | |
| 15 | typeConversion | /*Values received from the prompt() function are treated <br> as strings. <br> When performing operations: <br> + is a string concatenation operator, <br>  so it concatenates two strings. <br> * does not apply to string operations, <br> so it automatically performs <br> numeric operations (automatic type conversion). <br>*/ <br><br>  /* Type conversion is possible only when the value is <br> in a numeric format. <br> Non-numeric strings cannot be converted. <br> "Hong_gil_dong": Cannot be converted to a number <br> (+: string concatenation / *: NaN, not a number) <br> "a": Cannot be converted to a number <br> "123": Conversion is possible <br> "123.45": Conversion is possible <br>*/ <br><br>  // (1) Without type conversion: Input is treated as a string <br>let num1 = prompt("Enter number 1"); <br>let num2 = prompt("Enter number 2"); <br><br> // Arithmetic operations <br>```document.write(num1 + num2 + "<br>");``` <br>// String concatenation (+: concatenation) <br>document.write(num1 * num2);  <br>// Automatic type conversion to numeric <br><br> // (2) With type conversion: Input is converted to an integer <br>// let num1 = parseInt(prompt("Enter number 1")); <br>// let num2 = parseInt(prompt("Enter number 2")); <br><br>  // // Arithmetic operations <br>```// document.write(num1 + num2 + "<br>"); // Numeric operation``` <br>// document.write(num1 * num2); <br><br>  // (3) With type conversion: Input is converted <br> to a floating-point number <br>// let num1 = Number(prompt("Enter number 1")); <br>// let num2 = Number(prompt("Enter number 2")); <br><br>  // // Arithmetic operations <br>// document.write(num1 + num2 + "<br>");  <br>// Numeric operation <br>// document.write(num1 * num2);  <br>// Recognized as numbers (automatic type conversion) |  |
| 16  | variable | variables <br><br> // Explicit declaration <br>let num = 10, pi = 3.14; <br>let ch = 'a'; <br>let name = "Hong_gil_dong"; <br><br>  // Implicit declaration with direct value assignment <br>address = "Seoul 1st street"; <br>nation = 'South Korea';  <br>// Both single and double quotes can be used for strings <br><br>  // Output variable values <br>console.log(num); <br>console.log(pi); <br>console.log(ch); <br>console.log(name); <br>console.log(address); <br>console.log(nation); <br><br>  // Concatenate variables with strings and display <br>```document.write("Name: " + name + "<br>");``` <br> document.write("Address: " + address);--------------------------------------------------------------------------------------------- <br>variable_global <br><br> // Variables declared in this area are global variables <br> whether you use let/var or not. <br>let x = 5, y = 10; // Explicit declaration with let: global variable <br>total = 0; // Declaration without let: global variable <br><br> // Function 1 scope <br>function f1() { <br> // Can use global variables <br> x = x + y; <br> ```document.write(x + "<br>");``` <br>} <br><br> // Function 2 scope <br>function f2() { <br> // Can use global variables <br> total = x + y; <br> document.write(total + "<br>"); <br>} <br><br> // Variables declared here are also global <br> because they are not inside a function. <br>let name = "Kim"; <br><br> // Function calls (using functions) <br>// Functions won't do any work unless they are called. <br>// To execute a function, it must be called. <br>// Calling: Simply write the function name. <br>f1(); <br>f2(); <br><br> // Global variables can be accessed here <br>```document.write("x: " + x + "<br>");``` <br>  ```document.write(name + "<br>");``` <br><br>  function showName() { <br> // Can use global variables <br> document.write("Name: " + name); <br>} <br><br> showName(); <br><br>  -------------------------------------------------------------------------------------------- <br><br> variable_local <br><br>  //Local variables:Variables declared with let/var inside a function <br>function f1() { <br> let localVar1 = 100; <br>//Variable declared with let inside the function: Local variable <br>//Local variable: Can only be used within the function f1() <br> name = "Hong_gil_dong"; <br>//Variable declared without let inside the function: Global variable <br>} <br><br> function f2() { <br> // Cannot access the local variable localVar1 declared <br> in f1(): Error <br> // document.write(localVar1); <br> // Uncaught ReferenceError: localVar1 is not defined <br> // Global variable name can be accessed <br> document.write(name); <br>} <br><br>  // Function calls <br>f1(); <br>f2(); |  |
| 17  | while  | // Initialization is mandatory <br>let i = 1; <br><br>  while (i <= 5) { // Condition <br> ```document.write(i + "<br>")```; <br> // Increment or decrement must be set <br> i++; <br>} <br> document.write("End"); <br><br>  -------------------------------------------------------------------------------------------- <br><br> let num = parseInt(prompt("Enter a number")); <br> let count  = 1; <br>         while (count <= num) { <br> if (count % 3 == 1) { <br> ```document.write("<img src='image/cherry.png'>")```<br> } else if (count % 3 == 2) { <br> ```document.write("<img src='image/bomb.png'>")``` <br> } else { <br> ```document.write("<img src='image/apple.png'>")``` <br> } <br> count++; <br> } <br><br>  -------------------------------------------------------------------------------------------- <br><br> let num = parseInt(prompt("Enter a number")); <br> let count = 1; <br>         while (count <= num) { <br> switch (count % 3) { <br> case 1: <br> ```document.write("<img src='image/cherry.png'>");``` <br>  break; <br> case 2: <br> ```document.write("<img src='image/bomb.png'>");``` <br> break; <br> case 0: <br> ```document.write("<img src='image/apple.png'>");``` <br> break; <br> } <br> count++; <br> } |  |
| 18  | write | // The head part is displayed first <br><br> // Using document.write() to display content <br>document.write("hello"); <br>document.write("<h3>Title</h3>");  <br>// HTML tag effect applied <br><br>  // Using console.log() to display content <br>console.log("hello2"); <br>console.log("<h3>Title2</h3>")  <br>// HTML tag effect not applied, <h3> is treated as a string <br>// "<h3>Title2</h3>" is printed as-is |  |
| ```</script>``` | | | |