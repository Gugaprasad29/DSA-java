**Count and Say**
```
class Solution {
    public String countAndSay(int n) {
        String curr = "1";
        for(int j=1;j<n;j++){
            String next = "";
            int i = 0;
            while(i<curr.length()){
                int count = 1;
                while(i<curr.length()-1 && (curr.charAt(i)==curr.charAt(i+1))){
                    count+=1;
                    i+=1;
                }
                next+=Integer.toString(count)+curr.charAt(i);
                i+=1;
            }
            curr = next;
        }
        return curr;
    }
}
```
