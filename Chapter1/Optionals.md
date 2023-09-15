```` ruby
import Cocoa

/*:
 - När används Optionals? Om man inte vet exempelvis namnet, så kan man spara det som en Optional.
 - Flera exempel på hur och var det används.
 - Var kan jag läsa mer?
 */


//---------------//

var petName: String? //En String som INTE innehåller ett petName.
petName = "Mango" // En String SOM innehåller ett petName.
print(petName) // PetName är nu Mango.
petName = nil // PetName är nu igen nil. Dvs String?

//---------------//

var result: Int? = 30
print(result)

//---------------//

petName = "Mango" // Ändrat petName till Mango igen.
var petAge: Int? = 2 // Satt petAge till en Int? och 2.
var unwrappedPetName = petName! // Unwrappar petName, så det inte längre är en Optional.
print("The pets name is \(unwrappedPetName)") // Printar unwrapped, som inte längre blir en Optional.

//---------------//

if let petName = petName, // Om petName har ett värde.
   let petAge = petAge { // Om petAge har ett värde.
  print("The pet's name is \(petName) and is \(petAge) years old.") // Skriv detta.
} else {
  print("No pet name or age") // Annars skriv detta.
}

//---------------//

var optionalInt: Int? = 10 // Vilket värde Int? ska ha.
var requiredResult = optionalInt ?? 10 //Vilket värde optionalInt ska ha om första är 0.

//---------------//


//: ## Episode 08: Challenge - Optionals

/*:
 ## Challenge 1
 
 You've been provided with a constant below, `hasAllergies`, which has been set to `true`.
 
 Below that, declare a Optional String variable named `dogName`.
 
 On the next line, use a ternary conditional operator to set the value of `dogName` to `nil` if `hasAllergies` is `true`, and to `"Mango"` otherwise.
 */

// TODO: Write solution here
let hasAllergies = true
var dogName: String?
dogName = hasAllergies ? nil : "Mango"

/*:
 ## Challenge 2
 
 Create a constant called `parsedInt` and set it to `Int("10")`. Swift will attempt to parse the string `10` and convert it to an `Int`.
 
 Place your mouse over the constant name and use **Option-Click** to check the type of `parsedInt`. Why is `parsedInt` an optional here?
 */

// TODO: Write solution here
let parsedInt = Int("10")
// Vi har deklarerat att det är en Int.


/*:
 ## Challenge 3
 
 Create another constant named `newParsedInt` and set it equal to `Int("cat")`.
 
 What will the value of `newParsedInt be? Why?
 
 */

// TODO: Write solution here
let newParsedInt = Int("cat")
// Vi har deklarerat en Int med get tillbaka en String. Dvs det blir nil
