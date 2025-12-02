# Initials I & g

A SwiftUI project that draws my initials (I and g) in a 10×10 grid. Each circle is colored based on its position to form the letters. No arrays are used; only conditionals and simple logic.

**Target Audience:** People learning SwiftUI and beginner coders  
**Why?:** To practice grid layout, conditional coloring, and logic without arrays.  
**Design Choices:** Letters are formed using `if` statements; circles are dynamically colored to make the initials recognizable.  
**Hardest Part:** Figuring out the logic to draw the letter “g” properly using only `if` and `let`.  
**Learned:** Mapping rows and columns to shapes, using `ForEach` loops for grids, and SwiftUI circle coloring.

![Initials I & g Screenshot](initials_ig.png)

# Hot Chocolate Machine
A simulation where a hot chocolate heats over time and the player serves it safely. The machine auto-stops if it gets too hot.
Target Audience: Kids and casual players
Why?: Fun way to learn timing and temperature monitoring.
Design Choices: Fixed temperature steps, messages change by heat level, auto-stop prevents overheating.
Hardest Part: Stopping the machine correctly while updating temperature.
Timer/Level Logic: 20 “minutes,” temperature increases each minute, messages depend on thresholds.
Learned: Managing state, conditional logic, and dynamic feedback in Swift.
Swift Features Used: @State, Timer, print, loops, if/else, break, functions.

PROCEDURE HotChocolateMachine
    SET temperature TO 20
    SET totalChange TO 0

    FOR minute FROM 1 TO 20
        SET temperature TO temperature + 5
        SET totalChange TO totalChange + 5

        IF temperature > 80 THEN
            DISPLAY "Minute " + minute + ": " + temperature + "°C → ⚠ Machine auto-stop activated!"
            BREAK
        ELSE IF temperature > 70 THEN
            DISPLAY "Minute " + minute + ": " + temperature + "°C → Too hot! Wait before drinking."
        ELSE IF temperature >= 50 THEN
            DISPLAY "Minute " + minute + ": " + temperature + "°C → The drink is ready to serve!"
        ELSE
            DISPLAY "Minute " + minute + ": " + temperature + "°C → The drink is still cold."
        END IF
    END FOR

    DISPLAY "Total temperature change: " + totalChange + "°C"
END PROCEDURE

CALL HotChocolateMachine

import Foundation

func hotChocolateMachine() {
    var temperature = 20
    var totalChange = 0

    for minute in 1...20 {
        temperature += 5
        totalChange += 5

        if temperature > 80 {
            print("Minute \(minute): \(temperature)°C → ⚠ Machine auto-stop activated!")
            break
        } else if temperature > 70 {
            print("Minute \(minute): \(temperature)°C → Too hot! Wait before drinking.")
        } else if temperature >= 50 {
            print("Minute \(minute): \(temperature)°C → The drink is ready to serve!")
        } else {
            print("Minute \(minute): \(temperature)°C → The drink is still cold.")
        }
    }

    print("\nTotal temperature change: \(totalChange)°C")
}

hotChocolateMachine()



