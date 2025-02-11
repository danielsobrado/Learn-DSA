# Remove Duplicates from Sorted Array - Discussion

## Understanding Time and Space Complexity

### Time Complexity: O(n)
- We look at each element exactly once
- Each operation (comparison, assignment) is O(1)
- No nested loops

### Space Complexity: O(1)
- We only use two pointers
- No extra arrays or data structures
- Modifications done in-place

## Why This Problem is Important

### Learning Points
1. In-place array modification
2. Two-pointer technique
3. Taking advantage of sorted arrays
4. Space-efficient algorithms

### Real World Applications
1. Removing duplicate records
2. Cleaning data sets
3. Memory-efficient array operations
4. Database unique constraints

## Interview Tips

### What Interviewers Look For
1. Understanding of in-place operations
2. Efficient use of array properties
3. Clean, readable code
4. Handling edge cases

### Good Follow-up Questions to Ask
1. "What if the array wasn't sorted?"
2. "What if we wanted to keep duplicates but limit them to N occurrences?"
3. "How would we handle this with strings instead of numbers?"

## Edge Cases to Consider

### Important Test Cases
```
1. Empty Array
[]        -> []        return 0

2. Single Element
[1]       -> [1]       return 1

3. No Duplicates
[1,2,3]   -> [1,2,3]   return 3

4. All Same
[2,2,2]   -> [2]       return 1

5. Duplicates at End
[1,2,2]   -> [1,2]     return 2

6. Duplicates at Start
[1,1,2]   -> [1,2]     return 2

7. Negative Numbers
[-1,-1,0] -> [-1,0]    return 2
```

## Alternative Approaches

### Using Extra Space (Not Acceptable but Educational)
```python
def removeDuplicates(nums):
    unique = list(dict.fromkeys(nums))
    nums[:len(unique)] = unique
    return len(unique)
```

Pros:
- Easier to understand
- Less prone to errors
- Simpler code

Cons:
- Uses extra space
- Doesn't meet problem requirements
- Less efficient

### Two Pointers (Correct Solution)
Pros:
- Space efficient
- Meets all requirements
- Fast execution

Cons:
- More complex logic
- Harder to understand at first

## Common Mistakes and Solutions

### Mistake 1: Creating New Array
```python
# Wrong
def removeDuplicates(nums):
    nums = list(set(nums))  # Creates new array!
    return len(nums)

# Right
def removeDuplicates(nums):
    if not nums: return 0
    position = 1
    for i in range(1, len(nums)):
        if nums[i] != nums[i-1]:
            nums[position] = nums[i]
            position += 1
    return position
```

### Mistake 2: Not Using Sorted Property
```python
# Wrong (unnecessary comparisons)
def removeDuplicates(nums):
    position = 0
    for i in range(len(nums)):
        if nums[i] not in nums[:position]:  # Too much work!
            nums[position] = nums[i]
            position += 1
    return position

# Right (uses sorted property)
def removeDuplicates(nums):
    if not nums: return 0
    position = 1
    for i in range(1, len(nums)):
        if nums[i] != nums[i-1]:  # Only compare with previous
            nums[position] = nums[i]
            position += 1
    return position
```

## Performance Optimization

### Speed Improvements
1. Early returns for empty/single element arrays
2. Use fact that array is sorted
3. Minimize array writes

### Memory Usage
1. Use primitive types
2. Avoid temporary variables
3. No extra data structures

## Interview Strategy

### Key Points to Cover
1. Mention that array is sorted
2. Explain two-pointer approach
3. Discuss space efficiency
4. Handle edge cases

### Code Walkthrough Example
```
Input: [1,1,2,2,3]

1. Initialize:
   [1,1,2,2,3]
    p i
   position = 1, i = 1

2. First comparison:
   nums[1] == nums[0], skip

3. Second comparison:
   nums[2] != nums[1]
   Copy 2 to position 1:
   [1,2,2,2,3]
      p

And so on...
```

Remember: The key to this problem is using the sorted property and in-place modification efficiently!