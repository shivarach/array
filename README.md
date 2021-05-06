# array
### Binary Search
#### Iterative
```java
        int[] input = {1, 2, 3 ,4 ,5 ,6 , 7, 8, 9};
       
        int left = 0;
        int right = input.length - 1;
        int target = 8;
        while (left <= right) {
            int mid = left + (right -left) / 2;
            if (input[mid] < target) {
                left = mid + 1;
            } else if (input[mid] > right) {
                right = mid - 1;
            } else {
                System.out.println(input[mid]);
                return;
            }
        }
```
#### Recursive
```java
    public static void binarySearch(int[] input, int lower, int higher, int target) {
        if (lower >= higher) return;
        int mid = lower + (higher - lower) / 2;
        if (input[mid] < target) {
            binarySearch(input, mid + 1, higher, target);
        }
        else if (input[mid] > target) {
            binarySearch(input, lower, mid, target);
        } else {
            System.out.println(target);
        }
    }
