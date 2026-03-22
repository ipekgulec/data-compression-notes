# Rock-Paper-Scissors SwiftUI App – Explanation 
Purpose:
This app is a Rock-Paper-Scissors game. The user picks rock (🪨), paper (📄), or scissors (✂️), and the computer randomly picks one. The app shows who wins.
1. Data / Properties
choices is a list with ["🪨", "📄", "✂️"].
userChoice stores the user’s pick.
computerChoice stores the computer’s pick.
result shows the game outcome.
The list makes it easier to manage choices and edit the program. Without it, code would be longer and more complex.
2. User Interface (UI)
VStack shows the title, computer’s choice, result, and buttons.
Buttons let the user choose a move and call playGame(choice:).
3. Procedures
a) playGame(choice:)
Sets userChoice, calls randomComputerChoice(), and then determineWinner().
Updates result to show on screen.
b) randomComputerChoice()
Picks a random choice from the list.
c) determineWinner(userChoice:computerChoice:)
Checks if it’s a tie.
Checks winning conditions (rock beats scissors, paper beats rock, scissors beats paper).
Returns “You win!” or “You lose!”.
4. How It Works
User presses a button → playGame runs.
Computer chooses randomly.
Winner is calculated and shown.
5. Why It’s Good
List keeps choices organized.
Procedures prevent repeating code.
Easy to add new choices or change rules.
6. Reflection
This program helps me understand selection and procedures.
It shows how different inputs give different outputs.
Using a list makes editing and updating easy.


// *** Rock-Paper-Scissors SwiftUI App
// *** Author: Your Name
// *** Purpose: Simple game where user plays against computer
// *** AP CSP Create Task – Component A

import SwiftUI

// *** Main ContentView
struct ContentView: View {
    
    // *** Properties / Data
    // List of possible choices (data collection)
    let choices = ["🪨", "📄", "✂️"] // ***

    @State private var userChoice = ""  // user's current choice
    @State private var computerChoice = ""  // computer's current choice
    @State private var result = "Make your move!"  // game result

    // *** Body / UI
    var body: some View {
        
        VStack(spacing: 30) {
            
            Text("Rock Paper Scissors")
                .font(.largeTitle)
                .fontWeight(.bold)
            
            Text("Computer: \(computerChoice)") // show computer's choice
                .font(.title)
            
            Text(result) // show result of the game
                .font(.title2)
                .padding()
            
            // *** Buttons for user input
            HStack(spacing: 20) {
                
                Button(action: {
                    playGame(choice: "🪨") // user chooses rock
                }) {
                    Text("🪨")
                        .font(.largeTitle)
                }
                
                Button(action: {
                    playGame(choice: "📄") // user chooses paper
                }) {
                    Text("📄")
                        .font(.largeTitle)
                }
                
                Button(action: {
                    playGame(choice: "✂️") // user chooses scissors
                }) {
                    Text("✂️")
                        .font(.largeTitle)
                }
                
            }
        }
        .padding()
    }
    
    // *** Game Logic Procedure
    func playGame(choice: String) {
        userChoice = choice
        computerChoice = randomComputerChoice() // call procedure to get random choice
        result = determineWinner(userChoice: userChoice, computerChoice: computerChoice) // call procedure to determine winner
    }
    
    // *** Random Computer Choice Procedure
    func randomComputerChoice() -> String {
        return choices.randomElement() ?? "🪨" // pick random choice from list
    }
    
    // *** Determine Winner Procedure
    func determineWinner(userChoice: String, computerChoice: String) -> String {
        
        if userChoice == computerChoice { // tie condition
            return "It's a tie!"
        }
        
        // winning conditions
        if (userChoice == "🪨" && computerChoice == "✂️") ||
            (userChoice == "📄" && computerChoice == "🪨") ||
            (userChoice == "✂️" && computerChoice == "📄") {
            return "You win!"
        } else {
            return "You lose!"
        }
    }
}

// *** Preview
struct ContentView_Previews: PreviewProvider {
    static var previews: some View {
        ContentView()
    }
}
