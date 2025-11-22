
# EX 1D Sorted Array using Divide and Conquer Approach.
## AIM:
To write a Java program to for given constraints.
Given two sorted arrays nums1 and nums2 of size m and n respectively, return the median of the two sorted arrays.
The overall run time complexity should be O(log (m+n)).

## Algorithm
1. Start and read two sorted arrays nums1 and nums2
2. Initialize pointers p1 and p2 to 0 and calculate the total combined length.
3. Iteratively pick the smaller element from both arrays until reaching the middle positions
4. If the total length is odd, the median is the current element; otherwise, it’s the average of the last two elements.
5. Print the median and stop.

## Program:
#### Developed by: ARCHANA T
#### Register Number: 212223240013 
```
import java.util.Scanner;
public class Solution {
    private int p1 = 0, p2 = 0;
    private int getMin(int[] nums1, int[] nums2) {
        if (p1 < nums1.length && p2 < nums2.length) {
            return nums1[p1] < nums2[p2] ? nums1[p1++] : nums2[p2++];
        } else if (p1 < nums1.length) {
            return nums1[p1++];
        } else if (p2 < nums2.length) {
            return nums2[p2++];
        }
        return -1; // Should not reach here if input is valid
    }
    public double findMedianSortedArrays(int[] nums1, int[] nums2) {
        int totalLength = nums1.length + nums2.length;
        int midIndex1 = (totalLength - 1) / 2; 
        int midIndex2 = totalLength / 2;       
        int current = 0, prev = 0;
        for (int i = 0; i <= midIndex2; i++) {
            prev = current;
            current = getMin(nums1, nums2);
        }
        if (totalLength % 2 == 1) {
            return current;
        }
        return (prev + current) / 2.0;
    }
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        Solution sol = new Solution();
        int m = sc.nextInt();
        int[] nums1 = new int[m];
        for (int i = 0; i < m; i++) {
            nums1[i] = sc.nextInt();
        }
        int n = sc.nextInt();
        int[] nums2 = new int[n];
        for (int i = 0; i < n; i++) {
            nums2[i] = sc.nextInt();
        }
        double median = sol.findMedianSortedArrays(nums1, nums2);
        System.out.println("Median of the two sorted arrays = " + median);
        
        sc.close();
    }
}
```

## Output:

<img width="780" height="299" alt="image" src="https://github.com/user-attachments/assets/63ac35b7-7176-4584-8d09-2773ce4033b2" />


## Result:
The program successfully implemented and the expected output is verified.
