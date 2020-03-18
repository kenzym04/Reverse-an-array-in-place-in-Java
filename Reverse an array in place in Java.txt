/**
 * Program to reverse an array in place in Java.
 * Works both when array size is odd and even :)
 * @author: Kennedy
*/
import java.util.Arrays;
public class reverseArrayInPlace
{
    public static int [] arr;
     public static int a =0;
      public static int b = 0;
      //method to swap two values
    public static void swap(int[] arr,int a,int b)
    {
    //swap two values a & b
    int temp=arr[a];
    arr[a]=arr[b];
    arr[b]=temp;
    }
    //method to reverse array values
        public static int[] reverseArray(int[] arr)
        {
                //decrement the array size
            int size=arr.length-1;
            /**As long as current first index is less than array size swap current index with current last index
            */
                for(int i=0;i<size;i++)
                {
                swap(arr,i,size--);
                
                }
        
            return arr;
        }
            
                     public static void main(String []args)
                     {
                         
                         //create array
                         int [] arr = {3,5,7,9,11,13,15,17,19};
                         //print original array
                         System.out.println("Original Array:" + " " + Arrays.toString(arr));
                         //call reverse method
                         reverseArray(arr);
                         //print reversed array
                        System.out.println("Reversed Array:" + " " + Arrays.toString(arr));
                     }
}

OUTPUT:

$javac reverseArrayInPlace.java
$java -Xmx128M -Xms16M reverseArrayInPlace
Original Array: [3, 5, 7, 9, 11, 13, 15, 17, 19]
Reversed Array: [19, 17, 15, 13, 11, 9, 7, 5, 3]