**Finding Distinct digit in an Array**
```
class Solution{
    public int[] common_digits(int[] nums){
        Set<Integer> s = new HashSet<>();
        for(int n:nums){
            while(n>0){
                int rem = n%10;
                s.add(rem);
                n /= 10;
            }
        }
        int[] res = new int[s.size()];
        int i = 0;
        for(int num:s){
            res[i++] = num; 
        }
        return res;
    }
}
```
