# Ex13 Fill the First 10 Elements of an Array with a Constant using Arrays.fill()
## DATE:
## AIM:
To write a Java program that fills the first 10 elements of an array with a constant value using the Arrays.fill() method.
## Algorithm
1. Start
2. Read the size of the array n
3. Create an integer array arr of size n
4. Read the constant value val
5. Determine limit = minimum(10, n)
6. Use Arrays.fill(arr, 0, limit, val) to fill first 10 elements
7. Display the array with updated values
8. Stop
 

## Program:
```java
/*
Program to FILL the first 10 elements of an array with a constant value using the Arrays.fill() method.
Developed by: HARI PRIYA M
RegisterNumber: 212224240047 
*/

import java.util.*;

public class Node {

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Enter array size: ");
        int n = sc.nextInt();

        int[] arr = new int[n];

        System.out.print("Enter constant value to fill: ");
        int val = sc.nextInt();

        int limit = Math.min(10, n);
        Arrays.fill(arr, 0, limit, val);

        System.out.println("Array after filling first 10 elements:");
        for (int num : arr) {
            System.out.print(num + " ");
        }

        sc.close();
    }
}

```

## Output:
<img width="450" height="253" alt="image" src="https://github.com/user-attachments/assets/bbdd71e0-cb9c-4b10-9dff-61f2477f1225" />



## Result:
The program successfully fills the first 10 elements of the array with the constant value 5 using the Arrays.fill() method.
