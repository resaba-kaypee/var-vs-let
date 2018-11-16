# var-vs-let
//var keywords overide values of the same variable name
var camper = "James";
var camper = "David";
console.log(camper) // "David"


//let keywords does not allow same variable name
let camper = "James"
let camper = "David" // error duplicate variable declaration

//var
function checkScope(){
var i = "function scope"
if(true) {
var i = "block scope"; //overides the previous i "function scope"
console.log("Block scope i is: ", i) 
  }
  console.log(Function scope i is: ", i)
return i;
}

Block scope i is: "block scope";
Function scope i is: "block scope";
checkScope()// "block scope" because i is changed to "block scope"

//let
function checkScope(){
let i = "function scope"; // this is declared outside of if statement (globally)
if(true){
let i = "block scope"; // this is declared inside of if statement block (locally)
console.log("Block scope i is: ", i); //it will return what is inside the block
  }
  console.log("Function scope i is: ", i) // it will return what is outside of the block
  return i;
}

Block scope i is: "block scope";
Function scope i is: "function scope";
checkScope() //function scope because i did not change globally;


//const is a read only
const camper = "james"
camper = "david" // error

// mutate const
const num = [7 ,4, 2];
function editInPlace(){
  num[0] = 2
  num[1] = 4
  num[2] = 7
  return num;
}
