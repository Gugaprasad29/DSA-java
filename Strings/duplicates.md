**Hash method**
```
import java.util.*;
class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        String a = s.nextLine();
        duplicate(a);
    }
    static void duplicate(String a){
        Map<Character, Integer> co = new HashMap<>();
        for(int i=0;i<a.length();i++){
            if(co.containsKey(a.charAt(i)))
                co.put(a.charAt(i), co.get(a.charAt(i))+1);
            else
                co.put(a.charAt(i),1);
        }
        for(Map.Entry<Character, Integer> mapElement:co.entrySet()){
            if(mapElement.getValue()>1)
                System.out.println(mapElement.getKey()+" count = "+mapElement.getValue());
        }
    }
}
```
