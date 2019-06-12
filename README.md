# State-Color-Mapping-Puzzle
Solves a puzzle in which one of four colors is assigned to each US State to maximize the total score, where adjacent states cannot have the same color

My son's 5th grade class was given this assignment to complete using only their brains. I immediately recognized that actually solving this puzzle to find the optimal score is incredibly difficult - equivalent to work I did in my 4th year of Systems Engineering in college. So I decided to write code to find the optimal solution for comparison against what my son (and his classmates came up with).

It turns out my son found the optimal solution all on his own! As did 3 other students. But none fully appreciated the complexity until I volunteered in class one day to show them how there were actually 4^22 ways to color the states and only 340,416 valid ways to color them, with just 2 optimal solutions!

Once I coded the optimal solution, I wanted to see if I could scale it to 50 states, and quickly ran into memory problems, with 4^50 possible combinations, and the code would not run to completion. So I had to find a more clever way to solve the puzzle that would eliminate 'expensive' combinations quickly.

Here's the problem statement
