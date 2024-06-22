**Navie Approach**
```
import java.util.*;

class Main{
    public static void main(String[] args){
        String s1 = "abcd";
        String s2 = "cdab";
        if(s1.length()!=s2.length())
            System.out.println("S2 is not a rotation S1");
        else{
            ArrayList<Integer> index = new ArrayList<>();
            int l = s1.length();
            char f_char = s1.charAt(0);
            for(int i=0;i<l;i++){
                if(s2.charAt(i)==f_char)
                    index.add(i);
            }
            boolean flag = false;
            for(int idx:index){
                flag = rotation(s1, s2, idx, l);
                if(flag)
                    break;
            }
            if(flag)
                System.out.println("Rotate");
            else
                System.out.println("Not rotate");
        }
    }
    public static boolean rotation(String s1, String s2, int indexes, int l){
        for(int i=0;i<l;i++){
            if(s1.charAt(i)!=s2.charAt((indexes+i)%l))
                return false;
        }
        return true;
    }
}
```
