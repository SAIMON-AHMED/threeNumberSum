### Three Number Sum

---

#### Description

The `threeNumberSum` function identifies all unique triplets in an array that add up to a given target sum. It ensures that the triplets are returned in ascending order within each triplet and that the overall list of triplets is also sorted.

---

#### Function Signature

```javascript
function threeNumberSum(array, targetSum)
```

---

#### Parameters

1. **array**: `number[]`  
   - A non-empty array of integers.
2. **targetSum**: `number`  
   - The target sum for which triplets are to be found.

---

#### Returns

- **result**: `number[][]`  
  - A list of triplets, where each triplet contains three integers that add up to the `targetSum`. The triplets are sorted in ascending order.

---

#### Time and Space Complexity

- **Time Complexity**: `O(n^2)`  
  The algorithm iterates through the array and performs a two-pointer search for each element, leading to a quadratic time complexity.

- **Space Complexity**: `O(n)`  
  Sorting the input array requires additional space.

---

#### Algorithm Explanation

1. **Sorting**:  
   The function begins by sorting the input array in ascending order. Sorting simplifies the process of finding triplets and ensures they are returned in the correct order.

2. **Outer Loop**:  
   An outer loop iterates through the array. For each element:
   - It fixes the current element as the first number in the triplet.
   - Two pointers (`left` and `right`) are used to find two other numbers that, together with the fixed element, sum up to the `targetSum`.

3. **Two-Pointer Search**:  
   - The left pointer starts just after the fixed element, and the right pointer starts at the end of the array.
   - The sum of the three elements is calculated.
   - If the sum equals the `targetSum`, the triplet is added to the result.  
   - If the sum is less than the `targetSum`, the left pointer is moved forward to increase the sum.  
   - If the sum is greater than the `targetSum`, the right pointer is moved backward to decrease the sum.

4. **Result Construction**:  
   All valid triplets are stored in the result array and returned at the end of the function.

---

#### Examples

##### Example 1:
```javascript
threeNumberSum([1, 2, 3, 4, 5, 6], 10);
// Output: [[1, 3, 6], [2, 3, 5], [1, 4, 5]]
```

##### Example 2:
```javascript
threeNumberSum([-1, 0, 1, 2, -1, -4], 0);
// Output: [[-1, -1, 2], [-1, 0, 1]]
```

---

#### Edge Cases

1. **Empty Input Array**:  
   If the input array is empty, the function will return an empty list.

2. **No Valid Triplets**:  
   If no triplets match the target sum, the function will return an empty list.

3. **Duplicate Elements**:  
   The function does not explicitly handle duplicate elements but ensures that the result does not contain duplicate triplets by leveraging the sorted input array.

---

#### Usage

To use this function, ensure it is exported and imported correctly in your JavaScript project:

```javascript
const { threeNumberSum } = require('./path-to-file');
```

---

#### License

This project is licensed under the MIT License. Feel free to use and modify the code for personal and commercial purposes.
