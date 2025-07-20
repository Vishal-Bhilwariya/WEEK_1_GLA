Problem: Find Minimum in Rotated Sorted Array (Optimal)

Overview:
This project solves the problem of finding the minimum element in a sorted array that's been rotated. A rotated sorted array still consists of two sorted parts, and our goal is to find the smallest element efficiently.

Example:
Original array: [0, 1, 2, 4, 5, 6, 7]
After rotation: [4, 5, 6, 7, 0, 1, 2]
Minimum = 0

Approach: Binary Search

We use a modified binary search to achieve O(log n) time complexity.

How it works:

Start with two pointers: left at the beginning, right at the end.

While left <= right, compute the mid.

Compare arr[mid] with arr[right]:

If arr[mid] > arr[right], the minimum lies in the right half → left = mid + 1

Else, the minimum is in the left half (possibly at mid) → record arr[mid], then right = mid - 1

Repeat until the smallest element is found.

Complexity

Time: O(log n) — thanks to binary search.
Space: O(1) — uses only a few variables.