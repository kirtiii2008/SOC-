My code forces handle is https://codeforces.com/profile/kirti2008

# Week 1

Contest Link for Week 1 https://codeforces.com/group/MNl5W7SXII/contest/697929

Week 1 started with basics of cp like time and space analysis, learning how to use vectors, sets, maps, pairs and other built-in functions/libraries in cpp. Then we moved on to the concepts like binary search and sliding windows which are useful in many questions to reduce the time.

## Binary Search

This is an algorithm which is used to find the index of an element in a SORTED array. If the array isn't sorted we have to go through whole array and check each element which takes O(n) time but if the array is sorted we can use binary search to reduced the time complexity to O(log(n)).

### Working of Binary Search

The algorithm maintains two pointers, left and right, representing the current search range. At each step, the middle element is examined (`mid=(left+right)/2`). If the target is smaller than the middle element, the search continues in the left half, otherwise, it continues in the right half. This process repeats until the desired element or boundary is found.

### Finding lower and upper bounds

In the algo we can change the inequalities to find the first or last occurence of an element in a sorted array. For example if we have something like `if(arr[mid] <= target) left=mid;` and then return `left` in the end it will find the LAST occurence provided that target exists. Similarly we can flip the logic and say that if `arr[mid]>=target` `right=mid;` and then return `right` at the end will be the first occurence of the target element because whenever we find the target element we made that the right boundary resulting in squeezing the search space towards left.

### Binary Search on Answer

It can also be applied to the answer range of a problem. If a value `x` works, then all values greater than `x` also work, Binary Search can efficiently determine the minimum or maximum valid answer. This technique is commonly known as "Binary Search on Answer."

The problem in which we have to find the minimum length of the subarray for which the sum is atleast `S` (in `O(nlogn)`). We do binary search on the answer length `l`; for each `l` we can find the sums of subarrays of length `l` in `O(n)` time by two-pointers/sliding window.

## Sliding Windows

In this algo we maintain two pointers left and right which keeps on increasing and therefore reducing the time complexity to `O(n)`. This avoids going through the previous data which irrevalent for our answer.

One example of this is max length of subarray with `sum <= K` so we keep two pointers `left,right` and then keep adding elements of the array until the `sum > K` and when this happens we slide the left pointer till the `sum <= K` because the current window is invalid and continue the process.

The main idea is to avoid repeatedly processing elements that are not relevant to the current answer. As the right pointer expands the window, information about the current subarray is updated incrementally. If the window violates a required condition, the left pointer is moved forward until the condition is restored.

# Week 2

Contest Link for Week 2 is https://codeforces.com/group/MNl5W7SXII/contest/695081

## Divide And Conquer

In this we break the problem into smaller subproblems. The key is forget about solving the smaller subproblem and just focus on combining the solutions to solve the bigger one. Using this algo we saw some problems like counting inversions, area counting etc.

## Greedy

This algo makes sure to solve the problem locally by finding the locally best solution and then proving that any other choice is not better.

Some problems based on this were Scheduling where we have to maximise the number of events and we take the event whose ending is earliest and keep doing this until we run out of events. We can say that if we choose an event B which ends after event A, we can use event A instead of B because it will leave us with atleast as many choices as choosing B.

Tasks and deadlines, minimising sums and coin problems (when there are euro coins) were also covered.

## Sieve of Eratosthenes

This helps us count the number of primes till a number `n` by removing all the multiples of prime numbers till `sqrt(n)`.

# Week 3 and 4

Contest Link for Week 3 https://codeforces.com/group/MNl5W7SXII/contest/696451

Contest Link for Week 4 https://codeforces.com/group/MNl5W7SXII/contest/697929

These weeks were focused on DP which is recursion with memory management. We store previously computed values and reuse them to calculate future values which saves both time and memory significantly.

Problems were provided in the resources involving greedy and DP like Subset Sum Problem, Optimal Binary Search Tree, Knapsack Problem, etc.
Greedy and Advanced DP problems aren't disscussed in the report.
