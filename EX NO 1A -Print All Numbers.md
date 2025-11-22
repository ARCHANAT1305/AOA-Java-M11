
# EX 1 A Print All Numbers 
## AIM:
To Write a Java program that takes an integer input N from the user and prints all the numbers from 1 to N, separated by spaces, on a single line..

## Algorithm
1. Start the program.
2. Read integer N from the user.
3. If N ≤ 0: Print "Invalid input. N must be greater than 0." and stop
4.Set counter i = 1  
5. Repeat while i ≤ N: Print i if i < N, print a space and increment i by 1
6. Stop the program.

## Program:
### Developed by: ARCHANA T
### Register Number: 212223240013 
```
//Type your code here
import java.util.*;
public class Sum1
{
    public static void main(String a[]){
        int n;
        Scanner sc=new Scanner(System.in);
        n=sc.nextInt();
        if(n>0){
            for (int i=1;i<=n;i++){
                System.out.print(i+" ");
            }
        }
        else{
            System.out.println("Invalid");
        }
        sc.close();
    }
}

```

## Output:

<img width="413" height="136" alt="image" src="https://github.com/user-attachments/assets/1460bd9e-c3b5-46e1-a36c-6ddfaf33df45" />


## Result:
The program successfully print all the numbers from 1 to N. 
