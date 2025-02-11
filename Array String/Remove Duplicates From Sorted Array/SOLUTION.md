# Remove Duplicates from Sorted Array - Solutions

## Approach 1: Two Pointers (Most Efficient)

### Python Solution
```python
def removeDuplicates(nums):
    # Handle empty array
    if not nums:
        return 0
        
    # Position where we'll place next unique number
    position = 1
    
    # Look at each number starting from second position
    for i in range(1, len(nums)):
        # If current number is different from previous
        if nums[i] != nums[i-1]:
            # Place it at position and move position forward
            nums[position] = nums[i]
            position += 1
            
    return position

```

### Step by Step Example
```
Array: [0,0,1,1,1,2,2,3,3,4]

Start: position = 1
[0,0,1,1,1,2,2,3,3,4]
 p i

Step 1: i=1, nums[1]=0
Same as previous, skip it

Step 2: i=2, nums[2]=1
Different! Place at position 1
[0,1,1,1,1,2,2,3,3,4]
   p i

Step 3: i=3, nums[3]=1
Same as previous, skip it

And so on...
```

### Go Solution
```go
func removeDuplicates(nums []int) int {
    // Handle empty array
    if len(nums) == 0 {
        return 0
    }
    
    // Position for next unique number
    position := 1
    
    // Check each number starting from second
    for i := 1; i < len(nums); i++ {
        // If different from previous number
        if nums[i] != nums[i-1] {
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
        // Handle empty array
        if (nums.length == 0) {
            return 0;
        }
        
        // Position for next unique number
        int position = 1;
        
        // Check each number starting from second
        for (int i = 1; i < nums.length; i++) {
            // If different from previous number
            if (nums[i] != nums[i-1]) {
                nums[position] = nums[i];
                position++;
            }
        }
        
        return position;
    }
}
```

## Approach 2: Using Set (Not In-Place, but Easy to Understand)
```python
def removeDuplicates(nums):
    # This is NOT the correct solution because it uses extra space
    # But it helps understand what we're trying to do
    unique = sorted(set(nums))
    for i in range(len(unique)):
        nums[i] = unique[i]
    return len(unique)
```

## Why First Approach is Better
1. Uses no extra space (O(1) space complexity)
2. Only one pass through array (O(n) time complexity)
3. Modifies array in-place
4. Meets all problem requirements

## Common Mistakes to Avoid

1. Wrong Starting Position
```python
# Wrong
position = 0  # Starts from beginning
# Right
position = 1  # First element is always unique
```

2. Wrong Comparison
```python
# Wrong
if nums[i] != nums[i+1]  # Looking forward
# Right
if nums[i] != nums[i-1]  # Looking backward
```

3. Not Handling Empty Array
```python
# Wrong
def removeDuplicates(nums):
    position = 1  # Crashes on empty array
    
# Right
def removeDuplicates(nums):
    if not nums:
        return 0
    position = 1
```

## Tips for Solving
1. Use the fact that array is sorted
2. Keep track of position for next unique element
3. Compare current element with previous one
4. Move elements only when needed
5. Return position as final count

## Visual Guide of the Process
```
Original:  [1, 1, 2, 2, 3]
           p  i
           
Step 1:    [1, 1, 2, 2, 3]  (skip, same as previous)
           p     i
           
Step 2:    [1, 2, 2, 2, 3]  (different, copy and move p)
              p     i
           
Step 3:    [1, 2, 2, 2, 3]  (skip, same as previous)
              p        i
           
Step 4:    [1, 2, 3, 2, 3]  (different, copy and move p)
                 p        i

Final:     [1, 2, 3, 2, 3]
Return: 3 (three unique numbers)