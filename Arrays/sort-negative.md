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
