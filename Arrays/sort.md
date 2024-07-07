**Sort the Array elements, by Odd Numbers in Descending Order, Even Numbers in Ascending Order.**
```
class Solution{
    public void sortIt(long arr[], long n){
        List<Long> odd = new ArrayList<>();
        List<Long> even = new ArrayList<>();
        for(int i=0;i<n;i++){
            if(arr[i]%2!=0)
                odd.add(arr[i]);
            else
                even.add(arr[i]);
        }
        Collections.sort(odd, Collections.reverseOrder());
        Collections.sort(even);
        int k = 0;
        for(long i:odd)
            arr[k++] = i;
        for(long j:even)
            arr[k++] = j;
    }
}
```
