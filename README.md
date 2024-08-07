# Finding-Minimum-Number-of-Houses-to-feed-All-Rats
The function accepts two positive integers 'r' and 'unit' and a positive integer array 'arr' of size 'n' as its argument 'r' represents the number of rats present in an area, 'unit' is the amount of food each rat consumes and each ith element of array 'arr' represents the amount of food present in 'i+1' house number, where 0 &lt;= i
package javaproject;
import java.util.*;
public class ArrayPractice1{ 
	public static int solve (int r, int unit, int arr[], int n)  {  
		if (n == 0)     
			return -1;   
		int res = r * unit;    
		int sum = 0,i;   
		int count = 0;    
		for ( i = 0; i < n; i++)    
		{
			sum = sum + arr[i];
			count++;
		if (sum >= res) 
			break;   
		}    
		if (sum < res)   
			return 0;  
		return i+1; 
		} 
	public static void main (String[]args)  { 
		Scanner sc = new Scanner (System.in); 
		System.out.println("r:");
		int r = sc.nextInt ();
		System.out.println("unit: ");
		int unit = sc.nextInt ();
		System.out.println("n:");
		int n = sc.nextInt ();  
		int arr[] = new int[n]; 
		System.out.println("arr:");
		for (int i = 0; i < n; i++)  
			arr[i] = sc.nextInt ();   
		System.out.println (solve (r, unit, arr, n));
		}
	}
