# Remove Duplicates from Sorted Array II - Simple Explanation

## What is the Problem?
You have a sorted list of numbers, and you need to modify it so that each number appears at most twice. You must do this by changing the array directly.

## Simple Example with Cards
Imagine you have a deck of sorted number cards:
```
[1,1,1,2,2,3]
      ↑
  third '1' should be removed
```
You want to:
- Keep up to two of each card
- Remove extras
- Keep cards in order
- Move remaining cards to the front

## Key Points to Understand
1. Array is already sorted (numbers go up from left to right)
2. Can keep up to TWO of each number
3. Must modify array directly (no new arrays!)
4. Need to return how many numbers are left
5. Don't care what's left at the end of array after valid numbers

## Visual Examples

### Example 1:
```
Input:  [1, 1, 1, 2, 2, 3]
Output: [1, 1, 2, 2, 3, _]  (_ means don't care)
Return: 5 (because we kept 5 numbers)

What happened?
- Kept two 1s (removed third 1)
- Kept two 2s
- Kept one 3
```

### Example 2:
```
Input:  [0, 0, 1, 1, 1, 1, 2, 3, 3]
Output: [0, 0, 1, 1, 2, 3, 3, _, _]
Return: 7 (because we kept 7 numbers)

What happened?
- Kept two 0s
- Kept two 1s (removed other two 1s)
- Kept one 2
- Kept two 3s
```

## What Makes This Tricky?
1. You can't use extra arrays
2. Need to count how many numbers to keep
3. Must maintain order
4. Need to handle repeated numbers carefully

## Important Rules
1. Array is always sorted
2. Keep up to two of each number
3. Remove extras
4. Move valid numbers to front
5. Return count of kept numbers

## Think About It Like This
Imagine sorting a deck of cards:
1. You have multiple copies of each card
2. You can keep at most two of each number
3. You put the cards you keep at the front
4. You don't care what's left at the back
5. You need to tell someone how many cards you kept

## Limits to Remember
- Array will have at least 1 number
- Numbers can be negative or positive
- Array is always sorted from small to big
- Array won't be too big (max 30,000 elements)