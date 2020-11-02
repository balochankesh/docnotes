# **JAVA**

---

## Datatypes

![fig1](printf1.png)

## **Declaration**

```java
public class Solution {

    public static void main(String[] args) {
        System.out.println("Hello, World.");
    }
}
```

```
//OUTPUT

Hello, World.
```

---

## **INPUT / OUTPUT**

print , println.

```java
Scanner scanner = new Scanner(System.in);
String myString = scanner.next();
int myInt = scanner.nextInt();
scanner.close();

System.out.println("myString is: " + myString);
System.out.println("myInt is: " + myInt);
```

```
  //INPUT
  Hi 5
  //OUTPUT
  myString is: Hi
  myInt is: 5
```

### Printf [formatting]

![fig2](printf2.png)

![fig3](printf3.png)

![img4](https://i.imgur.com/UaAGxEE.png)

---

## **Strings**

### Methods

| Method                                                                                     | Description                                                                                                                             | Return Type  |
| ------------------------------------------------------------------------------------------ | --------------------------------------------------------------------------------------------------------------------------------------- | ------------ |
| [charAt()](https://www.w3schools.com/java/ref_string_charat.asp)                           | Returns the character at the specified index (position)                                                                                 | char         |
| [codePointAt()](https://www.w3schools.com/java/ref_string_codepointat.asp)                 | Returns the Unicode of the character at the specified index                                                                             | int          |
| [codePointBefore()](https://www.w3schools.com/java/ref_string_codepointbefore.asp)         | Returns the Unicode of the character before the specified index                                                                         | int          |
| [codePointCount()](https://www.w3schools.com/java/ref_string_codepointcount.asp)           | Returns the Unicode in the specified text range of this String                                                                          | int          |
| [compareTo()](https://www.w3schools.com/java/ref_string_compareto.asp)                     | Compares two strings lexicographically                                                                                                  | int          |
| [compareToIgnoreCase()](https://www.w3schools.com/java/ref_string_comparetoignorecase.asp) | Compares two strings lexicographically, ignoring case differences                                                                       | int          |
| [concat()](https://www.w3schools.com/java/ref_string_concat.asp)                           | Appends a string to the end of another string                                                                                           | String       |
| [contains()](https://www.w3schools.com/java/ref_string_contains.asp)                       | Checks whether a string contains a sequence of characters                                                                               | boolean      |
| [contentEquals()](https://www.w3schools.com/java/ref_string_contentequals.asp)             | Checks whether a string contains the exact same sequence of characters <br>of the specified CharSequence or StringBuffer                | boolean      |
| [copyValueOf()](https://www.w3schools.com/java/ref_string_copyvalueof.asp)                 | Returns a String that represents the characters of the character array                                                                  | String       |
| [endsWith()](https://www.w3schools.com/java/ref_string_endswith.asp)                       | Checks whether a string ends with the specified character(s)                                                                            | boolean      |
| [equals()](https://www.w3schools.com/java/ref_string_equals.asp)                           | Compares two strings. Returns true if the strings are equal, and false <br>if not                                                       | boolean      |
| [equalsIgnoreCase()](https://www.w3schools.com/java/ref_string_equalsignorecase.asp)       | Compares two strings, ignoring case considerations                                                                                      | boolean      |
| format()                                                                                   | Returns a formatted string using the specified locale, format string, and arguments                                                     | String       |
| getBytes()                                                                                 | Encodes this String into a sequence of bytes using the named charset, storing the result into a new byte array                          | byte[]       |
| getChars()                                                                                 | Copies characters from a string to an array of chars                                                                                    | void         |
| [hashCode()](https://www.w3schools.com/java/ref_string_hashcode.asp)                       | Returns the hash code of a string                                                                                                       | int          |
| [indexOf()](https://www.w3schools.com/java/ref_string_indexof.asp)                         | Returns the position of the first found occurrence of specified characters in a string                                                  | int          |
| intern()                                                                                   | Returns the index within this string of the first occurrence of <br>the specified character, starting the search at the specified index | String       |
| [isEmpty()](https://www.w3schools.com/java/ref_string_isempty.asp)                         | Checks whether a string is empty or not                                                                                                 | boolean      |
| [lastIndexOf()](https://www.w3schools.com/java/ref_string_lastindexof.asp)                 | Returns the position of the last found occurrence of specified characters in a string                                                   | int          |
| [length()](https://www.w3schools.com/java/ref_string_length.asp)                           | Returns the length of a specified string                                                                                                | int          |
| matches()                                                                                  | Searches a string for a match against a regular expression, and returns the matches                                                     | boolean      |
| offsetByCodePoints()                                                                       | Returns the index within this String that is offset from the given index by codePointOffset code points                                 | int          |
| regionMatches()                                                                            | Tests if two string regions are equal                                                                                                   | boolean      |
| [replace()](https://www.w3schools.com/java/ref_string_replace.asp)                         | Searches a string for a specified value, and returns a new string where the specified values are replaced                               | String       |
| replaceFirst()                                                                             | Replaces the first occurrence of a substring that matches the given regular expression with the given replacement                       | String       |
| replaceAll()                                                                               | Replaces each substring of this string that matches the given regular expression with the given replacement                             | String       |
| split()                                                                                    | Splits a string into an array of substrings                                                                                             | String[]     |
| [startsWith()](https://www.w3schools.com/java/ref_string_startswith.asp)                   | Checks whether a string starts with specified characters                                                                                | boolean      |
| subSequence()                                                                              | Returns a new character sequence that is a subsequence of this sequence                                                                 | CharSequence |
| substring()                                                                                | Extracts the characters from a string, beginning at a specified start position, and through the specified number of character           | String       |
| toCharArray()                                                                              | Converts this string to a new character array                                                                                           | char[]       |
| [toLowerCase()](https://www.w3schools.com/java/ref_string_tolowercase.asp)                 | Converts a string to lower case letters                                                                                                 | String       |
| toString()                                                                                 | Returns the value of a String object                                                                                                    | String       |
| [toUpperCase()](https://www.w3schools.com/java/ref_string_touppercase.asp)                 | Converts a string to upper case letters                                                                                                 | String       |
| [trim()](https://www.w3schools.com/java/ref_string_trim.asp)                               | Removes whitespace from both ends of a string                                                                                           | String       |
| valueOf()                                                                                  | Returns the primitive value of a String object                                                                                          | String       |

```java
//split delimiter example


String str = "This is an example string, right?  Yes!";
String delims = "[ .,?!]+";
String[] tokens = str.split(delims);
```

![](https://i.imgur.com/WsEhrTY.png)



### Conversions

![img5](https://i.imgur.com/yvVjDAi.png)

![fig6](https://i.imgur.com/ajH1pYv.png)

---

## **ARRAYS**

### declare

```java
int intArray[];    //declaring array
intArray = new int[20];  // allocating memory to array


int[] intArray = new int[20]; // combining both statements in one


// returning  array 
        return new int[]{1,2,3}; 
```

1. The elements in the array allocated by *new* will automatically be initialized to **zero** (for numeric types), **false** (for boolean), or **null** (for reference types).Refer [Default array values in Java](https://www.geeksforgeeks.org/default-array-values-in-java/)
2. Obtaining an array is a two-step process. First, you must declare a 
   variable of the desired array type. Second, you must allocate the memory
   that will hold the array, using new, and assign it to the array 
   variable. Thus, **in Java all arrays are dynamically allocated.**

### Array literal

```java
 int[] intArray = new int[]{ 1,2,3,4,5,6,7,8,9,10 }; 
```

### print

```java
for (int e: arr) {
    System.out.println(e)
}        
```

### Methods

- length

- add

- `Arrays.binarySearch(Arr, ele));`

---

## **Hash Maps**

```java
import java.util.HashMap; // import the HashMap class

HashMap<String, String> capitalCities = new HashMap<String, String>();
```

### Put Data(example)

```java
// Add keys and values (Country, City)
    capitalCities.put("England", "London");
    capitalCities.put("Germany", "Berlin");
    capitalCities.put("Norway", "Oslo");
    capitalCities.put("USA", "Washington DC");
```

### Print

```java
System.out.println(capitalCities);
```

```
//output
{USA=Washington DC, Norway=Oslo, England=London, Germany=Berlin} 
```

### Methods

- get()

- remove()

- clear()

- size()

- keySet()

- values()

- containsKey()

---

## **Regular Expressions**

- **Pattern Class** − A Pattern object is a compiled 
  representation of a regular expression. The Pattern class provides no 
  public constructors. To create a pattern, you must first invoke one of 
  its public static **compile()** methods, which will then return a Pattern object. These methods accept a regular expression as the first argument.

- **Matcher Class** − A Matcher object is the engine that 
  interprets the pattern and performs match operations against an input 
  string. Like the Pattern class, Matcher defines no public constructors. 
  You obtain a Matcher object by invoking the **matcher()** method on a Pattern object.

- **PatternSyntaxException** − A PatternSyntaxException object is an unchecked exception that indicates a syntax error in a regular expression pattern.



### Cheatsheet

| Character classes         |                                |
| ------------------------- | ------------------------------ |
| .                         | any character except newline   |
| \w\d\s                    | word, digit, whitespace        |
| \W\D\S                    | not word, digit, whitespace    |
| [abc]                     | any of a, b, or c              |
| [^abc]                    | not a, b, or c                 |
| [a-g]                     | character between a & g        |
| Anchors                   |                                |
| ^abc$                     | start / end of the string      |
| \b\B                      | word, not-word boundary        |
| Escaped characters        |                                |
| \.\*\\                    | escaped special characters     |
| \t\n\r                    | tab, linefeed, carriage return |
| Groups & Lookaround       |                                |
| (abc)                     | capture group                  |
| \1                        | backreference to group #1      |
| (?:abc)                   | non-capturing group            |
| (?=abc)                   | positive lookahead             |
| (?!abc)                   | negative lookahead             |
| Quantifiers & Alternation |                                |
| a*a+a?                    | 0 or more, 1 or more, 0 or 1   |
| a{5}a{2,}                 | exactly five, two or more      |
| a{1,3}                    | between one & three            |
| a+?a{2,}?                 | match as few as possible       |
| ab\|cd                    | match ab or cd                 |

### Syntax

```java
//example


import java.util.regex.Matcher;
import java.util.regex.Pattern;

public class RegexMatches {

   public static void main( String args[] ) {
      // String to be scanned to find the pattern.
      String line = "This order was placed for QT3000! OK?";
      String pattern = "(.*)(\\d+)(.*)";

      // Create a Pattern object
      Pattern r = Pattern.compile(pattern);

      // Now create matcher object.
      Matcher m = r.matcher(line);
      if (m.find( )) {
         System.out.println("Found value: " + m.group(0) );
         System.out.println("Found value: " + m.group(1) );
         System.out.println("Found value: " + m.group(2) );
      }else {
         System.out.println("NO MATCH");
      }
   }
}
```

```
//OUTPUT

Found value: This order was placed for QT3000! OK?
Found value: This order was placed for QT300
Found value: 0
```

### Methods

| Sr.No. | Method & Description                                                                                                                                          |
| ------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 1      | **public int start()** Returns the start index of the previous match.                                                                                         |
| 2      | **public int start(int group)** Returns the start index of the subsequence captured by the given group during the previous match operation.                   |
| 3      | **public int end()** Returns the offset after the last character matched.                                                                                     |
| 4      | **public int end(int group)** Returns the offset after the last character of the subsequence captured by the given group during the previous match operation. |

| Sr.No. | Method & Description                                                                                                                                                                           |
| ------ | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 1      | **public boolean lookingAt()** Attempts to match the input sequence, starting at the beginning of the region, against the pattern.                                                             |
| 2      | **public boolean find()** Attempts to find the next subsequence of the input sequence that matches the pattern.                                                                                |
| 3      | **public boolean find(int start)** Resets this matcher and then attempts to find the next subsequence of<br> the input sequence that matches the pattern, starting at the specified <br>index. |
| 4      | **public boolean matches()** Attempts to match the entire region against the pattern.                                                                                                          |

| Sr.No. | Method & Description                                                                                                                                                                                                                                     |
| ------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 1      | **public Matcher appendReplacement(StringBuffer sb, String replacement)** Implements a non-terminal append-and-replace step.                                                                                                                             |
| 2      | **public StringBuffer appendTail(StringBuffer sb)** Implements a terminal append-and-replace step.                                                                                                                                                       |
| 3      | **public String replaceAll(String replacement)** Replaces every subsequence of the input sequence that matches the pattern with the given replacement string.                                                                                            |
| 4      | **public String replaceFirst(String replacement)** Replaces the first subsequence of the input sequence that matches the pattern with the given replacement string.                                                                                      |
| 5      | **public static String quoteReplacement(String s)** Returns a literal replacement String for the specified String. This <br>method produces a String that will work as a literal replacement **s** in the appendReplacement method of the Matcher class. |
