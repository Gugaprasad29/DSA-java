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
