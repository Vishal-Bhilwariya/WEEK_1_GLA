This was my first try at solving the Paint House problem. The goal is to paint a row of houses at the lowest cost, with the rule that no two adjacent houses can have the same color.

My Initial Idea (Brute-Force Recursion)

My first approach was to try every valid color combination. It’s the most straightforward way to think about the problem.

Here’s how the logic works:

For the first house, I try painting it with each available color.

For the second house, I try every color except the one used for the first.

I repeat this process for all houses down the line.

I wrote a recursive function that does exactly this. It goes house by house, tries all valid color choices, and adds up the total cost for each complete path. It keeps track of the lowest-cost path it finds.

The Reality Check (Performance)

Speed (Time Complexity): This approach is easy to understand but very slow. It has exponential time complexity, roughly O(k^n), where k is the number of colors and n is the number of houses. It’s fine for small inputs, but with something like 100 houses, it becomes unusable.

Memory (Space Complexity): It uses memory for the recursive call stack, which depends on the number of houses, so the space complexity is O(n).