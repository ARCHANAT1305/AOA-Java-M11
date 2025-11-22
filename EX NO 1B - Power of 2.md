
# EX 1B Power of 2
## AIM:
To write a Java program to for given constraints.Given an integer n, return true if it is a power of two. Otherwise, return false.

An integer n is a power of two, if there exists an integer x such that n == 2x.

## Algorithm
1. Start and read the integer input n.
2. Check if n is greater than 0.
3. Compute (n & (n - 1)).
4. If the result equals 0, then n is a power of two.
5. Display the result and stop. 

## Program:
### Developed by: ARCHANA T
### Register Number: 212223240013
```
import java.util.Scanner;
public class Solution {
    public boolean isPowerOfTwo(int n) {
     return n > 0 && (n & (n - 1)) == 0;     
    }
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        Solution sol = new Solution();
        int n = scanner.nextInt();
        boolean result = sol.isPowerOfTwo(n);
        System.out.println(result);

        scanner.close();
    }
}
```

## Output:
<img width="393" height="213" alt="image" src="https://github.com/user-attachments/assets/fd6cea98-ab5d-40e4-8feb-59ffff30cbcc" />



## Result:
The program successfully implemented and the expected output is verified.
