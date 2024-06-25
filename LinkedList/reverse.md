**Reverse in Group**
```
class Solution
{
    public static Node reverse(Node node, int k)
    {
        if(node==null || k<=1)
            return node;
        Node next = null;
        Node curr = node;
        Node prev = null;
        int count = 0;
        while(curr!=null && count<k){
            next = curr.next;
            curr.next = prev;
            prev = curr;
            curr = next;
            count++;
        }
        if(next!=null)
            node.next = reverse(next, k);
        return prev;
    }
}
```
