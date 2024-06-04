**Bubble Sort**
```
public class Main{
    public static void main(String[] args){
        int[] arr = {9,2,7,6,8,4,3,5,1};
        bubblesort(arr);
        for(int i: arr){
            System.out.print(i + " ");
        }
    }
    public static void bubblesort(int[] arr){
        for(int i=0;i<arr.length-1;i++){
            for(int j=0;j<arr.length-i-1;j++){
                if(arr[j]>arr[j+1]){
                    int temp = arr[j];
                    arr[j] = arr[j+1];
                    arr[j+1] = temp;
                }
            }
        }
    }
}
```
**Insertion Sort**
```
public class Main{
    public static void main(String[] args){
        int[] arr = {9,2,7,6,8,4,3,5,1};
        insertionSort(arr);
        for(int i: arr){
            System.out.print(i + " ");
        }
    }
    public static void insertionSort(int[] arr){
        for(int i=1;i<arr.length;i++){
                int temp = arr[i];
                int j = i-1;
                while(j>=0 && arr[j]>temp){
                arr[j+1] = arr[j];
                j--;
            }
            arr[j+1] = temp;    
        }
    }
}
```
