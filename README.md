[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-24ddc0f5d75046c5622901739e7c5dd533143b0c8e959d652212380cedb1ea36.svg)](https://classroom.github.com/a/9YUeXH71)
# Theoretical Sorting

A Computer Science researcher claims to have come up with a sorting algorithm
that can sort arbitrary elements in $O(n)$ time based on comparisons of two
elements at a time. This would be asymptotically faster than any known general
sorting algorithm. The algorithm itself is proprietary and will be sold by a
company.

How would you verify this claim? You may assume that you have access to a
black-box implementation of the sorting algorithm, i.e. you cannot examine the
source code, but you can use it to sort any list you like. Explain in detail
your method for investigating whether X is correct, including any expected
results you would get.

Also give a theoretical argument for why X could or could not be correct, based
on the complexity of the general sorting problem we covered in class.

Add your answers to this markdown file.

Answer: 
To verify this claim, I would take a list of n size and create every possible permutation of this list. Then, I would use this sorting algorithm to solve every permutation of the list and see which one had the worst case runtime. Now, I would repeat this strategy for multiple different sizes of lists with different elements. If all of these were solved in worst case time, and the time would grow linearly, then X's claim would be verified.  

X's claim could not be correct because we know that theoretically, comparison-based sorting algorithms are restricted to at least $O(nlog n)$ time complexity because the function has to compare every element in the array at least once. The amount of comparisons after can be reduced to grow by log n, but it is theoretically impossible for a comparison-based sorting algorithm to get any more efficient than that. Therefore, X's sorting algorithm could not be correct. Additionally, this claim would also have to take into account multiple different data types and test if all of them also grow linearly. We would have to test the space complexity of the alogirthm. If the algorithm was extremely memory intensive, the algorithm could be completely impractical where we cannot possibly store the amount of data that the alogorithm requires or it causes significant slow down times to the point where the runtime does not grow linearly anymore. 
