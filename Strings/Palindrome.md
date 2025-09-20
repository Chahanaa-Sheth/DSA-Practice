# Java Program to Check Whether a String is a Palindrome
- **Platform:** (GFG)
- **Link:** [palindrome](https://www.geeksforgeeks.org/java/java-program-to-check-whether-a-string-is-a-palindrome/)
- **Difficulty:** Easy 
- **Topic:** (Strings)


## 💡 Approach
(convert the string to lowercase first so case insensitivity isn't an issue)
(can reverse the string using a loop)
(string.equals(string) returns a boolean value)
(Time Complexity: O(n)
Space Complexity: O(n))

## 🧑‍💻 Solution ( Java )
```java
import java.util.*;

class Codechef {
    // Function to check if string is palindrome
    public static boolean ispal(String s) {
        s = s.toLowerCase();

        String rev = "";  // (fix: use empty string instead of " ")
        for (int i = s.length() - 1; i >= 0; i--) {
            rev = rev + s.charAt(i);
        }

        return s.equals(rev);
    }

    public static void main(String[] args) {
        String s = "level";

        // Check if the string is a palindrome
        boolean res = ispal(s);

        // Print the result
        if (res) {
            System.out.println("\"" + s + "\" is a palindrome.");
        } else {
            System.out.println("\"" + s + "\" is not a palindrome.");
        }
    }
}

