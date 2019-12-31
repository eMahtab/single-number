# Single Number

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
