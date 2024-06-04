**Array reverse with extra array**
```
public class array {
    public static void revarr(int[] arr){
        int[] rarr = new int[arr.length];
        for(int i=0;i<arr.length;i++){
            rarr[i] = arr[arr.length-i-1];
        }
        System.out.print("Reverse Array: ");
        for(int i:rarr){
            System.out.print(i + " ");
        }
    }
    public static void main(String[] args) {
        int[] oarr = {1,2,3,4,5};
        revarr(oarr);
    }
}
```
**Array reverse with loop**
```
public class array {
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
        int[] oarr = {1,2,3,4,5};
        revarr(oarr);
    }
}
```
**Array reverse with in-built methods**
```
import java.util.*;

public class array{
    public static void main(String[] args){
        int[] oarr = {1,2,3,4,5};
        int[] rarr = new int[oarr.length];
        for(int i=0;i<oarr.length;i++){
            rarr[i] = oarr[oarr.length-i-1];
        }
        System.out.println(Arrays.toString(rarr));
    }
}
```
