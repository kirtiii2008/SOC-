My codeforces handle https://codeforces.com/profile/kirti2008
The topics written in the respective weeks may not be covered in that week but its an overview.
#Week 1

Week 1 started with basics of cp like time and space analysis, learning how to use vectors,sets,maps,pairs and other built-in fucntions/libraries in cpp.
Then we moved on to the concepts like binary search and sliding windows which are useful in many question to reduce the time.

##Binary Search
This is an algorithm which is used to find the index of an element in a SORTED array. 
If the array isn't sorted we have to go through whole array and check each element which takes O(n) time but if the array is sorted we can use binary search to reduced the time complexity to *O(log(n))*.

###Working of Binary Search
The algorithm maintains two pointers, left and right, representing the current search range. At each step, the middle element is examined ( mid=(left+right)/2). If the target is smaller than the middle element, the search continues in the left half, otherwise, it continues in the right half. This process repeats until the desired element or boundary is found.

###Finding lower and upper bounds
In the algo we can change the inequalities to find the first or last occurence of an element in a sorted array.
for example if we have something like if(arr[mid] <= target) left=mid; and then return left in the end it will find the **LAST** occurence provided that target exists.
Similarly we can flip the logic and say that if(arr[mid]>=target) right=mid; and then return right at the end will be the last occurence of the target element because whenever we find the target element we made that the right boundary resulting in squeezing the search space towards left ie towards the first occurence.

###Binary Search on Answer
It can also be applied to the answer range of a problem. If a value x works, then all values greater than x also work, Binary Search can efficiently determine the minimum or maximum valid answer. This technique is commonly known as "Binary Search on Answer."
The problem in which we have to find the minimum length of the subarray for which the sum is atleast S.(in O(nlogn))
We do binary search on the answer length l for each l we can find the sums of subarrays of length l in O(n) time by two-pointers/sliding window.

##Sliding Windows
In this algo we maintain two pointers left and right which keeps on increasing and therefore reducing the time complexity to O(n). This avoids going through the previous data which irrevalent for our answer.
One example of this is max length of subarray with sum<=K so we keep two pointers left,right and then keep adding elements of the array unitll the sum>K and when this happens we slide the left pointer till the sum<=K beacuse the curr window is invalid and continue the process.
The main idea is to avoid repeatedly processing elements that are not relevant to the current answer. As the right pointer expands the window, information about the curr subarray is updated incrementally. If the window violates a required condition, the left pointer is moved forward until the condition is restored.

#Week 2

##Divide And Conquer
In this we break the problem into smaller subproblems. The key is forget about solving the smaller subproblem and just focus on combining the solutions to solve the bigger one .
Using this algo we saw some problems like counting inversions,area counting etc.

##Greedy
This algo makes sure to solve the problem on locally like finding the locally best solution and then proving that any other thing you do this local optimising is atleast as good as the other.
Some problems based on this was
**Scheduling** where we have to maximise the no. of events and we take event whose ending is earliest and keep doing this until we run out of events. We can say that if u choose an event B who ends AFTER event A we can use event A instead of B beacuse it will left us with ATLEAST as many choices in case we schedule event B beacuse it ends after it so may loose an event whose starting is between ending of A and ending of B in case we choose B.
Tasks and dealines
Minimising sums and coin problems(when there are euro coins)

##Sieve of Eratosthenes
This helps us counting the number of primes till a number n by removing all the multiples of primes numbers till square root(n).

#Week 3 and 4

These weeks was focused on DP which is recursion with memory management like we store the previous values which we can use to calulate the next one which saves the memmory and time by a significant amount.

Many problems were provided in the resoures involving greedy,dp 
Subset Sum problem
Optimal Binary Tree Search
Knapsack Problem.. etc.





