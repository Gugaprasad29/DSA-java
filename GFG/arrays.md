**Given an array arr[] and an integer k where k is smaller than the size of the array, the task is to find the kth smallest element in the given array. It is given that all array elements are distinct.**
```
class Solution{
    public static int kthSmallest(int[] arr, int l, int r, int k) 
    { 
        Arrays.sort(arr);
        return (arr[k-1]);
    } 
}
```
**Given two arrays a[] and b[] of size n and m respectively. The task is to find the number of elements in the union between these two arrays.**
```
class Solution{
    public static int doUnion(int a[], int n, int b[], int m) 
    {
       HashSet<Integer> union = new HashSet<>();
       for(int i:a){
           union.add(i);
       }
       for(int i:b){
           union.add(i);
       }
       return union.size();
    }
}
```
**Given an array, rotate the array by one position in clock-wise direction.**
```
class Compute {
    
    public void rotate(int arr[], int n)
    {
        int temp = arr[n-1];
        int i = n-2;
        while(i>=0){
            arr[i+1] = arr[i];
            i--;
        }
        arr[0] = temp;
    }
}
```
