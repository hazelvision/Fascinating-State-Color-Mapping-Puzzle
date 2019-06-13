# State-Color-Mapping-Puzzle
Solves a puzzle in which one of four colors is assigned to each of 22 contiguous US States to maximize the total score, where adjacent states cannot have the same color.

My son's 5th grade class was given this assignment to complete using only their brains, and I immediately recognized this problem was far more complex than the teacher understood. 

-------------------------------------------------------------------------------------------------------------------
Here's the problem statement from the actual assignment:
Using these four colors (red, purple, blue and green), color every state with a number on it. No state may touch another state of the same color. 

STATE VALUES (Before color multiplier):
Washington - 71
Oregon - 98
California - 163
Idaho - 83
Nevada - 110
Montana - 147
Wyoming - 97
Utah - 84
Arizona - 113
Colorado - 104
New Mexico - 121
North Dakota - 70
South Dakota - 77
Nebraska - 77
Kansas - 82
Oklahoma - 69
Texas - 268
Minnesota - 86
Iowa - 56
Missouri - 69
Arkansas - 53
Louisiana - 51

Each color is a multiplier. If you color a state green, you will take the number value in that state and multiply it by 4. This will be the score for that state. All states you color purple will be multiplied by 2.

SCORING:
Red states x1
Purple states x2
Blue states x3
Green states x4

Add up all your state scores for your total number of points. Your goal is to get the lowest score possible (golf score). For a different challenge, color the states to get the maximum score possible.

-------------------------------------------------------------------------------------------------------------------

I realized actually solving this puzzle to find the optimal score is equivalent to work I did in my 4th year of Systems Engineering in college. So I decided to write code to find the optimal solution for comparison against what my son (and his classmates came up with). I wrote it in Pascal simply because it was easier for me to recall than C++ or any other language I learned in college 20 years ago.

It turns out my son found the optimal solution all on his own with the aid of a computer/algorithm! As did 3 other students. But none fully appreciated the complexity until I volunteered in class one day to show them how there were actually 4^22 ways to color the states and only 340,416 valid ways to color them, with just 2 optimal solutions!

Once I coded the optimal solution, I wanted to see if I could scale it to 50 states, but quickly ran into memory problems - with 4^50 possible combinations, the code would not run to completion. So I had to find a more clever way to solve the puzzle that would eliminate 'expensive' combinations quickly.

I've posted here the final code that solves the problem for 50 states, either for the min or max score, and in, I believe, the most efficient manner possible. 

I tried writing code to free up memory for objects that were no longer needed, but it would not compile in the compiler I used.
I also treid to write this using recursion (like you might for solving a maze), but couldn't figure out the logic.

I am curious whether anyone has any other ideas on how this could be solved.

I will include a description of how my algorithm works in a separate file.
