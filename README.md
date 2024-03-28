Toggle each character in a String
In this java program we’re going to make a program to toggle each character in a String , First we will take String input from user  . 

If the letter is in uppercase we will convert it to lowercase and if it is in uppercase we will convert it to lowercase.

 

 

length of string without using strlen
Algorithm
Take String input from user and store in the variable “s” (in this case)
Take another String variable s1 (in this case)
Take a for loop i start from i=0 to i<s.length
Take if part get one by one character from String using charAt() method and and check whether is it upper case using isUpperCase() and change upper case character to lower case and store it in s
In else part change the variable from lower case to upper case and store it in s variable
Code in Java
Run
import java.util.Scanner;

public class Main {

	public static void main(String[] args) {
	 String s = "PrePInsTa";
	 String s1 = "";
	 for (int i = 0; i < s.length(); i++) {
		if(Character.isUpperCase(s.charAt(i))) 
			 s1=s1+Character.toLowerCase(s.charAt(i));
		else 
			 s1=s1+Character.toUpperCase(s.charAt(i));
	}
	System.out.println("Toggle String is : "+s1);
	 
  }
	
}
Output
Enter a String : PrePInsTa
Toggle String is : pREpiNStA
Method 2
The Logic is same here we are using the ASCII value

Initialize the variables.
Initiate a for loop.
Toggle each character.
Terminate the loop.
Print toggled string.
Run
public class Main {

 public static void main(String[] args) {
    String str1 = "PrepInsta";
     char str[] = str1.toCharArray();

 for (int i = 0; i < str1.length(); i++) { if (str[i] >= 'A' && str[i] <= 'Z') str[i] = (char)(str[i] + 'a' - 'A'); else if (str[i] >= 'a' && str[i] <= 'z')
str[i]= (char)(str[i] + 'A' - 'a');
   }
System.out.println("Toggled string: ");
for (int i = 0; i < str1.length(); i++) {
 System.out.print(str[i]);
     }
  }
}
Toggled string: 
pREPiNSTA
Method 3
This program is the same as above, but this time we are using the While Loop.

Run
 public class Main {

    public static void main(String[] args) {

        String str1 = "PrepInsta";
        char str[] = str1.toCharArray();
        int i = 0;

        while (i < str1.length()) {
            if (str[i] >= 'a' && str[i] <= 'z') {               
           str[i] = (char)(str[i] + 'A' - 'a');           
 } 
else if (str[i] >= 'A' && str[i] <= 'Z') {
                str[i] = (char)(str[i] + 'a' - 'A');
            }
            i++;
        }

        System.out.println("Toggled string: ");
        for (i = 0; i < str1.length(); i++) {
            System.out.print(str[i]);
        }
    }
}
Output
Toggled string: 
pREPiNSTA
