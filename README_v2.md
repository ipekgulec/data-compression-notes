# Binary Counter

A SwiftUI project that shows a counter from 0 to 15 in decimal and 4-bit binary format. The user taps a button to increment the counter, which resets after reaching 15.

***Target Audience:*** Beginner SwiftUI learners and students learning binary numbers  
***Why?:*** To practice state management and conversion between decimal and binary  
***Design Choices:*** Uses a single `@State` variable for the counter; binary conversion is done using Swift’s `String(count, radix: 2)`  
***Hardest Part:*** Formatting binary output to always show 4 digits  
***Counter Logic:*** Increments the counter by 1; resets to 0 after 15  
***Learned:*** Learned decimal-to-binary conversion, string formatting, and state-driven UI updates  
***SwiftUI Features Used:*** @State, VStack, Text, Button  

---

# Person Illustration

A SwiftUI project that draws a person using shapes like Capsule, Rectangle, Circle, and Ellipse. The design includes face, hair, eyes, nose, mouth, arms, and shirt.

***Target Audience:*** Beginner SwiftUI learners and students learning shapes  
***Why?:*** To practice combining shapes to build complex illustrations  
***Design Choices:*** Each body part is a separate shape with position, size, and color; no arrays are used  
***Hardest Part:*** Arranging shapes correctly to resemble a person  
***Illustration Logic:*** Uses ZStack to overlay shapes; offsets and rotations adjust positioning  
***Learned:*** Learned shape composition, layering with ZStack, and color management  
***SwiftUI Features Used:*** ZStack, VStack, Capsule, Rectangle, Circle, Ellipse, Color, offset, rotationEffect  

---

# Index Numbers

A SwiftUI project that displays individual numbers as text without using arrays. Each number is manually defined and shown in a VStack.

***Target Audience:*** Beginner SwiftUI learners  
***Why?:*** Demonstrates how to show multiple items without using arrays  
***Design Choices:*** Each number is a separate `Text` view; indexes are hardcoded  
***Hardest Part:*** Displaying multiple numbers efficiently without arrays  
***Display Logic:*** Each number is placed manually in the VStack  


***Learned:*** Learned manual layout, text formatting, and VStack arrangement  
***SwiftUI Features Used:*** VStack, Text  
