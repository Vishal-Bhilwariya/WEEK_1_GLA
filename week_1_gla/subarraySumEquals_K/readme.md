My first try was a brute-force approach. It worked, but was too slow for larger inputs. So I looked for a better way and came up with this faster, smarter solution.

The Optimized Approach: Using HashMap and Prefix Sum

Instead of checking every possible combination, this method solves the problem in a single pass using a prefix sum and a HashMap.

Here’s the idea:

As we go through the calorie data, we maintain a running total called currentSum.

The HashMap keeps track of how many times each prefix sum has occurred so far.

At each step, we check if currentSum - k has been seen before.

If yes, it means the days between that previous sum and the current day add up to k. We add the count of that sum to our result.

Then we update the map to include the new currentSum.

There’s one important detail: we start by initializing the map with 0 occurring once. This handles the case where a valid streak starts right from the beginning.

Performance

Time Complexity: O(n) — We process the list only once, so the solution is very fast.
Space Complexity: O(n) — The HashMap might store a unique sum for each day, but it’s worth the trade-off for the speed.