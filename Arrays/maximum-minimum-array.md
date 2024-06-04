**Minimum and Maximum in array using functions**
```
import java.util.Arrays;

public class Min_Max{
    public static int min(int[] arr, int n){
        int mini = Integer.MAX_VALUE;
        for(int i=0;i<n;i++){
            if(arr[i]<mini)
                mini = arr[i];
        }
        return mini;
    }
    public static int max(int[] arr, int n){
        int maxi = Integer.MIN_VALUE;
        for(int i=0;i<n;i++){
            if(arr[i]>maxi)
                maxi = arr[i];
        }
        return maxi;
    }
    public static void main(String[] args){
        int[] arr = {9,42,23,49,57,40};
        int n = arr.length;
        System.out.println("Maximum value in array: " + max(arr,n));
        System.out.println("Minimum value in array: " + min(arr,n));
    }
}
```
**Minimum and Maximum in array using Sort**
```
import java.util.*;

public class Min_Max{
    public static void main(String[] args){
        int[] arr = {9,42,23,49,57,40};
        int n = arr.length;
        Arrays.sort(arr);
        System.out.println("Maximum value in array: " + arr[0]);
        System.out.println("Minimum value in array: " + arr[n-1]);
    }
}
```
**Minimum and Maximum in array using Linear search**
```
import java.util.*;

public class Min_Max{
    public static void min_max_arr(int[] arr, int n){
        int min, max;
        if(n==1){
            System.out.println("Minimum value in array: " + arr[0]);
            System.out.println("Maximum value in array: " + arr[0]);
            return;
        }
        if(arr[0]>arr[1]){
            max=arr[0];
            min=arr[1];
        }
        else{
            max=arr[1];
            min=arr[0];
        }
        for(int i=2;i<n;i++){
            if(arr[i]>max)
                max=arr[i];
            else if(arr[i]<min)
                min=arr[i];
        }
        System.out.println("Maximum value in array: " + max);
        System.out.println("Minimum value in array: " + min);    
    }
    public static void main(String[] args){
        int[] arr = {9,42,23,49,57,40};
        int n = arr.length;
        min_max_arr(arr,n);
    }
}
```
