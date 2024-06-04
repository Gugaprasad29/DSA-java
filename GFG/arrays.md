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
