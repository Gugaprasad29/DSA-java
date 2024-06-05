**Partition process**
```
public class Main {
    public static void main(String[] args) {
        int[] arr = {0,2,7,-6,8,-4,3,5,-1};
        int n = arr.length;
        partition(arr, n);
        for (int i = 0; i < n; i++)
            System.out.print(arr[i] + " ");
    }
    public static void partition(int[] arr, int n){
        int j=0;
        for(int i=0;i<n;i++){
            if(arr[i]<0){
                if(i != j){
                    int temp = arr[i];
                    arr[i] = arr[j];
                    arr[j] = temp;
                }
                j++;
            }
        }
    }
}
```
**Two pointer approach**
```
public class Main {
    public static void main(String[] args) {
        int[] arr = {0,2,7,-6,8,-4,3,5,-1};
        int n = arr.length;
        two_pointer(arr, 0, n-1);
        for (int i=0;i<=n-1;i++)
            System.out.print(arr[i] + " ");
    }
    public static void two_pointer(int[] arr, int left, int right){
        while(left<right){
            if(arr[left]<0 && arr[right]<0)
                left++;
            else if(arr[left]>=0 && arr[right]<0){
                int temp = arr[left];
                arr[left] = arr[right];
                arr[right] = temp;
                left++;
                right--;
            }
            else if (arr[left]>=0 && arr[right]>=0)
                right--;
        }
    }
}
```
**Dutch Flag algorithm**
```
public class Main {
    public static void main(String[] args) {
        int[] arr = {9,2,7,-6,8,-4,3,5,-1};
        dutch_flag(arr);
        for (int i:arr)
            System.out.print(i + " ");
    }
    public static void dutch_flag(int[] arr){
       int low = 0;
       int high = arr.length-1;
       while(low<=high){
           if(arr[low]<=0)
                low++;
            else
                swap(arr, low, high--);
        }
    }
    public static void swap(int[] arr, int i, int j){
        int temp = arr[i];
        arr[i] = arr[j];
        arr[j] = temp;
    }
}
```
