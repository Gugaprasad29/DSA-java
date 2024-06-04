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
**Array reverse with loop**
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
**Array reverse with in-built methods**
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
