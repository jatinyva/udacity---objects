# udacity---objects

Using the umbrella example from the previous video, see if you can follow the example open() method and create the close() method. It's alright if you have trouble at first! We'll go into more detail later in this lesson.

var umbrella = { 
  color: "pink",
  isOpen: false,
  open: function() { 
    if (umbrella.isOpen === true) {
      return "The umbrella is already opened!";
    } else {
      umbrella.isOpen = true;
      return "Julia opens the umbrella!";
    }
   }
};
TIP: Remember to put all of your object's properties and methods inside curly braces: var myObject = { greeting: "hello", name: "Julia" };. Also, remember that an object is just another data type. Just like how you would put a semicolon after a string variable declaration var myString = "hello";, don't forget to put a semi-colon at the end of your object's declaration.

/*
 * Programming Quiz: Umbrella (7-1)
 */

var umbrella = {
    color: "pink",
    isOpen: true,
    open: function() {
        if (umbrella.isOpen === true) {
            return "The umbrella is already opened!";
        } else {
            umbrella.isOpen = true;
            return "Julia opens the umbrella!";
        }
    },
    // your code goes here
    
    close: function() {
       if (umbrella.isOpen === false) {
           return "The umbrella is already closed!";
           
       } else {
           umbrella.isOpen = false;
           return "Julia closed the umbrella!";
       }
    }
};


Create a breakfast object to represent the following menu item:

The Lumberjack - $9.95
eggs, sausage, toast, hashbrowns, pancakes
The object should contain properties for the name, price, and ingredients.

/*
 * Programming Quiz: Menu Items (7-2)
 */

// your code goes here
var breakfast = {
    name: "The Lumberjack",
    price: "$9.95",
    ingredients: ["eggs","sausage","toast","hashbrowns","pancakes"]
};


Using the given object:

var savingsAccount = {
  balance: 1000,
  interestRatePercent: 1,
  deposit: function addMoney(amount) {
    if (amount > 0) {
      savingsAccount.balance += amount;
    }
  },
  withdraw: function removeMoney(amount) {
    var verifyBalance = savingsAccount.balance - amount;
    if (amount > 0 && verifyBalance >= 0) {
      savingsAccount.balance -= amount;
    }
  }
};
add a printAccountSummary() method that returns the following account message:

Welcome!
Your balance is currently $1000 and your interest rate is 1%.


 * Programming Quiz: Bank Accounts 1 (7-3)
 */

var savingsAccount = {
    balance: 1000,
    interestRatePercent: 1,
    deposit: function addMoney(amount) {
        if (amount > 0) {
            savingsAccount.balance += amount;
        }
    },
    withdraw: function removeMoney(amount) {
        var verifyBalance = savingsAccount.balance - amount;
        if (amount > 0 && verifyBalance >= 0) {
            savingsAccount.balance -= amount;
        }
    },
    // your code goes here
    printAccountSummary() {
   return("Welcome!\nYour balance is currently $"+savingsAccount.balance+" and your interest rate is "+ savingsAccount.interestRatePercent+"%."); 
  },
    };

console.log(savingsAccount.printAccountSummary());


Create an object called facebookProfile. The object should have 3 properties:

your name
the number of friends you have, and
an array of messages you've posted (as strings)
The object should also have 4 methods:

postMessage(message) - adds a new message string to the array
deleteMessage(index) - removes the message corresponding to the index provided
addFriend() - increases the friend count by 1
removeFriend() - decreases the friend count by 1


*
 * Programming Quiz: Facebook Friends (7-5)
 */

// your code goes here
var facebookProfile = { 
    name:"Jatin",
    friends : 100,
    messages : ["hey","message"],
    postMessage: function postMessage(message){
        facebookProfile.messages.push("Fourth message");
    },
        deleteMessage: function deleteMessage(index) {
        facebookProfile.messages.splice(index,1);
  
    },
        addFriend: function addFriend(){
        facebookProfile.friends += 1;
    },    
        removeFriend: function removeFriend(){
        facebookProfile.friends -= 1;    
        }
};
console.log(facebookProfile);


Directions:
Use the forEach() method to loop over the array and print out the following donut summaries using console.log.

Jelly donuts cost $1.22 each
Chocolate donuts cost $2.45 each
Cider donuts cost $1.59 each
Boston Cream donuts cost $5.99 each


/*
 * Programming Quiz: Donuts Revisited (7-6)
 */

var donuts = [
    { type: "Jelly", cost: 1.22 },
    { type: "Chocolate", cost: 2.45 },
    { type: "Cider", cost: 1.59 },
    { type: "Boston Cream", cost: 5.99 }
];

// your code goes here
donuts.forEach(function(element) {
  console.log(element.type + " donuts cost $" + element.cost + " each");
});

