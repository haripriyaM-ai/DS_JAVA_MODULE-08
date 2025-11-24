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
