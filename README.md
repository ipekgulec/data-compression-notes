# Frog Escape

A clock-based game where a character (😺) moves around a 12-hour clock face. The player taps a button to move the character to a random position. The game has levels, a countdown timer, and increasingly shorter time per level.

**Target Audience:** Kids and casual players  
**Why?:** It’s a fun way to practice timing and reaction skills, with a simple visual design.  
**Design Choices:** The clock face shows character movement without using arrays, and animation makes the movement smooth. Each level increases difficulty by reducing the timer.  
**Hardest Part:** Moving the character randomly without repeating the same position.  
**Timer/Level Logic:** Timer counts down, and when it reaches 0, the level increases and the timer resets to a slightly shorter duration.  
**Learned:** Learned how to map positions to X/Y offsets manually without arrays, and how to use SwiftUI animation with state changes.  
**SwiftUI Features Used:** @State, Timer.publish, onReceive, Button, VStack, ZStack, animation.
