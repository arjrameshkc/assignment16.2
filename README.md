# assignment16.2


package udf;

import java.util.Scanner;

import org.apache.hadoop.hive.ql.exec.UDF;


public class ToConcat extends UDF
{
	

   public static void main(String args[])
   {
      String str1, str2;
      Scanner scan = new Scanner(System.in);
 
      System.out.print("Enter First String : ");
      str1 = scan.nextLine();
      System.out.print("Enter Second String : ");
      str2 = scan.nextLine();
      
      System.out.print("Concatenating String 2 into String 1...\n");
      str1 = str1.concat(str2);
	  
      System.out.print("String 1 after Concatenation is " +str1);
   }
}

-------------------------------------------------------

ADD JAR /home/acadgild/hive/hivetocon-udf.jar;


CREATE TEMPORARY FUNCTION  AS 'udf.Toconcat';
