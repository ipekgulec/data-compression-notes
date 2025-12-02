# Frog Escape

A clock-based game where a character (😺) moves around a 12-hour clock face. The player taps a button to move the character to a random position. The game has levels, a countdown timer, and increasingly shorter time per level.

**Target Audience:** Kids and casual players  
**Why?:** It’s a fun way to practice timing and reaction skills, with a simple visual design.  
**Design Choices:** The clock face shows character movement without using arrays, and animation makes the movement smooth. Each level increases difficulty by reducing the timer.  
**Hardest Part:** Moving the character randomly without repeating the same position.  
**Timer/Level Logic:** Timer counts down, and when it reaches 0, the level increases and the timer resets to a slightly shorter duration.  
**Learned:** Learned how to map positions to X/Y offsets manually without arrays, and how to use SwiftUI animation with state changes.  
**SwiftUI Features Used:** @State, Timer.publish, onReceive, Button, VStack, ZStack, animation.

# Unplugged to Coding: Cryptography Projects
Encrypted message to solve
/+ |+ /+ \+ **
Decode the message using Pigpen Cipher and find the word.
Correct solution:
HELLO
-Which letter does “-+”represent in Pigpen Cipher?
-Encrypt your first and last name with Pigpen Cipher.
-What steps would you follow to decrypt a Pigpen Cipher message?
-Which symbol represents the E letter in Pigpen Cipher?



import SwiftUI

// Simple Pigpen Cipher
let pigpen: [Character: String] = [
    "A": "+-", "B": "-+", "C": "++",
    "D": "+|", "E": "|+", "F": "||",
    "G": "+/", "H": "/+", "I": "//",
    "J": "+\\", "K": "\\+", "L": "\\\\",
    "M": "+*", "N": "*+", "O": "**",
    "P": "+#", "Q": "#+", "R": "##",
    "S": "+@", "T": "@+", "U": "@@",
    "V": "+>", "W": ">+", "X": ">>",
    "Y": "+<", "Z": "<+"
]


let reversePigpen = Dictionary(uniqueKeysWithValues: pigpen.map { ($1, $0) })

func encryptPigpen(_ text: String) -> String {
    var result = ""
    for char in text.uppercased() {
        result += pigpen[char, default: String(char)] + " "
    }
    return result
}

func decryptPigpen(_ text: String) -> String {
    let parts = text.split(separator: " ")
    var result = ""
    for p in parts {
        result += String(reversePigpen[String(p)] ?? "?")
    }
    return result
}


func main() {
    let message = "HELLO"
    let encrypted = encryptPigpen(message)
    let decrypted = decryptPigpen(encrypted)
    
    print("Original:", message)
    print("Encrypted:", encrypted)
    print("Decrypted:", decrypted)
}

// Call main
