# Initials Pixel Art V2

This SwiftUI project allows users to create colorful pixel art initials using emojis. The user types their first and last name into text fields, then selects one of ten available emojis to use as the “pixels” for their initials. Each initial is displayed as a 10×10 grid, where each cell is either the chosen emoji or a background square, creating a recognizable letter pattern. The project is designed without using arrays; instead, it relies entirely on conditional statements (`if`) and logical checks to determine which grid cells are “on” and should display the emoji.  

**Target Audience:** Beginner SwiftUI learners and anyone interested in experimenting with simple pixel art.  

**Why?:** The goal of this project is to practice grid layouts, user input handling, conditional logic, and combining dynamic content with SwiftUI views, all without relying on arrays. It provides an interactive and visually engaging way for learners to understand how loops, conditionals, and state variables work together to build a functional app.  

**Design Choices:** Each letter is constructed using a “mask” function that decides which cells are filled, while another function determines which emoji to display for each active cell. The project also allows users to pick from multiple emoji options, making the output customizable and playful. `ForEach` loops are used to generate the grid efficiently, and each grid is wrapped in a `VStack` and `HStack` structure to form the pixel art layout.  

**Hardest Part:** The most challenging aspect was designing the masks for letters, particularly the letter “G,” entirely without arrays. It required careful mapping of rows and columns to visualize the letter accurately using only conditional statements.  

**Learned:** Through this project, I learned how to map grid coordinates to visual output, create interactive SwiftUI components, use state variables to handle user input and emoji selection, and apply logic to dynamically generate custom visuals. It also helped me understand how to build complex layouts using basic SwiftUI primitives, providing a foundation for more advanced interactive apps.


  # Candy Shop Simulation

A SwiftUI project that simulates a candy shop, tracking chocolate, gummies, and lollipops. The app simulates 60 minutes of sales, applies discounts every 15 minutes, restocks every 20 minutes, and shows low-stock warnings. All logic is handled with `if` statements and loops without arrays.  

**Target Audience:** Beginner SwiftUI learners  
**Why?:** To practice state management, loops, and conditional logic  
**Design Choices:** Separate counters for each candy, dynamic cash updates, and real-time report display  
**Hardest Part:** Managing multiple states and ensuring correct discount/restock logic  
**Learned:** Combining SwiftUI state, loops, randomization, and conditional logic to create a functional simulation

# Build-A-Sundae Dashboard

A SwiftUI project that visualizes ice cream flavors using a simple dashboard. Each flavor has a “meter” represented by a horizontal bar whose length corresponds to its value, allowing users to quickly see the popularity or availability of each flavor. The project demonstrates the use of `ForEach` loops, `GeometryReader`, and dynamic layouts in SwiftUI.  

**Target Audience:** Beginner SwiftUI learners and those interested in interactive dashboards  
**Why?:** To practice dynamic layouts, bar chart visualization, and using SwiftUI views together  
**Design Choices:** Horizontal bars with color coding for flavors, bold labels, and numeric values for clarity  
**Hardest Part:** Learning to combine `GeometryReader` with dynamic bar lengths while keeping the layout neat  
**Learned:** How to create simple dashboards, use `ForEach` for dynamic content, and map data values to visual representations in SwiftUI
