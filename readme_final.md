# BudgetBuddy Final CSP Project
BudgetBuddy is a simple budget tracking application built with SwiftUI. Users can add expenses, view their total spending, and compare it to a fixed budget limit.
Features
Add expenses with a name and amount
Display total expenses in real time
Compare spending against a predefined budget
Show a budget status message ("Within Budget" or "Budget Exceeded")
Clean and beginner-friendly SwiftUI interface
Technologies Used
Swift
SwiftUI
State Management with @State
NavigationStack
List and Form Components
How It Works
Users enter an expense name and amount, then add it to the expense list. The app automatically calculates the total expenses and checks whether the spending remains within the budget limit of $1000.
Learning Objectives
This project demonstrates:
Swift structures and data modeling
Arrays and list management
User input with TextFields
State management in SwiftUI
Functions and basic calculations
Conditional UI updates
import SwiftUI

struct Expense: Identifiable {
    let id = UUID()
    let name: String
    let amount: Double
}

struct ContentView: View {
    
    @State private var expenses: [Expense] = []
    
    @State private var itemName = ""
    @State private var itemAmount = ""
    
    let budget = 1000.0
    
    var body: some View {
        
        NavigationStack {
            
            VStack(spacing: 20) {
                
                Text("BudgetBuddy")
                    .font(.largeTitle)
                    .bold()
                
                Text("Budget: $\(Int(budget))")
                
                Text("Total: $\(Int(totalExpenses()))")
                
                if totalExpenses() > budget {
                    Text("Budget Exceeded!")
                        .foregroundColor(.red)
                        .bold()
                } else {
                    Text("Within Budget")
                        .foregroundColor(.green)
                        .bold()
                }
                
                TextField("Expense Name", text: $itemName)
                    .textFieldStyle(.roundedBorder)
                
                TextField("Amount", text: $itemAmount)
                    .textFieldStyle(.roundedBorder)
                
                Button("Add Expense") {
                    
                    let newExpense = Expense(
                        name: itemName,
                        amount: Double(itemAmount) ?? 0
                    )
                    
                    expenses.append(newExpense)
                    
                    itemName = ""
                    itemAmount = ""
                }
                .buttonStyle(.borderedProminent)
                
                List {
                    ForEach(expenses) { expense in
                        HStack {
                            Text(expense.name)
                            Spacer()
                            Text("$\(Int(expense.amount))")
                        }
                    }
                }
            }
            .padding()
        }
    }
    
    func totalExpenses() -> Double {
        
        var total = 0.0
        
        for expense in expenses {
            total += expense.amount
        }
        
        return total
    }
}
