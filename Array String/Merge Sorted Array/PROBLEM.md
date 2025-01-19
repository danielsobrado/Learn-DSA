# Merge Sorted Array - Simple Guide

## What is the problem asking?
You have two arrays of numbers:
- First array (nums1): has extra space at the end (filled with zeros)
- Second array (nums2): needs to be merged into the first array
- Both arrays are already sorted from smallest to largest

For example:
- nums1 = [1,2,3,0,0,0] (only 1,2,3 are real numbers, zeros are empty spaces)
- nums2 = [2,5,6]
- After merging: nums1 should become [1,2,2,3,5,6]

## Key Points to Understand
1. The arrays are already sorted
2. You must put the result in the first array (nums1)
3. The zeros at the end of nums1 are just empty spaces

## Simple Way to Think About It
Imagine you have two piles of cards, both sorted from smallest to largest:
- Pile 1: [1,2,3]
- Pile 2: [2,5,6]
- Empty spaces: [_,_,_] (in Pile 1)

You need to merge them into Pile 1, keeping them sorted.

## Why Start From the End?
The smart way to solve this is to start placing numbers from the end:
1. It's like having extra spaces at the end of Pile 1
2. You won't overwrite any numbers you still need
3. You can fill the biggest numbers first

## Step by Step Example
Using nums1 = [1,2,3,0,0,0] and nums2 = [2,5,6]

1. Compare last real numbers from each array:
   - nums1: 3
   - nums2: 6
   - 6 is bigger → put 6 at the end
   [1,2,3,0,0,6]

2. Next comparison:
   - nums1: 3
   - nums2: 5
   - 5 is bigger → put 5
   [1,2,3,0,5,6]

3. Next:
   - nums1: 3
   - nums2: 2
   - 3 is bigger → put 3
   [1,2,3,3,5,6]

And so on...

## Common Mistakes to Avoid
1. Don't try to start from the beginning - you'll lose numbers
2. Don't forget that nums1 has empty spaces at the end
3. Remember that both arrays are already sorted

## Visual Guide
```
Initial state:
nums1 = [1, 2, 3, _, _, _]  (where _ means empty space)
nums2 = [2, 5, 6]

We start filling from the end:
Step 1: [1, 2, 3, 0, 0, 6]  ← Added biggest number (6)
Step 2: [1, 2, 3, 0, 5, 6]  ← Added next biggest (5)
Step 3: [1, 2, 3, 3, 5, 6]  ← Added 3
Step 4: [1, 2, 2, 3, 5, 6]  ← Added 2
And so on...
```

Remember: This is like merging two sorted piles of cards into one pile, always picking the bigger card to place from the end.