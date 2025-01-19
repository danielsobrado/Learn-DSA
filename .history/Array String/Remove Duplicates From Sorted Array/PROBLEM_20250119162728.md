# Remove Element - Simple Explanation

## What is the Problem?
You need to remove all instances of a specific number from an array. But there's a catch - you need to do it without creating a new array!

## Simple Example
```
Array: [3, 2, 2, 3]
Number to remove: 3
Result should be: [2, 2, ?, ?]  (? means we don't care what's here)
Return value: 2 (because we have two numbers left)
```

## What Makes This Problem Special?
1. You must modify the array directly (no creating new arrays)
2. You only need to worry about the remaining numbers
3. The order of numbers doesn't matter
4. You need to return how many numbers are left

## Real World Example
Think of it like cleaning a shelf:
- You have a shelf with items (the array)
- You want to remove all items of a certain color (the value)
- You move the items you want to keep to the front
- You don't care what's left at the back of the shelf
- You need to tell someone how many items you kept

## What the Problem Wants
1. Remove a specific number from the array
2. Move all other numbers to the front
3. Count how many numbers are left
4. Return that count

## Important Points to Remember
1. You can't use a new array
2. Order doesn't matter
3. You don't care about what's after your valid numbers
4. Return the count of remaining numbers

## Visual Example
Starting array: [0,1,2,2,3,0,4,2]
Remove all 2s:
```
Before: [0,1,2,2,3,0,4,2]
After:  [0,1,4,0,3,?,?,?]  (? means we don't care)
Return: 5 (because we have 5 numbers left)
```

## Constraints (Simple Terms)
- Array can be empty or have up to 100 numbers
- Numbers in array are between 0 and 50
- Number to remove is between 0 and 100

## Testing Understanding
The judge will:
1. Check if your count is correct
2. Check if all remaining numbers are not the removed value
3. Not care about the order of remaining numbers
4. Not care what's beyond your count