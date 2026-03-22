# AP CSP Topics Notes – Swift Examples 

# 3.6 Conditionals
Explanation:
Conditionals let the program make decisions. The program checks if something is true and does one thing or another.
Swift Example:
let score = 70
if score >= 50 {
    print("Pass")
} else {
    print("Fail")
}

# 3.7 Nested Conditionals
Explanation:
Nested conditionals are if statements inside another if statement. They let the program check more than one condition.
Swift Example:
let score = 70
if score >= 50 {
    if score >= 90 {
        print("Excellent")
    } else {
        print("Good")
    }
} else {
    print("Fail")
}

# 3.8 Iteration
Explanation:
Iteration is repeating a block of code multiple times. Loops are used for iteration.
Swift Example:
for i in 1...5 {
    print("Step \(i)")
}

# 3.9 Developing Algorithms
Explanation:
Algorithms are step-by-step instructions to solve a problem. They help the program know what to do in order.
Swift Example (pseudo-code style):
1. User chooses rock, paper, or scissors
2. Computer chooses randomly
3. Compare user and computer choices
4. Show result on screen
   
# 3.10 Lists

Explanation:
Lists (arrays) store multiple values together. They make programs easier to manage.
Swift Example:
let choices = ["🪨", "📄", "✂️"]
let randomChoice = choices.randomElement()!
print(randomChoice)

# 3.11 Binary Search
Explanation:
Binary search finds an item in a sorted list faster than checking every element.
Swift Example (simplified):
let numbers = [1,2,3,4,5,6,7]
let target = 5
// binary search idea: check middle, go left or right

# 3.12 Calling Procedures
Explanation:
Procedures are blocks of code that do something and can be called whenever needed.
Swift Example:
func sayHello(name: String) {
    print("Hello \(name)")
}

sayHello(name: "Ipek")
