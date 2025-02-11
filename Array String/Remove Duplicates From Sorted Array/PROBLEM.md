# Remove Duplicates from Sorted Array - Simple Explanation

## What is the Problem?
You have a list of sorted numbers that might have repeated numbers. You need to remove all duplicates so each number appears only once.

## Real World Example
Think of organizing a deck of numbered cards:
- Original deck: [1,1,1,2,2,3]
- After organizing: [1,2,3]
- We keep only one copy of each number

## Important Rules
1. Array is already sorted (numbers go up from left to right)
2. Keep only ONE copy of each number
3. Must change array directly (can't create new array)
4. Keep numbers in the same order
5. Return how many unique numbers you kept

## Visual Examples

### Example 1:
```
Input:  [1, 1, 2]
Output: [1, 2, _]  (_ means we don't care what's here)
Return: 2 (because we kept 2 unique numbers)

What happened?
- Kept first 1 (removed second 1)
- Kept 2
```

### Example 2:
```
Input:  [0, 0, 1, 1, 1, 2, 2, 3, 3, 4]
Output: [0, 1, 2, 3, 4, _, _, _, _, _]
Return: 5 (because we kept 5 unique numbers)

What happened?
- Kept one 0 (removed duplicate)
- Kept one 1 (removed duplicates)
- Kept one 2 (removed duplicate)
- Kept one 3 (removed duplicate)
- Kept 4
```

## What Makes This Special?
1. You must modify the array directly
2. You can't use extra arrays
3. Array is already sorted (this helps!)
4. Original order must be kept

## Think About It Like This
Imagine sorting a stack of cards:
1. Look at each card
2. If it's different from the last card you kept, keep it
3. If it's the same as the last card you kept, skip it
4. Count how many cards you kept

## Limits to Remember
- Array will have at least 1 number
- Numbers can be negative or positive (-100 to 100)
- Array is always sorted from small to big
- Array won't be too big (max 30,000 numbers)

## What the Judge Will Check
1. Did you return the correct count of unique numbers?
2. Are the first k numbers in the array correct?
3. Are the numbers in the right order?

Remember: You only need to care about the first k positions in the array, where k is the number of unique elements!