# Remove Element - Solutions

## Approach 1: Two Pointers (Most Efficient)

### Python Solution
```python
def removeElement(nums, val):
    # k is where we'll place numbers we want to keep
    k = 0
    
    # Look at each number in the array
    for i in range(len(nums)):
        # If this number is not the one we want to remove
        if nums[i] != val:
            # Put it at position k and move k forward
            nums[k] = nums[i]
            k += 1
    
    # k is now how many numbers we kept
    return k
```

### Golang Solution
```go
func removeElement(nums []int, val int) int {
    // k is where we'll place numbers we want to keep
    k := 0
    
    // Look at each number in array
    for i := 0; i < len(nums); i++ {
        // If this number is not the one we want to remove
        if nums[i] != val {
            // Put it at position k and move k forward
            nums[k] = nums[i]
            k++
        }
    }
    
    // k is now how many numbers we kept
    return k
}
```

### Java Solution
```java
class Solution {
    public int removeElement(int[] nums, int val) {
        // k is where we'll place numbers we want to keep
        int k = 0;
        
        // Look at each number in array
        for (int i = 0; i < nums.length; i++) {
            // If this number is not the one we want to remove
            if (nums[i] != val) {
                // Put it at position k and move k forward
                nums[k] = nums[i];
                k++;
            }
        }
        
        // k is now how many numbers we kept
        return k;
    }
}
```

## Approach 2: Two Pointers from Both Ends

### Python Solution
```python
def removeElement(nums, val):
    # Start from both ends
    left = 0
    right = len(nums) - 1
    
    # Keep going until pointers meet
    while left <= right:
        # If left number needs to be removed
        if nums[left] == val:
            # Copy last number to this position
            nums[left] = nums[right]
            # Move right pointer in
            right -= 1
        else:
            # Move left pointer forward
            left += 1
    
    # left is now how many numbers we kept
    return left
```

## How These Solutions Work

### Approach 1 (Single Direction)
Think of it like organizing books on a shelf:
1. Start with an empty spot at the beginning (k = 0)
2. Look at each book:
   - If it's one we want to keep: put it in the next empty spot
   - If it's one we want to remove: skip it
3. Count how many books we kept

Example step by step:
```
Array: [3,2,2,3], remove 3
k = 0, i = 0: [3,2,2,3] (skip 3)
k = 0, i = 1: [2,2,2,3] (keep 2)
k = 1, i = 2: [2,2,2,3] (keep 2)
k = 2, i = 3: [2,2,2,3] (skip 3)
Return: 2
```

### Approach 2 (Two Ends)
Think of it like swapping items between shelves:
1. Look at item from left
2. If it needs to be removed:
   - Replace it with last item
   - Move last position in
3. If it can stay:
   - Move to next item

Example step by step:
```
Array: [3,2,2,3], remove 3
Start: [3,2,2,3], left=0, right=3
Step 1: [3,2,2,3] → swap → [3,2,2,3], right=2
Step 2: [2,2,2,3], left=1
Step 3: [2,2,2,3], left=2
Return: 2
```

## Which Solution to Use?
- Approach 1 (Single Direction):
  - Simpler to understand
  - Maintains relative order
  - Good when order matters

- Approach 2 (Two Ends):
  - Fewer moves needed
  - Doesn't maintain order
  - Good when order doesn't matter

## Common Mistakes to Avoid
1. Don't create a new array
2. Don't forget to return the count
3. Remember array indices start at 0
4. Be careful with edge cases:
   - Empty array
   - All elements are val
   - No elements are val