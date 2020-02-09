https://linuxize.com/post/install-java-on-ubuntu-18-04/  install 
Java Fundamentals

History of java



Features of java 

    • robust easy to debug
    • oops
    • multithreading
    • exception handling mechanism
    • streams
    • Java does not require any preprocessor: It does not require inclusion of header files for creating a Java application.
      
working principles of java
    • jdk sw set of packages 
    • jvm Java Virtual Machine 
      installation happens during installation of os
    1. Class Loader :responsible for loading class from sec to main memory
    2. byte code verifier :all the lines of code are converted to byte  
       i.e high level language to byte code
       
    3. just in time compiler byte code can be converted to native code i.e machine code that’s why we say java is not a compiler only but a interpreter
    • jre
javac compiled
java executable architectural neutral

java is a platform independent because all our code is executed in run time environmemnt.

 The programs written in Java language, after compilation, are converted into an intermediate level language called the bytecode which is a part of the Java platform irrespective of the machine on which the programs run. This makes java highly portable as its bytecodes can be run on any machine by an interpreter called the Java Virtual Machine(JVM) and thus java provides ‘reusability of code’.

public static void main(String args[])
call main method witout creating object so use static


system.out.println()
class.staticvariable.method
in/out static variable

Data types :
    1. primitive    
       byte 
       short
       int
       long
       double
float
       boolean
       char
    2. reference
       Array,strings,objects
       control structures
       simple if,if else,nested if,if else ladder
       switch
       Iterative statment
       while do,do ..while
       do and for are entry level loop
       do .. while exit level loop:  Menu Driven
       enhanced for: for each
Downloading of STS 4.0

https://spring.io/tools
select Download STS4
LINUX64 BIT
It will download the tar/zip file 
extract

new file 
meaven
mavenarchi quick start
group id project name

java build path   configure build path
 add libraries     jre system library

click installed jre
remove  
Scanner Class in Java
Scanner is a class in java.util package used for obtaining the input of the primitive types like int, double, etc. and strings.

To create an object of Scanner class, we usually pass the predefined object System.in, which represents the standard input stream. We may pass an object of class File if we want to read input from a file.
    • To read numerical values of a certain data type XYZ, the function to use is nextXYZ(). For example, to read a value of type short, we can use nextShort()
    • To read strings, we use nextLine().
    • To read a single character, we use next().charAt(0).
    •  next() function returns the next token/word in the input as a string and charAt(0) function returns the first character in that string.
      Scanner sc = new Scanner(System.in); 
  
        // String input 
        String name = sc.nextLine(); 
  
        // Character input 
        char gender = sc.next().charAt(0); 
  
        // Numerical data input 
        // byte, short and float can be read 
        // using similar-named functions. 
        int age = sc.nextInt(); 
        long mobileNo = sc.nextLong(); 
        double cgpa = sc.nextDouble(); 


Arrays in Java

An array is a group of like-typed variables that are referred to by a common name.Arrays in Java work differently than they do in C/C++. Following are some important point about Java arrays.
    • In Java all arrays are dynamically allocated.(discussed below)
    • Since arrays are objects in Java, we can find their length using member length. This is different from C/C++ where we find length using sizeof.
    • A Java array variable can also be declared like other variables with [] after the data type.
    • The variables in the array are ordered and each have an index beginning from 0.
    • Java array can be also be used as a static field, a local variable or a method parameter.
    • The size of an array must be specified by an int value and not long or short.
    • The direct superclass of an array type is Object.
    • Every array type implements the interfaces Cloneable and java.io.Serializable.

Array can contains primitives data types as well as objects of a class depending on the definition of array. In case of primitives data types, the actual values are stored in contiguous memory locations. In case of objects of a class, the actual objects are stored in heap segment.

type var-name[];
OR
type[] var-name;






Instantiating an Array in Java

When an array is declared, only a reference of array is created. To actually create or give memory to array, you create an array like this:The general form of new as it applies to one-dimensional arrays appears as follows:
var-name = new type [size];
int intArray[];    //declaring array
intArray = new int[20];  // allocating memory to array
OR
int[] intArray = new int[20]; // combining both statements in one


Array Literal
In a situation, where the size of the array and variables of array are already known, array literals can be used.
 int[] intArray = new int[]{ 1,2,3,4,5,6,7,8,9,10 }; 
 // Declaring array literal
    • The length of this array determines the length of the created array.
    • There is no need to write the new int[] part in the latest versions of Java

int[][] intArray = new int[10][20]; //a 2D array or matrix
int[][][] intArray = new int[10][20][10]; //a 3D array


                                       





                      Strings
charArray
a group of characters

It is a class not a primitive datatype. 

ToCharArray() : into character Arrays

getBytes : in form of Byte Arrays

String is immutable //cannot make changes

In order to make String mutable
    1. String Buffer : All the methods in this class are synchronized
       use in multithreading
    2. String Builder:All the methods in this class are unsynchronized hence used in Single threaded application
String object is created
Two objects will be created

<String_Type> <string_variable> = “<sequence_of_string>”;
Example:
String str = "Geeks";
Memory allotment of String
Whenever a String Object is created, two objects will be created- one in the Heap Area and one in the String constant pool and the String object reference always points to heap area object


String name="Roshni";//String literal memory wise advisable

String name1=new String("Stack route");//String object



StringBuffer: StringBuffer is a peer class of String that provides much of the functionality of strings. String represents fixed-length, immutable character sequences while StringBuffer represents growable and writable character sequences.
      Syntax:
      StringBuffer s = new StringBuffer("GeeksforGeeks");
      
package Strings;

public class stringBuffer {
	public static void main(String [] args) {
		StringBuffer sb=new StringBuffer("Stack");
		sb.append("Route");
		System.out.println(sb);
		System.out.println(sb.insert(2, "nht"));
		System.out.println(sb.deleteCharAt(0));
		System.out.println(sb.reverse());
		
		
	}

      }
    • StringBuilder: The StringBuilder in Java represents a mutable sequence of characters. Since the String Class in Java creates and immutable sequence of characters, the StringBuilder class provides an alternate to String Class, as it creates a mutable sequence of characters.
      Syntax:
      StringBuilder str = new StringBuilder();
      str.append("GFG");


















StringTokenizer: StringTokenizer class in Java is used to break a string into tokens.

A StringTokenizer object internally maintains a current position within the string to be tokenized. Some operations advance this current position past the characters processed.
A token is returned by taking a substring of the string that was used to create the StringTokenizer object.






String Poem=”sam sam iu ndf”;
String[] st=poem.split(“ “);
//
for(String x: st)
{ 
sout(x);
}
StringTokenizer st=new StringTokenizer(poem,”  “);
while(strn.hasMoreTokens()){
Sout(strn.nextToken());
}


       
                
      

 String st=sc.nextLine();

String Methods
    1. int length(): Returns the number of characters in the String.
       "GeeksforGeeks".length();  // returns 13
    2. Char charAt(int i): Returns the character at ith index.
       "GeeksforGeeks".charAt(3); // returns  ‘k’
    3. String substring (int i): Return the substring from the ith  index character to end.
       "GeeksforGeeks".substring(3); // returns “ksforGeeks”
    4. String substring (int i, int j): Returns the substring from i to j-1 index.
        "GeeksforGeeks".substring(2, 5); // returns “eks”
    5. String concat( String str): Concatenates specified string to the end of this string.
        String s1 = ”Geeks”;
        String s2 = ”forGeeks”;
        String output = s1.concat(s2); // returns “GeeksforGeeks”

int indexOf (String s): Returns the index within the string of the first occurrence of the specified string.
        String s = ”Learn Share Learn”;
        int output = s.indexOf(“Share”); // returns 6
    1. int indexOf (String s, int i): Returns the index within the string of the first occurrence of the specified string, starting at the specified index.
        String s = ”Learn Share Learn”;
        int output = s.indexOf("ea",3);// returns 13
    2. Int lastIndexOf( String s): Returns the index within the string of the last occurrence of the specified string.
        String s = ”Learn Share Learn”;
        int output = s.lastIndexOf("a"); // returns 14
    3. boolean equals( Object otherObj): Compares this string to the specified object.
        Boolean out = “Geeks”.equals(“Geeks”); // returns true
        Boolean out = “Geeks”.equals(“geeks”); // returns false
    4. boolean  equalsIgnoreCase (String anotherString): Compares string to another string, ignoring case considerations.
        Boolean out= “Geeks”.equalsIgnoreCase(“Geeks”); // returns true
        Boolean out = “Geeks”.equalsIgnoreCase(“geeks”); // returns true
 int compareTo( String anotherString): Compares two string lexicographically.
        int out = s1.compareTo(s2);  // where s1 ans s2 are
                                    // strings to be compared
       
        This returns difference s1-s2. If :
        out < 0  // s1 comes before s2
        out = 0  // s1 and s2 are equal.
        out > 0   // s1 comes after s2.
    1. int compareToIgnoreCase( String anotherString): Compares two string lexicographically, ignoring case considerations.
        int out = s1.compareToIgnoreCase(s2);  
       // where s1 ans s2 are 
       // strings to be compared
       
        This returns difference s1-s2. If :
        out < 0  // s1 comes before s2
        out = 0   // s1 and s2 are equal.
        out > 0   // s1 comes after s2.
       Note- In this case, it will not consider case of a letter (it will ignore whether it is uppercase or lowercase).
String toLowerCase(): Converts all the characters in the String to lower case.
       String word1 = “HeLLo”;
       String word3 = word1.toLowerCase(); // returns “hello"
    1. String toUpperCase(): Converts all the characters in the String to upper case.
       String word1 = “HeLLo”;
       String word2 = word1.toUpperCase(); // returns “HELLO”
    2. String trim(): Returns the copy of the String, by removing whitespaces at both ends. It does not affect whitespaces in the middle.
       String word1 = “ Learn Share Learn “;
       String word2 = word1.trim(); // returns “Learn Share Learn”
    3.  String replace (char oldChar, char newChar): Returns new string by replacing all occurrences of oldChar with newChar.
       String s1 = “feeksforfeeks“;
       String s2 = “feeksforfeeks”.replace(‘f’ ,’g’); // returns “geeksgorgeeks”
       Note:- s1 is still feeksforfeeks and s2 is geeksgorgeeks
Math pow() method in Java with Example

The java.lang.Math.pow() is used to calculate a number raise to the power of some other number. This function accepts two parameters and returns the value of first parameter raised to the second parameter. There are some special cases as listed below:
    • If the second parameter is positive or negative zero then the result will be 1.0.
    • If the second parameter is 1.0 then the result will be same as that of the first parameter.
    • If the second parameter is NaN then the result will also be NaN.
Syntax:
public static double pow(double a, double b)
Parameter:
a : this parameter is the base
b : this parameter is the exponent.
Return :
This method returns ab.
