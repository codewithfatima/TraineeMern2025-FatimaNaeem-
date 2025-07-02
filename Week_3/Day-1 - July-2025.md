
### Week 3: if and else statement in javasscript
 - If  Means  if  acondition  is  true  the  execute  some  code  if 
   Notification, do  something  else.**

## 1. checked property

**that  determins  the  checked  state  of  an  HTML  character  or  radio  button  Element..**


## 2. ternary operator 

**A  shortout  to  if() and  else() statements  helps  to  assign  a  varaiable  on  a
condition  condition  ?  codeIsTrue  :  codeIsFalse**

**Examples.*
let age;
const myText = document.getElementById(‘myText’);
const mysubmitBtn = document.getElementById(‘mysubmitBtn’);
const result = document.getElementById(‘result’)
mysubmitBtn.onclick = function () {
age = myText.value;
age = Number(age);
if (age > 100) {
result.textContent = Your are Too old to enter in this site..;
} else if (age == 0) {
result.textContent = You can't enter , You juist born ..;
} else if (age >= 18) {
result.textContent = You are old engouh to enter this site.;
} else if (age < 0) {
console.log(“Your age can’t be below than 0…”);
} else {
console.log(‘Your age needs to be 18+ to enter this site…’)
}
}

## String slicing = creating a substring from a portion of another string.. String.slice(strart, end)

# paratice ::

**e.g1**
const  fullName  =  'Fatima Naeem';
let  firstName  =  fullName.slice(0, 6);
let  lastName  =  fullName.slice(7);
console.log(firstName);
console.log(lastName);
let  lastChar  =  fullName.slice(0, 1);
console.log(lastChar)

 **e.g2**
 const  email  =  'new@gmail.com';
let  extension  =  email.slice(email.indexOf("@"))
let  usernames  =  email.slice(0, email.indexOf("@"))
console.log(usernames);
console.log(extension)

## Method chaining in js = calaling one method after another in one continuous line

**

let  usernamess  =  window.prompt('Enter your name ');
usernamess  =  usernamess.trim();
let  letter  =  usernames.charAt(0);
letter  =  letter.toUpperCase();
console.log(usernamess)
usernamess  =  usernamess.trim().charAt(0).toUpperCase  +  usernamess.slice(1).toLowerCase();


## Strict quality operation in js

 1. = assignment operator 
 2.  == comparison operator (compare if valus are equal')
 3. === strict eaulity operator (compare if values & datatype are equal)  
 4. != inequality operator 
 5.  !== strict inequality operator   
 6. = (Assignment Operator)

1) 👉 Used to assign a value to a variable.
let  nameOfYou  =  "Fatima";
console.log(nameOfYou);

## 2️⃣ == (Equality / Comparison Operator)

**
 👉 Compares values only, not data types. If values are the same after type conversion, it returns true.
console.log(5  ==  "5");
console.log(0  ==  false);
console.log(null  ==  undefined);

## 3️⃣ === (Strict Equality Operator)

**
👉 Compares both value and data type. No type conversion happens.
console.log(5  ===  "5");
console.log(5  ===  5);
console.log(true  ===  1);
  

 **

## 4️⃣ != (Inequality Operator)

**
 👉 Checks if values are not equal, ignoring data type.
console.log(5  !=  "5");
console.log(3  !=  4);
console.log(false  !=  0);

 **

## 5️⃣ !== (Strict Inequality Operator

**
 👉 Checks if either value or data type is not equal.
console.log(5  !==  "5");

console.log(3  !==  3);

console.log(false  !==  0);


## Summary Table 

**

## Operator - Name - Compares - Returns true when

**

**=  -  Assignment – -  -  Value  is  assigned
==  -  Loose  Equality  -  Value  -  Values  are  equal  after  conversion
===  -  Strict  Equality  -  Value  +  Type  -  Values  and  types  are  equal
!=  -  Loose  Inequality  -  Value  -  Values  are  not  equal (after  conversion)
!==  -  Strict  Inequality  -  Value  +  Type  -  Values  or  types  are  not  equal**

Scripting Javascript Fundamentals
In JavaScript, the this keyword refers to the object that is currently executing the function. Its value depends on how a function is called, not where it is defined.

this Inside a Method (Object Function)
const person = {

name : “fatima”,

greet:function(){

console.log(this.name);
}
}

person.greet();

2. Alone in a Function (Non-Strict Mode)
function show() {
console.log(this);
}

show();

3. In an Event Listener
**

Click me

const obj = {
name: “Fatima”,
greet: () => {
console.log(this.name);
}
};
obj.greet();

4 . In Global Scope**
console.log(this)

Tip to Remember:
"this always refers to how the function is called, not where it is written."
