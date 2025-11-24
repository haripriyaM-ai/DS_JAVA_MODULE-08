# Ex11 Convert HashSet to ArrayList in Java
## DATE:
## AIM:
To convert a collection of distinct integers stored in a HashSet into an ArrayList and display its contents.
## Algorithm
1. Start
2. Read the number of elements n
3. Create a HashSet to store distinct integers
4. Input elements and insert them into the HashSet
5. Create an ArrayList and initialize it using the HashSet
6. Display all elements of the ArrayList
7. Stop


## Program:
```java
/*
Program to To convert a collection of distinct integers stored in a HashSet into an ArrayList and display its contents.
Developed by: HARI PRIYA M
RegisterNumber: 212224240047
*/

import java.util.*;

public class Node {

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Enter number of elements in HashSet: ");
        int n = sc.nextInt();

        HashSet<Integer> set = new HashSet<>();
        System.out.println("Enter elements:");
        for (int i = 0; i < n; i++) {
            set.add(sc.nextInt());
        }

        ArrayList<Integer> list = new ArrayList<>(set);

        System.out.println("ArrayList contents:");
        for (int num : list) {
            System.out.print(num + " ");
        }

        sc.close();
    }
}
```

## Output:
<img width="474" height="242" alt="image" src="https://github.com/user-attachments/assets/7c27ae48-bca6-48dc-b49d-2718354552b1" />



## Result:
The program successfully converts a collection of distinct integers stored in a HashSet into an ArrayList
