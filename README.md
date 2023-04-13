# Second_Highest_Element_Using_Stream_API

package Com.nt.practice;

/**
 *  We first create an integer array with some values. then,
 
 *  we use the Arrays.stream() method to convert the array to a stream of integers.
 
 *  We box each element of the stream using boxed() method to convert int to Integer.
 
 *  Next ,we sort the stream in descending order using the sorted() method and Comparator interface.
 
 *  we then use distinct() method to remove duplicate from stream.
 
 *  we then skip the first element using skip(1) to get the second highest element.
 
 *  finally, we use the findFirst() method to get the first elelemnt of the stream and convert it to int using orElse() method.
 
 */
 
import java.util.Arrays;

public class SecondHighestElementUsingStringAPI {

	public static void main(String[] args) {
  
		int arr[] = { 5, 12, 36, 3, 1, 18, 45, 9 };
		int secondHighestElement = Arrays.stream(arr).boxed().sorted((a, b) -> b.compareTo(a)).distinct().skip(1)
				.findFirst().orElse(0);
        
		System.out.println("Second Highest Element In The Array->" + secondHighestElement);
	}

}

Output:- Second Highest Element In The Array->36

