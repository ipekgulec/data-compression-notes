# Binary Search Project – AP CSP
Mission: Binary Search Protocol
You are a Backend Engineer. You have a sorted database of User IDs. A linear search takes too long, so you must implement a Binary Search algorithm to find a specific ID and report efficiency.
Target ID: 23
Database: [2, 5, 8, 12, 16, 23, 38, 56, 72, 91]
# 1- Pseudocode (AP CSP Style)
Algorithm: BinarySearch
Input: sorted list of user IDs, target ID
Output: index of target ID and number of steps

1. Set low = 0
2. Set high = length of list - 1
3. Set steps = 0
4. Set found = false
5. WHILE low <= high AND found == false
     a. Set middle = (low + high) / 2
     b. Increment steps by 1
     c. Print "Step steps: Checking Index [middle] -> Value: list[middle]"
     d. IF list[middle] == target
           Set found = true
           RETURN middle, steps
     e. ELSE IF list[middle] < target
           Set low = middle + 1
     f. ELSE
           Set high = middle - 1
6. IF found
       Print "SUCCESS: User ID found at Index middle"
       Print "EFFICIENCY: Operation completed in steps steps"
7. ELSE
       Print "FAIL: User ID not found"
       Print "EFFICIENCY: Operation completed in steps steps"
# 2- Swift Implementation
import Foundation

// DATA INPUT
let database = [2, 5, 8, 12, 16, 23, 38, 56, 72, 91]
let targetID = 23

print("SYSTEM: Starting Binary Search Protocol...")
print("Target ID: \(targetID)")
print("---------------------------------------------")

// BINARY SEARCH
var low = 0
var high = database.count - 1
var steps = 0
var found = false
var indexFound = -1

while low <= high && !found {
    let middle = (low + high) / 2
    steps += 1
    print("Step \(steps): Checking Index [\(middle)] -> Value: \(database[middle])")
    
    if database[middle] == targetID {
        found = true
        indexFound = middle
    } else if database[middle] < targetID {
        low = middle + 1
    } else {
        high = middle - 1
    }
}

// OUTPUT
if found {
    print("\nSUCCESS: User ID found at Index \(indexFound)")
    print("EFFICIENCY: Operation completed in \(steps) steps")
} else {
    print("\nFAIL: User ID not found")
    print("EFFICIENCY: Operation completed in \(steps) steps")
}
# 3- Expected Console Output
SYSTEM: Starting Binary Search Protocol...
Target ID: 23
---------------------------------------------
Step 1: Checking Index [4] -> Value: 16
Step 2: Checking Index [7] -> Value: 56
Step 3: Checking Index [5] -> Value: 23

SUCCESS: User ID found at Index 5
EFFICIENCY: Operation completed in 3 steps
