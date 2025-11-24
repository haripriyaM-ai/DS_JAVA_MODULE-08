# Ex12 Add Elements from an Array into a TreeSet
## DATE:
## AIM:
To write a Java program that adds elements from an array into a TreeSet and displays the elements in sorted order.
## Algorithm
1. Start
2. Read number of elements n
3. Create an integer array arr of size n
4. Input array elements
5. Create a TreeSet to store integers
6. Insert each element from the array into the TreeSet
7. Display the contents of the TreeSet in sorted order
8. Stop
  

## Program:
```java
/*
Program that adds elements from an array into a TreeSet and displays the elements in sorted order.
Developed by: HARI PRIYA M
RegisterNumber: 212224240047 
*/

import java.util.*;

public class Node {

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Enter number of elements in array: ");
        int n = sc.nextInt();

        int[] arr = new int[n];
        System.out.println("Enter array elements:");
        for (int i = 0; i < n; i++) {
            arr[i] = sc.nextInt();
        }

        TreeSet<Integer> set = new TreeSet<>();
        for (int num : arr) {
            set.add(num);
        }

        System.out.println("TreeSet elements in sorted order:");
        for (int num : set) {
            System.out.print(num + " ");
        }

        sc.close();
    }
}

```

## Output:
<img width="461" height="261" alt="image" src="https://github.com/user-attachments/assets/e7df43da-a8d4-4886-8edd-ca918f319316" />



## Result:
The program successfully adds elements from an array into a TreeSet.
