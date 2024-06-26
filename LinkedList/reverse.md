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
**Move Last Elemment to First**
```
class Solution {
    public static Node moveToFront(Node head) {
        if(head==null || head.next==null)
            return head;
        Node temp = head;
        while(temp.next.next!=null){
            temp = temp.next;
        }
        Node tail = temp.next;
        temp.next = null;
        tail.next = head;
        head = tail;
        return head;
    }
}
```
