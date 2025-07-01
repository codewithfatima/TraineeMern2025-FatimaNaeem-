### if and else statement in javasscript


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
