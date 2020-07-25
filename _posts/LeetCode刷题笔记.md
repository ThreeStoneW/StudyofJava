# LeetCode刷题笔记
>记录刷LeetCode时的一些细节知识
### Java数组使用
+ 创建空数组
`new int[0];`
+ 返回值中新建数组
`return new int[]{0,0};`

### 关于return使用
如果根据输入可能出现无返回值的情况时，要抛出异常  
例：
```java
class Solution {
    public int[] twoSum(int[] nums, int target) {
        for (int i = 0; i < nums.length; i++) {
            for (int j = i + 1; j < nums.length; j++) {
                if (nums[j] == target - nums[i]) {
                    return new int[] { i, j };
                }
            }
        }
        throw new IllegalArgumentException("No two sum solution");
    }
}

```

### String数组方法
`charAt()`方法，可以返回字符串相应位置的单个字符  
`length()`方法，返回string的长度；注意数组的长度函数为`length`

### 二分法查找的Java实现
```java
public int searchInsert(int[] nums, int target) {
        int n = nums.length;
        int left = 0, right = n - 1, ans = n;
        while (left <= right) {
            int mid = ((right - left) >> 1) + left;//右移一位等同于除以二
            if (target <= nums[mid]) {
                ans = mid;
                right = mid - 1;
            } else {
                left = mid + 1;
            }
        }
        return ans;
    }
```