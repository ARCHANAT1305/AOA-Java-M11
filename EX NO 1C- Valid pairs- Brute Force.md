
# EX 1C Valid Pairs using Brute Force Approach
## AIM:
To write a Java program to for given constraints.
Given an integer array nums and an integer k, return the number of pairs (i, j) where i < j such that |nums[i] - nums[j]| == k.

The value of |x| is defined as:

x if x >= 0.
-x if x < 0.

## Algorithm
1. Start and read the array size n, the elements of the array nums[], and the integer k.
2. Initialize count = 0 to store the number of valid pairs.
3. For each pair of indices (i, j) where i < j, calculate |nums[i] - nums[j]|.
4. If the absolute difference equals k, increment count by 1.
5. Print the final count and stop. 

## Program:
#### Developed by: ARCHANA T
#### Register Number: 212223240013
```
import java.util.Scanner;
public class CountPairsWithDifference {
    public static int countKDifference(int[] nums, int k) {
        int count = 0;
        int n = nums.length;
        for (int i = 0; i < n; i++) {
            for (int j = i + 1; j < n; j++) {
                if (Math.abs(nums[i] - nums[j]) == k) {
                    count++;
                }
            }
        }
        
        return count;
    }
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        int[] nums = new int[n];
        for (int i = 0; i < n; i++) {
            nums[i] = sc.nextInt();
        }
        int k = sc.nextInt();
        int result = countKDifference(nums, k);
        System.out.println(result);
        sc.close();
    }
}
```

## Output:

<img width="465" height="261" alt="image" src="https://github.com/user-attachments/assets/fa651a26-64aa-4e19-9cfe-a2ee5697fc73" />


## Result:
The program successfully implemented and the expected output is verified.
