# Remove Duplicates from Sorted Array II - Solutions

## Approach 1: Two Pointers (Simple Count)

### Python Solution
```python
def removeDuplicates(nums):
    # Handle arrays of length 0 or 1
    if len(nums) <= 2:
        return len(nums)
    
    # Position to place next number
    position = 2
    
    # Start from third element
    for i in range(2, len(nums)):
        # If current number is different from two positions back
        # we can keep it
        if nums[i] != nums[position - 2]:
            nums[position] = nums[i]
            position += 1
    
    return position
```

### Step by Step Explanation
```
Example: [1,1,1,2,2,3]

Initial state:
[1,1,1,2,2,3]
  p i
p = 2 (position), i = 2

Step 1:
i = 2: Looking at second 1
nums[i] = 1, nums[p-2] = 1
Skip because same as two back

Step 2:
i = 3: Looking at 2
nums[i] = 2, nums[p-2] = 1
Different! Place it:
[1,1,2,2,2,3]
    p

Step 3:
i = 4: Looking at second 2
nums[i] = 2, nums[p-2] = 1
Different! Place it:
[1,1,2,2,2,3]
      p

And so on...
```

### Go Solution
```go
func removeDuplicates(nums []int) int {
    // Handle small arrays
    if len(nums) <= 2 {
        return len(nums)
    }
    
    // Position to place next number
    position := 2
    
    // Check each number starting from third
    for i := 2; i < len(nums); i++ {
        // If different from two positions back
        if nums[i] != nums[position-2] {
            nums[position] = nums[i]
            position++
        }
    }
    
    return position
}
```

### Java Solution
```java
class Solution {
    public int removeDuplicates(int[] nums) {
        // Handle small arrays
        if (nums.length <= 2) {
            return nums.length;
        }
        
        // Position to place next number
        int position = 2;
        
        // Check each number starting from third
        for (int i = 2; i < nums.length; i++) {
            // If different from two positions back
            if (nums[i] != nums[position - 2]) {
                nums[position] = nums[i];
                position++;
            }
        }
        
        return position;
    }
}
```

## Approach 2: Count While Moving (More Intuitive)

### Python Solution
```python
def removeDuplicates(nums):
    # Count of current number
    count = 1
    # Position to place next number
    position = 1
    
    # Start from second number
    for i in range(1, len(nums)):
        # If same as previous number
        if nums[i] == nums[i-1]:
            count += 1
        else:
            # Different number, reset count
            count = 1
            
        # If count is 1 or 2, keep the number
        if count <= 2:
            nums[position] = nums[i]
            position += 1
            
    return position
```

## Which Solution to Use?

### Approach 1 (Two Pointers):
- Pros:
  - Faster (fewer comparisons)
  - Cleaner code
- Cons:
  - Harder to understand at first
  - Less intuitive

### Approach 2 (Count While Moving):
- Pros:
  - More intuitive
  - Easier to modify for different counts
- Cons:
  - More operations
  - Slightly more complex logic

## Common Mistakes to Avoid

1. Starting from Wrong Position
```python
# Wrong: Starting from beginning
position = 0  # Wrong!
# Right: We keep first two elements always
position = 2  # Right!
```

2. Wrong Comparison
```python
# Wrong: Comparing with previous
if nums[i] != nums[i-1]  # Wrong!
# Right: Compare with two positions back
if nums[i] != nums[position-2]  # Right!
```

3. Forgetting Small Arrays
```python
# Wrong: No check for small arrays
# Right: Handle small arrays first
if len(nums) <= 2:
    return len(nums)
```

## Tips for Solving
1. Start by keeping first two elements
2. Use position pointer for where to place next number
3. Compare with element two positions back
4. Only move position when keeping a number
5. Return position as final count