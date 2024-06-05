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
**Selection Sort**
```
public class Main{
    public static void main(String[] args){
        int[] arr = {9,2,7,6,8,4,3,5,1};
        selectionSort(arr);
        for(int i: arr){
            System.out.print(i + " ");
        }
    }
    public static void selectionSort(int[] arr){
        for(int i=0;i<arr.length-1;i++){
            int min = i;
            for(int j=i+1;j<arr.length;j++){
                if(arr[min]>arr[j])
                    min = j;
            }
        int temp = arr[i];
        arr[i] = arr[min];
        arr[min] = temp;
        }    
    }
}
```
**Merge Sort**
```
public class Main {
    public static void main(String[] args) {
        int[] arr = {9,2,7,6,8,4,3,5,1};
        mergeSort(arr);
        for(int i=0;i<arr.length;i++)
            System.out.print(arr[i] + " ");
    }
    public static void mergeSort(int[] arr){
        int n = arr.length;
        if(n<=1)
            return;
        int mid = n/2;
        int[] leftArray = new int[mid];
        int[] rightArray = new int[n-mid];
        int j=0;
        for(int i=0;i<arr.length;i++){
            if(i<mid){
                leftArray[i] = arr[i];
            }
            else{
                rightArray[j] = arr[i];
                j++;
            }
        }
        mergeSort(leftArray);
        mergeSort(rightArray);
        merge(leftArray, rightArray, arr);
    }
    public static void merge(int[] leftArray, int[] rightArray, int[] arr){
        int leftSize = arr.length/2;
        int rightSize = arr.length-leftSize;
        int l=0, r=0, i=0;
        while(l<leftSize && r<rightSize){
            if(leftArray[l]<rightArray[r]){
                arr[i] = leftArray[l];
                i++;
                l++;
            }
            else{
                arr[i] = rightArray[r];
                i++;
                r++;
            }
        }
        while(l<leftSize){
            arr[i] = leftArray[l];
            i++;
            l++;
        }
        while(r<rightSize){
            arr[i] = rightArray[r];
            i++;
            r++;
        }
    }
}
```
**Quick Sort**
```
public class Main {
    public static void main(String[] args) {
        int[] arr = {9,2,7,6,8,4,3,5,1};
        int n = arr.length;
        quickSort(arr, 0, n-1);
        for(int i: arr)
            System.out.print(i + " ");
    }
    public static void quickSort(int[] arr, int start, int end){
        if(end<=start)
            return;
        int pivot = partition(arr, start, end);
        quickSort(arr, start, pivot-1);
        quickSort(arr, pivot+1, end);
    }
    public static int partition(int[] arr, int start, int end){
        int pivot = arr[end];
        int i = start-1;
        for(int j=start;j<end-1;j++){
            if(arr[j]<pivot){
                i++;
                int temp = arr[i];
                arr[i] = arr[j];
                arr[j] = temp;
            }
        }
        i++;
        int temp = arr[i];
        arr[i] = arr[end];
        arr[end] = temp;
        
        return i;
    }
}
```
