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
