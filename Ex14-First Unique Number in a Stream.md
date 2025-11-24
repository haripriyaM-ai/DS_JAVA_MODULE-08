# Ex14 Tracking the First Unique Number in a Stream using LinkedHashMap
## DATE:
## AIM:
To implement a program that tracks the first unique (non-repeating) number in a stream of integers using a LinkedHashMap.

## Algorithm
1. Start
2. Read the total number of stream elements n
3. Create a LinkedHashMap to store each number and its frequency count
4. For each number in the input stream:
      a. Insert into map or increment its count if it already exists
      b. Traverse keys of the LinkedHashMap in insertion order
      c. Identify the first number whose count is 1
      d. Display the first unique number if found, otherwise print "No unique number currently"
5. Stop


## Program:
```java
/*
Program to tracks the first unique (non-repeating) number in a stream of integers using a LinkedHashMap.
Developed by: HARI PRIYA M 
RegisterNumber: 212224240047 
*/

import java.util.*;

public class Node {

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Enter count of stream values: ");
        int n = sc.nextInt();

        LinkedHashMap<Integer, Integer> map = new LinkedHashMap<>();

        System.out.println("Enter stream values:");
        for (int i = 0; i < n; i++) {
            int num = sc.nextInt();
            map.put(num, map.getOrDefault(num, 0) + 1);

            Integer firstUnique = null;
            for (int key : map.keySet()) {
                if (map.get(key) == 1) {
                    firstUnique = key;
                    break;
                }
            }

            if (firstUnique != null)
                System.out.println("First unique so far: " + firstUnique);
            else
                System.out.println("No unique number currently");
        }

        sc.close();
    }
}

```

## Output:
<img width="496" height="459" alt="image" src="https://github.com/user-attachments/assets/573bb9d2-c0d5-48a2-b556-0a08e3d9106c" />



## Result:
The program successfully tracks and returns the first unique number at any point in the integer stream using a LinkedHashMap.
