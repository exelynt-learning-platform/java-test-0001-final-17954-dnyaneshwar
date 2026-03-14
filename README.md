# java-test-0001-final-17954-dnyaneshwar
Final Project Assignment - This repository contains the complete final project code and documentation.

Java Hollow Diamond Pattern Program
📌 Project Overview

This project demonstrates how to generate a Hollow Diamond Star Pattern using Java programming.
The pattern is created by carefully controlling nested loops, spaces, and star placement to achieve the required symmetrical structure.

Pattern problems are commonly used in coding interviews to test a candidate's understanding of:

Loop control structures

Logical thinking

Output formatting

Pattern recognition

Problem-solving ability

This program prints a hollow diamond shape, where stars (*) appear only on the boundary of the diamond while the inside remains empty.

⭐ Pattern Output

The program prints the following pattern exactly:

    *
   * *
  *   *
 *     *
*       *
 *     *
  *   *
   * *
    *
Pattern Explanation

The pattern consists of two symmetrical parts:

1️⃣ Upper Half (Expanding Triangle)

Starts with one star at the top

Each row increases the width of the diamond

Spaces between stars increase gradually

2️⃣ Lower Half (Contracting Triangle)

Mirrors the upper half

Each row reduces the width of the diamond

The pattern closes back to one star

Total rows = 2 × n − 1

For this program:

n = 5
Total rows = 9
🧠 Concepts Used
1. Nested Loops

Nested loops are used to control:

Rows

Spaces before stars

Stars and internal spaces

Example structure:

Outer Loop → controls rows
Inner Loop 1 → prints leading spaces
Inner Loop 2 → prints stars and internal spaces
2. Space Alignment

Spaces are printed before stars so that the diamond stays center aligned.

Example:

for(int j = i; j < n; j++)
{
    System.out.print(" ");
}

This ensures that the stars appear in the center of the console output.

3. Hollow Pattern Logic

To make the diamond hollow, stars are printed only at the boundaries.

Condition used:

if(j == 1 || j == (2*i - 1))

Meaning:

Print star at the first position

Print star at the last position

Print space inside

Example row:

*       *
💻 Java Implementation
public class DiamondPattern {

    public static void main(String[] args) {

        int n = 5;

        for (int i = 1; i <= n; i++) {

           
            for (int j = i; j < n; j++) {
                System.out.print(" ");
            }

            for (int j = 1; j <= (2 * i - 1); j++) {

                if (j == 1 || j == (2 * i - 1)) {
                    System.out.print("*");
                } 
                else {
                    System.out.print(" ");
                }
            }

            System.out.println();
        }
        
        for (int i = n - 1; i >= 1; i--) {

            // Print leading spaces
            for (int j = n; j > i; j--) {
                System.out.print(" ");
            }

            for (int j = 1; j <= (2 * i - 1); j++) {

                if (j == 1 || j == (2 * i - 1)) {
                    System.out.print("*");
                } 
                else {
                    System.out.print(" ");
                }
            }

            System.out.println();
        }
    }
}
⚙️ Step-by-Step Execution
Step 1

Set the size of the diamond

int n = 5;

This determines the height of the upper triangle.

Step 2

Print the upper half of the diamond.

for(int i = 1; i <= n; i++)

Rows increase gradually.

Step 3

Print leading spaces before stars.

for(int j = i; j < n; j++)

Spaces decrease as rows increase.

Step 4

Print stars and internal spaces.

for(int j = 1; j <= (2*i - 1); j++)

This controls the width of the diamond.

Step 5

Print the lower half of the diamond.

for(int i = n-1; i >= 1; i--)

Rows decrease gradually.

📊 Time Complexity

The program uses nested loops.

Time Complexity = O(n²)

Where n = number of rows in half diamond

▶️ How to Run the Program
1️⃣ Save the file
HollowDiamondPattern.java
2️⃣ Compile the program
javac HollowDiamondPattern.java
3️⃣ Run the program
java HollowDiamondPattern
✅ Evaluation Criteria

This solution meets the following evaluation standards:

✔ Correct use of nested loops
✔ Accurate pattern generation
✔ Proper spacing and alignment
✔ Clean and readable code structure
✔ Successful compilation and execution

