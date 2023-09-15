```` ruby

import Cocoa

/*:
 - När används Booleans(Bool) ?
 - Flera exempel på hur och var det används.
 - Var kan jag läsa mer?
 */


//---------------//

let yes: Bool = true //Man kan skriva såhär.
let yesAgain = true //Eller såhär. Swift vet att det är en Bool.

let no: Bool = false //Man kan skriva såhär.
let noAgain = false //Eller såhär. Swift vet att det är en Bool.


//---------------//

let passingGrade = 50 //Minsta poäng för att vara godkänd, 50 poäng.
let studentGrade = 74 //Poäng som eleven har, 74 poäng.
let studentPassed = studentGrade > passingGrade // Är studentGrade mer än passinGrade. Om sant, då är vi godkända - dvs true.
let studentFailed = studentGrade < passingGrade // Är studentGrade mindre än passinGrade. Om false, då är vi fortfarande godkända.
let sudentPassedAgain = studentGrade >= passingGrade // Vi kan använda >= för att inkludera passingGrade värdet också, dvs 50.

//---------------//

let AndreasGrade = 49 //Andreas poäng på provet.
let ThereseGrade = 99 //Therese poäng på provet.
AndreasGrade == ThereseGrade // Vi kollar om Andreas poäng är samma som Thereses poäng. I detta fallet är de inte samma, dvs false.
AndreasGrade != ThereseGrade // Vi kollar om Andreas poäng är olikt Therese poäng. I detta fallet är de inte samma, dvs true.

//---------------//

let hundNamn = "AB" //Namnet på hunden
let kattNamn = "BC" //Namnet på katten
hundNamn == kattNamn //Är de samma namn? Nej. Dvs false.
hundNamn > kattNamn //Kommer bokstaven A efter B? Nej, dvs false
hundNamn < kattNamn //Kommer bokstaven A efter B? Ja, dvs true.

//---------------//


/*:
 ## Challenge 1
 
 Create a constant named `myAge` and set its value to your age.

 Then, create a constant named `isVotingAge` that uses Boolean logic to determine if the value stored in `myAge` denotes someone of voting age. In my part of the world, the voting age is 18, so I'll use that here.
*/

// TODO: Write solution here

let myAge = 33 //Min ålder
let isVotingAge = myAge >= 18 //Är min ålder, 33 större eller lika med 18. Ja det är den, dvs true.


/*:
 ## Challenge 2
 
 Create a constant named `student` and set its value to your name as a string.
 
 Next, create a constant named `author` and set its value to `"Matt Galloway"`, the original author of these exercises.
 
 Then, create a third constant named `authorIsStudent` that uses string equality to determine if the values of `student` and `author` are equal.
 */

// TODO: Write solution here

let student = "Andreas Poulsen" //Namnet på student, dvs Andreas.
let author = "Matt Galloway" //Namnet på author, dvs Matt Galloway.
let authorIsStudent = student == author // är Andreas Poulsen lika med Matt Galloway, dvs samma. Nej, dvs false.



/*:
 ## Challenge 3
 
 Create a constant named `studentBeforeAuthor` which uses string comparison to determine if the string value in the constant `student` comes, alphabetically speaking, before the string value in the constant `author`.
 
 The constants `student` and an `author` were declared above in Challenge 2, so you do not need to redeclare them here.
 */

// TODO: Write solution here

let studentBeforeAuthor = author > student //Kommer author efter student? Ja, dvs true. < = Innan | = > Efter
