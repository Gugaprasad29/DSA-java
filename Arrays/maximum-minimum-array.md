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
**Minimum and Maximum in array using Tournament method**
```
import java.util.*;

public class Min_Max{
    public static int[] tournament(int[] arr, int low, int high){
        int min = Integer.MAX_VALUE;
        int max = Integer.MIN_VALUE;
        int mid;
        
        if(low==high){
            min = arr[low];
            max = arr[low];
            return new int[]{min, max};
        } 
        if(high==low+1){
            min = Math.min(arr[low], arr[high]);
            max = Math.max(arr[low], arr[high]);
            return new int[]{min, max};
        }
        mid = (low+high)/2;
        int[] mml = tournament(arr, low, mid);
        int[] mmr = tournament(arr, mid+1, high);
        
        min = Math.min(mml[0],mmr[0]);
        max = Math.max(mml[1],mmr[1]);
        
        return new int[]{min,max};
    }
    public static void main(String[] args){
        int[] arr = {9,42,23,49,57,40};
        int n = arr.length;
        int[] minmax = tournament(arr, 0, n-1);
        System.out.println("Minimum value in array: " + minmax[0]);
        System.out.println("Maximum value in array: " + minmax[1]);
    }
}
```
