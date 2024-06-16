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
**Palindrome or not**
```
class Solution {
    int isPalindrome(String S) {
        int a = S.length()-1;
        int i = 0;
        while(i<a){
            if(S.charAt(i)==S.charAt(a)){
                i++;
                a--;
            }
            else
                return 0;
        }
        return 1;
    }
}
```
