# Merge Sorted Array - Solutions

## Solution 1: Start From the End (Most Efficient)

### Python Solution
```python
def merge(nums1, m, nums2, n):
    # p1 points to last real number in nums1
    # p2 points to last number in nums2
    # p points to last position in final array
    p1 = m - 1
    p2 = n - 1
    p = m + n - 1

    # While we still have numbers to process in nums2
    while p2 >= 0:
        # If we still have numbers in nums1 AND current nums1 number is bigger
        if p1 >= 0 and nums1[p1] > nums2[p2]:
            # Put nums1 number at the end
            nums1[p] = nums1[p1]
            p1 -= 1
        else:
            # Put nums2 number at the end
            nums1[p] = nums2[p2]
            p2 -= 1
        # Move to next position from end
        p -= 1
```

### Golang Solution
```go
func merge(nums1 []int, m int, nums2 []int, n int) {
    // Create three pointers
    // p1: last element in nums1
    // p2: last element in nums2
    // p: last position in result
    p1 := m - 1
    p2 := n - 1
    p := m + n - 1

    // Continue until we process all nums2 elements
    for p2 >= 0 {
        // If nums1 has elements AND current nums1 element is bigger
        if p1 >= 0 && nums1[p1] > nums2[p2] {
            // Place nums1 element at the end
            nums1[p] = nums1[p1]
            p1--
        } else {
            // Place nums2 element at the end
            nums1[p] = nums2[p2]
            p2--
        }
        // Move to next position from end
        p--
    }
}
```

### Java Solution
```java
class Solution {
    public void merge(int[] nums1, int m, int[] nums2, int n) {
        // Create three pointers
        // p1: points to last element in nums1
        // p2: points to last element in nums2
        // p: points to last position in result
        int p1 = m - 1;
        int p2 = n - 1;
        int p = m + n - 1;

        // Continue until we process all nums2 elements
        while (p2 >= 0) {
            // If nums1 has elements AND current nums1 element is bigger
            if (p1 >= 0 && nums1[p1] > nums2[p2]) {
                // Place nums1 element at the end
                nums1[p] = nums1[p1];
                p1--;
            } else {
                // Place nums2 element at the end
                nums1[p] = nums2[p2];
                p2--;
            }
            // Move to next position from end
            p--;
        }
    }
}
```

## Solution 2: Using Extra Space (Easier to Understand)

### Python Solution
```python
def merge(nums1, m, nums2, n):
    # Make a copy of the first m elements of nums1
    # This is like making a backup of our cards
    nums1_copy = nums1[:m]
    
    # Pointers for nums1_copy and nums2
    p1 = 0  # Points to start of nums1_copy
    p2 = 0  # Points to start of nums2
    
    # Pointer for where we're placing numbers in nums1
    p = 0
    
    # Compare elements from both arrays and place them in order
    while p1 < m and p2 < n:
        if nums1_copy[p1] <= nums2[p2]:
            # If nums1 number is smaller, use it
            nums1[p] = nums1_copy[p1]
            p1 += 1
        else:
            # If nums2 number is smaller, use it
            nums1[p] = nums2[p2]
            p2 += 1
        p += 1
    
    # If there are remaining elements in nums1_copy, add them
    while p1 < m:
        nums1[p] = nums1_copy[p1]
        p1 += 1
        p += 1
    
    # If there are remaining elements in nums2, add them
    while p2 < n:
        nums1[p] = nums2[p2]
        p2 += 1
        p += 1
```

### How Both Solutions Work

#### Solution 1 (Starting from End):
1. Create three pointers:
   - p1: points to last real number in nums1
   - p2: points to last number in nums2
   - p: points to last position where we'll put numbers

2. Compare numbers from end:
   - If nums1 number is bigger: put it at the end
   - If nums2 number is bigger: put it at the end
   - Move pointer to next position

3. Advantages:
   - No extra space needed
   - Doesn't overwrite numbers we still need
   - Very efficient

#### Solution 2 (Using Extra Space):
1. Make a copy of numbers in nums1
2. Start from beginning of both arrays
3. Compare numbers and put smaller one first
4. Add any remaining numbers at the end

This solution is:
- Easier to understand
- Uses extra memory
- More like how we would do it by hand

## Common Pitfalls to Avoid
1. Don't forget to check if arrays are empty
2. Be careful with array indices (don't go past the beginning)
3. Remember that nums1 has extra space at the end

## Which Solution to Use?
- For interviews: Use Solution 1 (from end) - it's more efficient
- For learning: Start with Solution 2 - it's easier to understand
- For practice: Try to implement both to understand trade-offs

## Time and Space Complexity
Both Solutions:
- Time: O(m + n) - we look at each number once
- Space: 
  - Solution 1: O(1) - no extra space
  - Solution 2: O(m) - needs space for nums1 copy