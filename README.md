# java_cheatsheet
### Getting Started
<br>Hello.java

<br>public class Hello {
  // main method
<br>  public static void main(String[] args)
  {
   <br>// Output: Hello, world!
   <br> System.out.println("Hello, world!");
  }
}
## Compiling and running


<br>$ javac Hello.java
<br>$ java Hello
Hello, world!
## Variables

int num = 5;<br>                                                                                                                               <br>
float floatNum = 5.99f;<br>                                                                                                                    <br>
char letter = 'D';<br>  <br>
boolean bool = true;<br><br>
String site = "tgc";<br><br>
## Primitive Data Types
Data Type	Size	Default	Range <br>
byte	1 byte	0	-128 to 127<br>
short	2 byte	0	-215 to 215-1<br>
int	4 byte	0	-231 to 231-1<br>
long	8 byte	0	-263 to 263-1<br>
float	4 byte	0.0f	N/A<br>
double	8 byte	0.0d	N/A<br>
char	2 byte	\u0000	0 to 65535<br>
boolean	N/A	false	true / false<br>
## Strings

String first = "John";<br><br>
String last = "Doe";<br><br>
String name = first + " " + last;<br><br>
System.out.println(name);<br><br>
See: Strings<br>

## Loops

String word = "TGC";<br><br>
for (char c: word.toCharArray()) {
  System.out.print(c + "-");<br>
}
// Outputs: T-G-C-
See: Loops

## Arrays<br>

char[] chars = new char[10];<br><br>
chars[0] = 'a'<br>
chars[1] = 'b'<br>

String[] letters = {"A", "B", "C"};<br>
int[] mylist = {100, 200};<br>
boolean[] answers = {true, false};<br>
See: Arrays

## Swap

int a = 1;<br>
int b = 2;<br>
System.out.println(a + " " + b);<br> // 1 2

int temp = a;<br>
a = b;<br>
b = temp;<br>
System.out.println(a + " " + b);<br> // 2 1
## Type Casting

// Widening
// byte<short<int<long<float<double
int i = 10;<br>
long l = i;<br>               // 10

// Narrowing 
double d = 10.02;<br>
long l = (long)d;<br>         // 10

String.valueOf(10);<br>       // "10"
Integer.parseInt("10");<br>   // 10
Double.parseDouble("10");<br> // 10.0
## Conditionals

int j = 10;<br>

if (j == 10) {
  System.out.println("I get printed");<br>
} else if (j > 10) {
  System.out.println("I don't");<br>
} else {
  System.out.println("I also don't");<br>
}
See: Conditionals

## User Input

Scanner in = new Scanner(System.in);<br>
String str = in.nextLine();<br>
System.out.println(str);<br>

int num = in.nextInt();<br>
System.out.println(num);<br>
## Java Strings
Basic

String str1 = "value";<br> 
String str2 = new String("value");<br>
String str3 = String.valueOf(123);<br>
## Concatenation

String s = 3 + "str" + 3;<br>     // 3str3
String s = 3 + 3 + "str";<br>     // 6str
String s = "3" + 3 + "str";<br>   // 33str
String s = "3" + "3" + "23";<br>  // 3323
String s = "" + 3 + 3 + "23";<br> // 3323
String s = 3 + 3 + 23;<br>        // 29
## StringBuilder
StringBuilder sb = new StringBuilder(10);<br>


┌───┬───┬───┬───┬───┬───┬───┬───┬───┐
|   |   |   |   |   |   |   |   |   |
└───┴───┴───┴───┴───┴───┴───┴───┴───┘
0   1   2   3   4   5   6   7   8   9
sb.append("QuickRef");<br>


┌───┬───┬───┬───┬───┬───┬───┬───┬───┐
| Q | u | i | c | k | R | e | f |   |
└───┴───┴───┴───┴───┴───┴───┴───┴───┘
0   1   2   3   4   5   6   7   8   9
sb.delete(5, 9);<br>


┌───┬───┬───┬───┬───┬───┬───┬───┬───┐
| Q | u | i | c | k |   |   |   |   |
└───┴───┴───┴───┴───┴───┴───┴───┴───┘
0   1   2   3   4   5   6   7   8   9
sb.insert(0, "My ");<br>


┌───┬───┬───┬───┬───┬───┬───┬───┬───┐
| M | y |   | Q | u | i | c | k |   |
└───┴───┴───┴───┴───┴───┴───┴───┴───┘
0   1   2   3   4   5   6   7   8   9
sb.append("!");<br>


┌───┬───┬───┬───┬───┬───┬───┬───┬───┐
| M | y |   | Q | u | i | c | k | ! |
└───┴───┴───┴───┴───┴───┴───┴───┴───┘
0   1   2   3   4   5   6   7   8   9
## Comparison

String s1 = new String("Quick");<br> 
String s2 = new String("Q");<br> 

s1 == s2          // false
s1.equals(s2)     // true

"AB".equalsIgnoreCase("ab")  // true
## Manipulation

String str = "Abcd";<br>

str.toUpperCase();<br>     // ABCD
str.toLowerCase();<br>     // abcd
str.concat("#");<br>       // Abcd#
str.replace("b", "-");<br> // A-cd

"  abc ".trim();<br>       // abc
"ab".toCharArray();<br>    // {'a', 'b'}
## Information

String str = "abcd";<br>

str.charAt(2);<br>       // c
str.indexOf("a")     // 0
str.indexOf("z")     // -1
str.length();<br>        // 4
str.toString();<br>      // abcd
str.substring(2);<br>    // cd
str.substring(2,3);<br>  // c
str.contains("c");<br>   // true
str.endsWith("d");<br>   // true
str.startsWith("a");<br> // true
str.isEmpty();<br>       // false
## Immutable

String str = "hello";<br>
str.concat("world");<br>

// Outputs: hello
System.out.println(str);<br>

String str = "hello";<br>
String concat = str.concat("world");<br>

// Outputs: helloworld
System.out.println(concat);<br>
Once created cannot be modified, any modification creates a new String

## Java Arrays
Declare

int[] a1;<br>
int[] a2 = {1, 2, 3};<br>
int[] a3 = new int[]{1, 2, 3};<br>

int[] a4 = new int[3];<br>
a4[0] = 1;<br>
a4[2] = 2;<br>
a4[3] = 3;<br>
## Modify

int[] a = {1, 2, 3};<br>
System.out.println(a[0]);<br> // 1

a[0] = 9;<br>
System.out.println(a[0]);<br> // 9

System.out.println(a.length);<br> // 3
## Loop (Read & Modify)

int[] arr = {1, 2, 3};<br>
for (int i=0;<br> i < arr.length;<br> i++) {
    arr[i] = arr[i] * 2;<br>
    System.out.print(arr[i] + " ");<br>
}
// Outputs: 2 4 6
Loop (Read)

String[] arr = {"a", "b", "c"};<br>
for (int a: arr) {
    System.out.print(a + " ");<br>
}
// Outputs: a b c 
## Multidimensional Arrays

int[][] matrix = { {1, 2, 3}, {4, 5} };<br>

int x = matrix[1][0];<br>  // 4
// [[1, 2, 3], [4, 5]]
Arrays.deepToString(matrix)

for (int i = 0;<br> i < a.length;<br> ++i) {
  for(int j = 0;<br> j < a[i].length;<br> ++j) {
    System.out.println(a[i][j]);<br>
  }
}
// Outputs: 1 2 3 4 5 6 7 
## Sort

char[] chars = {'b', 'a', 'c'};<br>
Arrays.sort(chars);<br>

// [a, b, c]
Arrays.toString(chars);<br>
## Java Conditionals
Operators
+
-
*
/
%
=
++
--
!
==
!=
>
>=
<
<=
&&
||
?:
instanceof
~
<<
>>
>>>
&
^
|
If else

int k = 15;<br>
if (k > 20) {
  System.out.println(1);<br>
} else if (k > 10) {
  System.out.println(2);<br>
} else {
  System.out.println(3);<br>
}
## Switch

int month = 3;<br>
String str;<br>
switch (month) {
  case 1:
    str = "January";<br>
    break;<br>
  case 2:
    str = "February";<br>
    break;<br>
  case 3:
    str = "March";<br>
    break;<br>
  default:
    str = "Some other month";<br>
    break;<br>
}

// Outputs: Result March
System.out.println("Result " + str);<br>
## Ternary operator

int a = 10;<br>
int b = 20;<br>
int max = (a > b) ? a : b;<br>

// Outputs: 20
System.out.println(max);<br>
#Java Loops
For Loop

for (int i = 0;<br> i < 10;<br> i++) {
  System.out.print(i);<br>
}
// Outputs: 0123456789

for (int i = 0,j = 0;<br> i < 3;<br> i++,j--) {
  System.out.print(j + "|" + i + " ");<br>
}
// Outputs: 0|0 -1|1 -2|2
## Enhanced For Loop

int[] numbers = {1,2,3,4,5};<br>

for (int number: numbers) {
  System.out.print(number);<br>
}
// Outputs: 12345
Used to loop around array's or List's

While Loop

int count = 0;<br>

while (count < 5) {
  System.out.print(count);<br>
  count++;<br>
}
// Outputs: 01234
Do While Loop

int count = 0;<br>

do {
  System.out.print(count);<br>
  count++;<br>
} while (count < 5);<br>
// Outputs: 01234
Continue Statement

for (int i = 0;<br> i < 5;<br> i++) {
  if (i == 3) {
    continue;<br>
  }
  System.out.print(i);<br>
}
// Outputs: 01245
### Break Statement

for (int i = 0;<br> i < 5;<br> i++) {
  System.out.print(i);<br>
  if (i == 3) {
    break;<br>
  }
}
// Outputs: 0123
## Java Collections Framework
<br>Java Collections
<br>Collection                                                Interface	Ordered	Sorted	Thread safe	Duplicate	Nullable
<br>ArrayList	List	                                               Y	        N            	N         Y          Y
<br>Vector	List                                                   Y        	N           	Y       	Y        	Y
<br>LinkedList	List, Deque                                        Y        	N            	N        	Y          	Y
<br>CopyOnWriteArrayList	List                                     Y        	N            	Y        	Y          	Y
<br>HashSet	Set	                                                            N	N	N	N	One null
<br>LinkedHashSet	Set                                                     	Y	N	N	N	One null
<br>TreeSet	Set                                                            	Y	Y	N	N	N
<br>CopyOnWriteArraySet	Set                                                	Y	N	Y	N	One null
<br>ConcurrentSkipListSet Set	                                              Y	Y	Y	N	N
<br>HashMap	Map                                                            	N	N	N	N (key)	One null (key)
<br>HashTable	Map	                                                          N	N	Y	N (key)	N (key)
<br>LinkedHashMap	Map	                                                      Y	N	N	N (key)	One null (key)
<br>TreeMap	Map	                                                            Y	Y	N	N (key)	N (key)
<br>ConcurrentHashMap	Map                                                  	N	N	Y	N (key)	N
<br>ConcurrentSkipListMap	Map	                                              Y	Y	Y	N (key)	N
<br>ArrayDeque	Deque	                                                      Y	N	N	Y	N
<br>PriorityQueue	Queue                                                    	Y	N	N	Y	N
<br>ConcurrentLinkedQueue	Queue	                                            Y	N	Y	Y	N
<br>ConcurrentLinkedDeque	Deque                                            	Y	N	Y	Y	N
<br>ArrayBlockingQueue	Queue	                                              Y	N	Y	Y	N
<br>LinkedBlockingDeque	Deque	                                              Y	N	Y	Y	N
<br>PriorityBlockingQueue	Queue                                              	Y	N	Y	Y	N
## ArrayList

List<Integer> nums = new ArrayList<>();<br>

// Adding
nums.add(2);<br>
nums.add(5);<br>
nums.add(8);<br>

// Retrieving
System.out.println(nums.get(0));<br>

// Indexed for loop iteration
for (int i = 0;<br> i < nums.size();<br> i++) {
    System.out.println(nums.get(i));<br>
}

nums.remove(nums.size() - 1);<br>
nums.remove(0);<br> // VERY slow

for (Integer value : nums) {
    System.out.println(value);<br>
}
## HashMap

Map<Integer, String> m = new HashMap<>();<br>
m.put(5, "Five");<br>
m.put(8, "Eight");<br>
m.put(6, "Six");<br>
m.put(4, "Four");<br>
m.put(2, "Two");<br>

// Retrieving
System.out.println(m.get(6));<br>

// Lambda forEach
m.forEach((key, value) -> {
    String msg = key + ": " + value;<br>
    System.out.println(msg);<br>
});<br>
## HashSet

Set<String> set = new HashSet<>();<br>
if (set.isEmpty()) {
    System.out.println("Empty!");<br>
}

set.add("dog");<br>
set.add("cat");<br>
set.add("mouse");<br>
set.add("snake");<br>
set.add("bear");<br>

if (set.contains("cat")) {
    System.out.println("Contains cat");<br>
}

set.remove("cat");<br>
for (String element : set) {
    System.out.println(element);<br>
}
## ArrayDeque

Deque<String> a = new ArrayDeque<>();<br>

// Using add()
a.add("Dog");<br>

// Using addFirst()
a.addFirst("Cat");<br>

// Using addLast()
a.addLast("Horse");<br>

// [Cat, Dog, Horse]
System.out.println(a);<br>

// Access element
System.out.println(a.peek());<br>

// Remove element
System.out.println(a.pop());<br>
## Misc
#### Access Modifiers
Modifier	Class	Package	Subclass	World
public	Y	Y	Y	Y
protected	Y	Y	Y	N
no modifier	Y	Y	N	N
private	Y	N	N	N
## Regular expressions

String text = "I am learning Java";<br>
// Removing All Whitespace
text.replaceAll("\\s+", "");<br>

// Splitting a String
text.split("\\|");<br>
text.split(Pattern.quote("|"));<br>
See: Regex in java

## Comment

// I am a single line comment!
 
/*
And I am a 
multi-line comment!
*/

/**
 * This  
 * is  
 * documentation  
 * comment 
 */
## Keywords
<br>abstract
<br>continue
<br>for
<br>new
<br>switch
<br>assert
<br>default
<br>goto
<br>package
<br>synchronized
<br>boolean
<br>do
<br>if
<br>private
<br>this
<br>break
<br>double
<br>implements
<br>protected
<br>throw
<br>byte
<br>else
<br>import
<br>public
<br>throws
<br>case
<br>enum
<br>instanceof
<br>return
<br>transient
<br>catch
<br>extends
<br>int
<br>short
<br>try
<br>char
<br>final
<br>interface
<br>static
<br>void
<br>class
<br>finally
<br>long
<br>strictfp
<br>volatile
<br>const
<br>float
<br>native
<br>super
<br>while
## Math  methods
<br>Math .max(a,b)	Maximum of a and b
<br>Math .min(a,b)	Minimum of a and b
<br>Math .abs(a)	Absolute value a
<br>Math .sqrt(a)	Square-root of a
<br>Math .pow(a,b)	Power of b
<br>Math .round(a)	Closest integer
<br>Math .sin(ang)	Sine of ang
<br>Math .cos(ang)	Cosine of ang
<br>Math .tan(ang)	Tangent of ang
<br>Math .asin(ang)	Inverse sine of ang
<br>Math .log(a)	Natural logarithm of a
<br>Math .toDegrees(rad)	Angle rad in degrees
<br>Math .toRadians(deg)	Angle deg in radians

## Try/Catch/Finally

try {
  // something
} catch (Exception e) {
  e.printStackTrace();<br>
} finally {
  System.out.println("always printed");<br>
}
