# Learning_Javascript
Welcome to my javascript learning repo!
I will be uploading my notes as I'm learning JS from scratch, my goal is to learn front-end and transition into blockchain development.
Learning Git and Github to create a healthy repository for all the projects that will be created.
My previous experience is basic python knowledge so I'm comfortable with programming concepts such as variables, loops and conditionals. 
Javascript notes
Lines are ended with ; (not necessary but good practice for readability)

Data types:
•	Undefined
•	Null: Nothing
•	Boolean: True False
•	String: text
•	Symbol: immutable primitive unique value
•	Number
•	Object: Can store key value pairs

3 ways to declare variables:
1.	Let ourname = “freeCodeCamp”
2.	const pi = 3.14
3.	var myName = “Beau”
note: Capitalization is important, “Code” is not the same as “code”, recommended to use camelCase: “properCamelCase”
You can declare or assign a variable:
Declare: var a;
Assign: var b = 2;

Initializing a variable to an initial value at the same time its declared.
var a = 4;

Incrementing and Decrementing
++ or --
var myVar = 98;
myVar++;
console.log(myVar)
99

Augmented Math Operations:
Adding to an existing variable can be done with a += 5;
This type of operations supports “+ - * /”
var a = 3;
a = a + 12;      is the same as saying  a += 12;

Escape Character:
When you try to write “” inside a “string”, you add \ before “.
var myStr = “I am a \”double quoted\” string inside \”double quotes”
console.log(myStr)

Strings:
Quoting Strings with Single Quotes:
Starting with single quotes ‘ instead of double quotes “ makes it easy to avoid escaping character.
Using backticks .'. (alt + 96) makes possible using ‘ and “ inside a string.

Concatenating strings:
var ourStr = “I come first. “ + “I come second.”;
Can also be concatenated using the += operator
var ourStr = “I come first.”;
ourStr += “I come second.”;

Concatenating strings to variables
var ourName = “sharp”;
var ourStr = “Hello, our name is” + ourName + “, how are you?”;

Append variables to string
Using the += operator, two variables containing strings can be appended.
var anAdjective = “awesome!”;
var ourStr = “freeCodeCamp Is”;
ourStr += anAdjective;

Length of a string
Using the .length operator
var firstName = “ada”l
firstNameLength = firstName.length;

Bracket Notation:
To select a letter of a string the bracket notation is used firstName[0];
firstName[0] represents the first letter of the string.

Arrays:
An array allows us to collect items of any data type.
var ourArray = [“John”, 23];

Nested array:
An array inside an array:
var ourArray = [[“the universe”, 42], [“cat”, 22]];

Accessing an array:
Same as python:
var ourArray = [[“the universe”, 42], [“cat”, 22]];
ourArray[index]

Accessing multi-dimensional arrays:
var myArray = [[1,2,3], [4,5,6], [7,8,9], [[10,11,12], 13, 14]];

.Push():
The .push() method adds one or more elements to the end of an array and returns the new length of the array.
An array can be pushed into another one.

.pop():
Remove the last element of an array, storing this element to the new variable.
Var ourArray = [1,2,3];
Var removedFromOurArray = ourArray.pop();
Console.log(ourArray)  // the result is [1,2]
Console.log(removedFromOurArray)  // the result is [3] 

.shift():
Remove the first element of an array, storing this element to the new variable.
Var ourArray = [1,2,3];
Var removedFromOurArray = ourArray.pop();
Console.log(ourArray)  // the result is [1,2]
Console.log(removedFromOurArray)  // the result is [3] 

.unshift():
Add an element to the beginning of an array and returns the new length of the array.

Functions:
Syntax is:
function myFunction(arguments or placerholder) {code to be executed by the function}
To run the function:
console.log(myFunction(arguments or placerholder) {code to be executed by the function}

Functions with arguments
A function that has placeholder for data input, they are the variables used in the operations.
Syntax is:
function argFunction(a, b) { 
console.log(a-b);} 
console.log(argFunction(10, 5))  /// Calling the function the parameters are 10 and 5

Global variables:
Variables made in the body of the code (not inside a function) are usable in the whole code.
You can create global variables within a function by declaring without the var keyword and indentation, for example:
function func1() {
	myGlobalVar = 5;
}

Local variables:
Variables which are declared within a function, as well as the parameters have a local scope:

Return statement:
Used to return the result of an operation from a function, the difference with console.log() is that con.log() only prints the result, nothing can interact with it, function’s return on the other hand, gives a tangible, usable object that can interact with the rest of the code. 

If statements:
Used to make decisions in code, it tells javascript to execute the code under certain condicions inside a parenthesis. After the {}, the else part of the conditional is written the sintax goes this way:
if (isItTrue) {           
code to be executed if true;   /// IF true
}
code to be executed if not true;    /// IF not true
Else Statement:
Used after the if statement to define what happens if the statement returns false.
Var result = “”;
If (val > 5) {
	result = “Bigger than 5”;
} else {
	result = “5 or Smaller”;
}
Return result

Else if Statement:
Used to chain several if statements, it cannot be placed at the end of the chain unless it contains other condition. Else is used to express every other possible output does this.
function testeElseIf(val) {
    if (val > 10) {
        return "Greater than 10"
    } else if (val < 5) {
        return "Smaller than 5"
    } else {
        return "Between 5 and 10"
    }
}

console.log(testeElseIf(5))

Switch Statement:
Used to compare a value given (strictly), you have cases for each possible answer. Multiple cases can be used, after every case, break must be used or it will jump straight to the next case.
function caseInSwitch(val) {
    var answer = "";
    switch (val) {
        case 1:
            answer = "alpha";
            break;
        case 2:
            answer = "beta";
            break;
    }

    return answer;
}

console.log(caseInSwitch(1));
Default option in Switch Statement:
When no case gets triggered, a default option is used to represent everything else.
function caseInSwitch(val) {
    var answer = "";
    switch (val) {
        case 1:
            answer = "alpha";
            break;
        case 2:
            answer = "beta";
            break;
        default:
            answer = "other";
    }

    return answer;
}

console.log(caseInSwitch(5));


Comparison Operators:
Equality Operator:
Used to compare, if something is equal, greater or smaller than, a == is used to compare.
A common mistake is using = which is an assignment operator.
function testEqual(val) {
	if (val == 12) {
		return “Equal”;
	}
	Return “Not Equal”;
}

Console.log(testEqual(10));   // This line is calling the function with 10, as it is not == to 12, it returns the false statement.

Strict Equality Operator:
Used to evaluate the truth more strictly based on type of variable as well.
3 == “3”  would be true because it converts the type of variable to match
3 === “3” would be false because it doesn’t convert the data type.

Inequality Operator:
The opposite of the equality operator represented as != and can be read as not equal to.

Strict Inequality Operator:
The opposite of the strict equality operator represented as !==, checks if condition is not true and it does not convert variable type.

Logical Operator:
>, <, >=, <=

And Operator:
To evaluate a value between two conditions, for example, greater than 10 and lesser than 20.
Represented with &&.
If (val < 20 && val >10) {
	return “Yes;
}
Return “No”;
}

Or Operator:
function testLogicalOr(val) {
if (val  < 10 || val >20) {
	return “Outside”;
}
Return inside;
}
Returning Boolean Values from Functions:
When we want the Boolean value from a comparison or statement, the following example will illustrate this better.
function isLess(a, b) {
    return a < b;
}

console.log(isLess(10, 15))

The system prints True because 10 is less than 15.

Objects
Similar to arrays, they are used to store data but instead of indexes, we use properties In a key:value pair. The key is the property

var ourDog = {
    "name": "Camper",
    "legs": 4,
    "tails": 1,
    "friends": ["everything!"]
};

Accessing objects with Dot Notation:
To access a value, you must use varName.property;
For example:
var ourDogName = ourDog.tails;
console.log(ourDogName)
returns 1.

Accessing objects with Bracket Notation:
Similar to dot notation, bracket notation has the following syntax
var testObj = {
    "an entree": "hamburger",
    "my side": "veggies",
    "the drink": "water"
}

var entreeValue = testObj["my side"]
console.log(entreeValue)
returns hamburger
Can be used at any time but it is required when the name has a space in it.




