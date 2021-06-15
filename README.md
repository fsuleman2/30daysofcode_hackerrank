# Solutions for the Hacker Rank 30 DAYS OF CODE
[Check out my Hacker Rank Profile](https://www.hackerrank.com/fsuleman2)

[Day 0: Hello, World.](https://www.hackerrank.com/challenges/30-hello-world/problem)

```c++
int main() {
    // Declare a variable named 'input_string' to hold our input.
    string input_string; 
    
    // Read a full line of input from stdin (cin) and save it to our variable, input_string.
    getline(cin, input_string); 
    
    // Print a string literal saying "Hello, World." to stdout using cout.
    cout << "Hello, World." << endl;

    // TODO: Write a line of code here that prints the contents of input_string to stdout.
    cout<<input_string;
    return 0;
}
```
[Day 1: Data Types](https://www.hackerrank.com/challenges/30-data-types/problem)

```java
import java.io.*;
import java.util.*;
import java.text.*;
import java.math.*;
import java.util.regex.*;

public class Solution {
	
    public static void main(String[] args) {
        int i = 4;
        double d = 4.0;
        String s = "HackerRank ";
		
        Scanner scan = new Scanner(System.in);

        /* Declare second integer, double, and String variables. */
        int j;
        double dbl;
        String str;

        /* Read and save an integer, double, and String to your variables.*/
        // Note: If you have trouble reading the entire String, please go back and review the Tutorial closely.
        Scanner sc = new Scanner(System.in).useDelimiter("\\n");
        j=sc.nextInt();
        dbl=sc.nextDouble();
        str=sc.next();
        
        /* Print the sum of both integer variables on a new line. */
            System.out.println(i+j);
        /* Print the sum of the double variables on a new line. */
		      System.out.println(d+dbl);
        /* Concatenate and print the String variables on a new line; 
        	the 's' variable above should be printed first. */
            System.out.println(s+str);

        scan.close();
```
[Day 2: Operators](https://www.hackerrank.com/challenges/30-operators/problem)

```java
import java.io.*;
import java.math.*;
import java.security.*;
import java.text.*;
import java.util.*;
import java.util.concurrent.*;
import java.util.function.*;
import java.util.regex.*;
import java.util.stream.*;
import static java.util.stream.Collectors.joining;
import static java.util.stream.Collectors.toList;

class Result {

    /*
     * Complete the 'solve' function below.
     *
     * The function accepts following parameters:
     *  1. DOUBLE meal_cost
     *  2. INTEGER tip_percent
     *  3. INTEGER tax_percent
     */

    public static void solve(double meal_cost, int tip_percent, int tax_percent) {
    // Write your code here
        double tip  = (meal_cost/100)*tip_percent;
        // System.out.println(tip);
        // double tax = (8/100)*12;
        double tax = (double)tax_percent/100*meal_cost;
        // System.out.println(tax);
        double total_cost = meal_cost+tip+tax;
        System.out.println(Math.round(total_cost));
    }

}

public class Solution {
    public static void main(String[] args) throws IOException {
        BufferedReader bufferedReader = new BufferedReader(new InputStreamReader(System.in));

        double meal_cost = Double.parseDouble(bufferedReader.readLine().trim());

        int tip_percent = Integer.parseInt(bufferedReader.readLine().trim());

        int tax_percent = Integer.parseInt(bufferedReader.readLine().trim());

        Result.solve(meal_cost, tip_percent, tax_percent);

        bufferedReader.close();
    }
}

```
[Day 3: Intro to Conditional Statements](https://www.hackerrank.com/challenges/30-conditional-statements/problem)

```python
#!/bin/python3

import math
import os
import random
import re
import sys



if __name__ == '__main__':
    N = int(input().strip())
    n=N
    if n%2==0 and n in range(2,5):
        print("Not Weird")
    elif n%2==0 and n>20:
        print("Not Weird")
    else:
        print("Weird")

```
[Day 4: Class vs. Instance](https://www.hackerrank.com/challenges/30-class-vs-instance/problem)

```java


public class Person {
    private int age;	
  
	public Person(int initialAge) {
  		// Add some more code to run some checks on initialAge
          this.age=initialAge;
          if(age<0)
          {
              System.out.println("Age is not valid, setting age to 0.");
            age=0;
          }
	}

	public void amIOld() {
  		// Write code determining if this person's age is old and print the correct statement:
         if(this.age<13){
             System.out.println("You are young.");
         }
         else if(this.age>=13 && this.age<18){
             System.out.println("You are a teenager.");
         }
         else{
        System.out.println("You are old."/*Insert correct print statement here*/);
         }
	}

	public void yearPasses() {
  		// Increment this person's age.
          this.age+=1;
	}
```
[Day 5: Loops](https://www.hackerrank.com/challenges/30-loops/problem)

```java
import java.io.*;
import java.math.*;
import java.security.*;
import java.text.*;
import java.util.*;
import java.util.concurrent.*;
import java.util.regex.*;



public class Solution {
    public static void main(String[] args) throws IOException {
        BufferedReader bufferedReader = new BufferedReader(new InputStreamReader(System.in));

        int n = Integer.parseInt(bufferedReader.readLine().trim());
        int count=1;
        for(int i=1;i<=10;i++)
        {
            System.out.println(n+" "+"x"+" "+i+" "+"="+" "+(n*i));
        }
            
        bufferedReader.close();
    }
}
```
[Day 6: Let's Review](https://www.hackerrank.com/challenges/30-review-loop/problem)

```java
import java.io.*;
import java.util.*;
import java.text.*;
import java.math.*;
import java.util.regex.*;

public class Solution {

    public static void main(String[] args) {
        /* Enter your code here. Read input from STDIN. Print output to STDOUT. Your class should be named Solution. */
    Scanner sc = new Scanner(System.in);
    int n = sc.nextInt();
    String res1="",res2="";
    for(int i = 0;i<n;i++)
    {
        String str = sc.next();
        char[] chr1 = str.toCharArray();
        for(int j=0;j<str.length();j++)
        {
            if(j%2==0)
            {
                res1=res1+chr1[j];
            }
            else{
                res2=res2+chr1[j];
            }
            
        }
         System.out.println(res1+" "+res2);
         res1="";
        res2="";
    }
    // System.out.println(res1+" "+res2);
    }
}
```
[Day 7: Arrays](https://www.hackerrank.com/challenges/30-arrays/problem)

```java
import java.io.*;
import java.math.*;
import java.security.*;
import java.text.*;
import java.util.*;
import java.util.concurrent.*;
import java.util.regex.*;



public class Solution {
    public static void main(String[] args) throws IOException {
        BufferedReader bufferedReader = new BufferedReader(new InputStreamReader(System.in));

        int n = Integer.parseInt(bufferedReader.readLine().trim());

        String[] arrTemp = bufferedReader.readLine().replaceAll("\\s+$", "").split(" ");

        List<Integer> arr = new ArrayList<>();

        for (int i = 0; i < n; i++) {
            int arrItem = Integer.parseInt(arrTemp[i]);
            arr.add(arrItem);
        }
        for(int i=n-1;i>=0;i--)
        {
            int arrItem = Integer.parseInt(arrTemp[i]);
            System.out.print(arrItem+" ");
        }
        bufferedReader.close();
    }
}
```
[Day 8: Dictionaries and Maps](https://www.hackerrank.com/challenges/30-dictionaries-and-maps/problem)

```python
# Enter your code here. Read input from STDIN. Print output to STDOUT
n = int(input())
# accepting input, splitting by space and adding into the list using list compre
mylist=[input().split(' ') for i in range(n)]
# input accepted successfully. After that converting that list data into a dict
phone_book = {k:v for k,v in mylist}
# checking the above given condn
while True:
    try:
        name = input()
        if name in phone_book:
            print('%s=%s'%(name,phone_book[name]))
        else:
            print("Not found")
    except:
        break
```
```java
//Same solution in java
//Complete this code or write your own from scratch
import java.util.*;
import java.io.*;

class Solution{
    public static void main(String []argh){
        Scanner in = new Scanner(System.in);
        Map<String,Integer> myMap = new HashMap<String,Integer>();
           
        int n = in.nextInt();
        boolean flag = false;
        for(int i = 0; i < n; i++){
            String name = in.next();
            int phone = in.nextInt();
            // Write code here
            myMap.put(name,phone);
        }
        while(in.hasNext()){
            String s = in.next();
            // Write code here
            if(myMap.containsKey(s) == flag){
                System.out.println("Not found");
            }
            else{
                System.out.println(s+"="+myMap.get(s));
            }
            
        }
        in.close();
    }
}
```
[Day 9: Recursion 3](https://www.hackerrank.com/challenges/30-recursion/problem)

```python
#!/bin/python3

import math
import os
import random
import re
import sys

#
# Complete the 'factorial' function below.
#
# The function is expected to return an INTEGER.
# The function accepts INTEGER n as parameter.
#

def factorial(n):
    # Write your code here
    if n==0:
        return 1
    else:
        return n*factorial(n-1)
if __name__ == '__main__':
    fptr = open(os.environ['OUTPUT_PATH'], 'w')

    n = int(input().strip())

    result = factorial(n)

    fptr.write(str(result) + '\n')

    fptr.close()
```
[Day 10: Binary Numbers](https://www.hackerrank.com/challenges/30-binary-numbers/problem)

```java
import java.io.*;
import java.math.*;
import java.security.*;
import java.text.*;
import java.util.*;
import java.util.concurrent.*;
import java.util.function.*;
import java.util.regex.*;
import java.util.stream.*;
import static java.util.stream.Collectors.joining;
import static java.util.stream.Collectors.toList;



public class Solution {
    public static void main(String[] args) throws IOException {
        BufferedReader bufferedReader = new BufferedReader(new InputStreamReader(System.in));

        int n = Integer.parseInt(bufferedReader.readLine().trim());
        //  int n = in.nextInt();
    int rem=0,s=0,t=0;


    while(n>0)
        {
        rem=n%2;
        n=n/2;
        if(rem==1)
         {   s++;
           if(s>=t)

            t=s;

        }
        else{

            s=0;
        }   
    }

    System.out.println(t);
        bufferedReader.close();
    }
}
```
[Day 11: 2D Arrays](https://www.hackerrank.com/challenges/30-2d-arrays/problem)

```python
#!/bin/python3

import math
import os
import random
import re
import sys

if __name__ == '__main__':

    arr = []

    for _ in range(6):
        arr.append(list(map(int, input().rstrip().split())))

    rows=len(arr)
    cols=len(arr[0])
    max_hour_glass = -63;
    for i in range(rows-2):
        for j in range(cols-2):
            current_hour_glass = arr[i][j]+arr[i][j+1]+arr[i][j+2]+arr[i+1][j+1]+arr[i+2][j]+arr[i+2][j+1]+arr[i+2][j+2]
            max_hour_glass = max(max_hour_glass,current_hour_glass)
    print(max_hour_glass)

```
