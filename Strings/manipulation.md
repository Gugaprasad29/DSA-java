**Reverse String**
```
class Solution {
    public void reverseString(char[] s) {
        int a = s.length-1;
        for(int i=0;i<s.length/2;i++){
            char temp = s[i];
            s[i] = s[a];
            s[a] = temp;
            a--;
        }
    }
}
```
