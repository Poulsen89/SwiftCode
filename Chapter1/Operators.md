```` ruby
import Cocoa

/*:
 - När används Logical Operators ? Bara vid Booleans.
 - Flera exempel på hur och var det används.
 - Var kan jag läsa mer?
 */


//---------------//

let passingGrade = 50
let studentGrade = 50
let chrisGrade = 49
let samGrade = 99

let studentPassed = studentGrade >= passingGrade // Är studentGrade(50) högre eller lika med passingGrade(50)
let chrisPassed = chrisGrade >= passingGrade // Är chrisGrade(49) högre eller lika med passingGrade(50)
let samPassed = samGrade >= passingGrade // Är samGrade(99) högre eller lika med passingGrade(50)

samPassed // Klarade sig samPassed ovanför? Ja, dvs true.
!samPassed // Detta betyder motsatsen. Vi säger. !samPassed klarade INTE  det. Men det är ju falskt, för han klarade ju det. Dvs det blir då false.

let bothPassed = chrisPassed && samPassed // Klarade Chris OCH Sam provet? Nej, dvs false.
let everyonePassed = chrisPassed && samPassed && studentPassed // Klarade alla provet? Nej. Dvs false.

let eitherPassed = chrisPassed || samPassed // Klarade Chris ELLER Sam Provet? Sam klarade provet. Ja, dvs true.
let anyonePassed = chrisPassed || samPassed || studentPassed // Klarade någon av alla dessa 3 provet? Ja, dvs true.


//---------------//

let superGrade = 90 // Vi säger att "Super" betyget är minst 90
let samSuperAttendance = true // Vi frågar om Sam har bra närvaro. I detta fallet säger vi ja det har han. Dvs true.
let samGradeAttendance = samSuperAttendance && samGrade > superGrade // Är närvaro sant och är samGrade större än superGrade. Ja, dvs true.

let chrisSuperAttendance = true // Vi frågar om Chris har bra närvaro. I detta fallet säger vi ja det har han. Dvs true.
let chrisGradeAttendance = chrisSuperAttendance && chrisGrade > superGrade // Attendance är true, men inte betyget. Dvs false.

//---------------//

if chrisGradeAttendance {  // Om chrisGradeAttendance är true.
  print("Congratulations!") // Skriv då detta.
} else { print("Try harder next time!") // Om det inte är true, skriv då detta. Dvs false.
}

if samGradeAttendance { // Om samGradeAttendance är true.
  print("Congratulations!") // Skriv då detta.
} else { print("Try harder next time!") // Om det inte är true, skriv då detta. Dvs false.
}

//---------------//

var betterStudent: String // Använder String som value, eftersom jag inte vet vem som är den bättre eleven ännu.
if samGrade > chrisGrade { // Om SamGrade har högre betyg än chrisGrade
  betterStudent = "Sam" // Skriv ut, "Sam"
} else { betterStudent = "Chris" // Om inte, skriv ut "Chris"
}

// Istället för IF Statement, när det bara är 2 värden eller om vill förenkla det.
// Så kan man använda en
// #Ternary Conditinal Operator

var betterStudentNew = samGrade > chrisGrade ? "Sam" : "Chris" // Om SamGrade är högre än chrisGrade, skriv "Sam" annars "Chris".

//---------------//

//: ## Episode 06: Challenge - Logical Operators

/*:
 ## Challenge 1
 
 You've been provided with a a constant named `myAge` below that's already been assigned a value. Feel free to change the value of this constant to match your actual age.

 Use that constant to create an `if-else` statement to print out `"Teenager"` if the value of `myAge` is greater or  than 13 but less than or equal to 19, and to print out `"Not a teenager"` if the value is outside that range.
 */

// TODO: Write solution here
let myAge = 34 // Ålder
if myAge >= 13 && myAge <= 19 { // Om ålder är mer än 13 OCH är mindre än 19
  print("Teenager") // Säg Teenager
} else { // Annars säg
  print("Not a teenager") // Not a teenager
}

/*:
 ## Challenge 2
 Create a constant named `teenagerName`, and use a ternary conditional operator to set the value of `teenagerName` to your own name as a string if the value of `myAge`, declared above, is greater than or equal to 13, but less than or equal to 19, and to set the value of `teenagerName` to `"Not me!"` if the value is outside that range.
 
 Then print out the value of `teenagerName`.
 */

// TODO: Write solution here
let teenagerName = myAge >= 13 && myAge <= 19 ? "Andreas" : "Not me!" //Samma som ovanför, bara att jag använde en Ternary Conditional.
print(teenagerName)
