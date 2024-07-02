**Array reverse with extra array**
```
public class Reverse_array {
    public static void revarr(int[] arr){
        int[] rev_arr = new int[arr.length];
        for(int i=0;i<arr.length;i++){
            rev_arr[i] = arr[arr.length-i-1];
        }
        System.out.print("Reverse Array: ");
        for(int i:rev_arr){
            System.out.print(i + " ");
        }
    }
    public static void main(String[] args) {
        int[] org_arr = {1,2,3,4,5};
        revarr(org_arr);
    }
}
```
**Array reverse with Loops**
```
public class Reverse_array {
    public static void revarr(int[] arr){
        int temp, start=0, end=4;
        while(start<end){
            temp = arr[start];
            arr[start] = arr[end];
            arr[end] = temp;
            start++;
            end--;
        }
        System.out.print("Reverse Array: ");
        for(int i=0;i<5;i++){
            System.out.print(arr[i] + " ");
        }
    }
    public static void main(String[] args) {
        int[] org_arr = {1,2,3,4,5};
        revarr(org_arr);
    }
}
```
**Array reverse with In-built methods**
```
import java.util.*;

public class Reverse_array{
    public static void main(String[] args){
        int[] org_arr = {1,2,3,4,5};
        int[] rev_arr = new int[org_arr.length];
        for(int i=0;i<org_arr.length;i++){
            rarr[i] = org_arr[org_arr.length-i-1];
        }
        System.out.println(Arrays.toString(rev_arr));
    }
}
```
**Array reverse with Recursion**
```
public class array{
    public static void revarr(int[] arr, int start, int end){
        int temp;
        if(start>=end)
            return;
        else
            temp = arr[start];
            arr[start] = arr[end];
            arr[end] = temp;
            revarr(arr, start+1, end-1);
        System.out.print("Reverse array: ");
        for(int i=0;i<5;i++)
            System.out.print(arr[i] + " ");
    }
    public static void main(String[] args){
       int[] org_arr = {1,2,3,4,5};
       revarr(org_arr, 0, 4);
    }
}
```
**Array reverse with Stack**
```
import java.util.Stack;

public class array{
    public static void revarr(int[] arr){
        Stack<Integer> stack = new Stack<>();
        for(int i:arr)
            stack.push(i);
        for(int i=0;i<arr.length;i++)
            arr[i] = stack.pop();
    }
    public static void main(String[] args){
        int[] arr = {1,2,3,4,5};
        revarr(arr);
        System.out.print("Reverse array: ");
        for(int i:arr)
            System.out.print(i + " ");
    }
}
```
** Reverse Sub Array**
```
class Solution {
    void reverseSubArray(int arr[], int n, int l, int r) {
        int i = l-1;
        int j = r-1;
        while(i<=j){
            int temp = arr[i];
            arr[i] = arr[j];
            arr[j] = temp;
            i++;
            j--;
        }
    }
}
```
