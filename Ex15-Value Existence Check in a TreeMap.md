# Ex15 Value Existence Check in a TreeMap
## DATE:
## AIM:
To write a Java program that checks whether a given value exists in a TreeMap.

## Algorithm
1. Start
2. Read the number of entries n
3. Create a TreeMap to store key-value pairs
4. Input n key-value pairs and insert them into the TreeMap
5. Read the value to search
6. Use containsValue() method to check if the value exists in the TreeMap
7. If true, display "Value exists in TreeMap"
8. Otherwise, display "Value does not exist in TreeMap"
9. Stop


## Program:
```java
/*
Program to checks whether a given value exists in a TreeMap.
Developed by: HARI PRIYA M
RegisterNumber: 212224240047 
*/
import java.util.*;

public class Node {

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Enter number of entries: ");
        int n = sc.nextInt();

        TreeMap<Integer, Integer> map = new TreeMap<>();

        System.out.println("Enter key-value pairs:");
        for (int i = 0; i < n; i++) {
            int key = sc.nextInt();
            int value = sc.nextInt();
            map.put(key, value);
        }

        System.out.print("Enter value to search: ");
        int val = sc.nextInt();

        boolean exists = map.containsValue(val);

        if (exists)
            System.out.println("Value exists in TreeMap");
        else
            System.out.println("Value does not exist in TreeMap");

        sc.close();
    }
}

```

## Output:
<img width="479" height="416" alt="image" src="https://github.com/user-attachments/assets/4758e5e2-f4b7-4dfb-81a4-2666ecfb6056" />



## Result:
Thus, the program successfully checks whether a specified value exists in a TreeMap using the containsValue() method.
