# Ice Cream Cone Builder

A SwiftUI project where users build a colorful ice cream cone by adding scoops one by one. Each scoop has a unique color and number, and the cone updates dynamically from bottom to top. Users can reset the cone at any time, and adding more than 5 scoops triggers an automatic reset (overflow handling).

**Target Audience:** Beginner SwiftUI learners and casual users  
**Why?:** It’s a fun way to learn stacking views, state management, and conditional rendering in SwiftUI  
**Design Choices:** Scoops are added sequentially using optional `@State` variables; the cone is a custom `Triangle` shape; overflow is handled gracefully by resetting the cone automatically  
**Hardest Part:** Displaying multiple optional scoops in the correct stacked order while keeping the layout clean  
**Scoop/Reset Logic:** Scoops are added bottom to top; once 5 scoops are present, adding another resets all scoops; users can also reset manually  
**Learned:** Learned to use ZStack and VStack for layered layouts, optional state variables for conditional display, and dynamically updating UI elements  
**SwiftUI Features Used:** @State, if let, ZStack, VStack, Button, custom Shape, conditional rendering  

---

# Food List

A simple SwiftUI project that displays a list of food emojis in a vertical stack. Each item is numbered and shown clearly, demonstrating basic use of `ForEach` and `VStack`.

**Target Audience:** Beginner SwiftUI learners and anyone learning to display lists  
**Why?:** It’s a fun and visual way to practice loops and layout in SwiftUI  
**Design Choices:** The list uses a `VStack` and `ForEach` over indices instead of the array directly, so each item can display its index  
**Hardest Part:** Ensuring the indices match the correct items while keeping the code clean  
**Learned:** Learned how to loop through arrays with indices, use `ForEach` properly, and format text dynamically in SwiftUI  
**SwiftUI Features Used:** VStack, ForEach, Text, Array indices, basic layout  
