## Problem: Insert a String into another String in Java
- **Platform:** GFG
- **Link:** (https://www.geeksforgeeks.org/java/insert-a-string-into-another-string-in-java/)
- **Difficulty:** Easy
- **Topic:** Strings

### ✅ Solution (java)
```java
// Java program to insert a string into another string
// without using any pre-defined method

import java.lang.*;

class GFG {

    // Function to insert string
    public static String insertString(
        String originalString,
        String stringToBeInserted,
        int index)
    {

        // Create a new string
        String newString = new String();

        for (int i = 0; i < originalString.length(); i++) {

            // Insert the original string character
            // into the new string
            newString += originalString.charAt(i);

            if (i == index) {

                // Insert the string to be inserted
                // into the new string
                newString += stringToBeInserted;
            }
        }

        // return the modified String
        return newString;
    }

    // Driver code
    public static void main(String[] args)
    {

        // Get the Strings
        String originalString = "GeeksGeeks";
        String stringToBeInserted = "For";
        int index = 4;

        System.out.println("Original String: "
                           + originalString);
        System.out.println("String to be inserted: "
                           + stringToBeInserted);
        System.out.println("String to be inserted at index: "
                           + index);

        // Insert the String
        System.out.println("Modified String: "
                           + insertString(originalString,
                                          stringToBeInserted,
                                          index));
    }
}
// there are three methods - 
Without using any pre-defined method Approach:
Get the Strings and the index.
Create a new String
Traverse the string till the specified index and copy this into the new String.
Copy the String to be inserted into this new String
Copy the remaining characters of the first string into the new String
Return/Print the new String

Using StringBuilder Approach:
Get the Strings and the index.
Create a StringBuilder object
Append the first string till the specified index
Append the String to be inserted
Append the remaining characters of the first string
Return/Print the StringBuilder object

Using StringBuffer Approach:
Get the Strings and the index.
Create a StringBuffer object
Append the first string till the specified index
Append the String to be inserted
Append the remaining characters of the first string
Return/Print the StringBuffer object

```java
public class Main {
    public static void main(String[] args) {
        String originalString = "Hello World";
        String stringToBeInserted = "Java ";
        int index = 6;
        System.out.println(insertString(originalString, stringToBeInserted, index));
    }
    public static String insertString(String originalString,
                                      String stringToBeInserted,
                                      int index) {
        StringBuilder sb = new StringBuilder(originalString);
        sb.insert(index, stringToBeInserted);
        return sb.toString();
    }
}
