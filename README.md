# Single Number

Given a non-empty array of integers, every element appears twice except for one. Find that single one.

Note: Your algorithm should have a linear runtime complexity. Could you implement it without using extra memory?

```
Example 1:

Input: [2,2,1]
Output: 1

Example 2:

Input: [4,1,2,1,2]
Output: 4
```

### Implementation

```java
import java.util.HashSet;
import java.util.Set;

public class App {

	public static void main(String[] args) {
		int[] nums = { 4,1,2,1,2};
		System.out.println(singleNumber(nums));
	}
	
	public static int singleNumber(int[] nums) {
		Set<Integer> set = new HashSet<>();
		for(int i : nums) {
			if(!set.contains(i)) {
				set.add(i);
			} else {
				set.remove(i);
			}
		}
		for(int singleNumber : set) {
			return singleNumber;
		}
		return -1;
	}
}
```
Above implementation have runtime complexity of O(n) and space complexity of O(n)
```
Runtime Complexity = O(n)
Space Complexity   = O(n)
```
