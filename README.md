# var-vs-let
//var keywords overide values of the same variable name
var camper = "James";
var camper = "David";
console.log(camper) // "David"


//let keywords does not allow same variable name
let camper = "James"
let camper = "David" // error duplicate variable declaration

