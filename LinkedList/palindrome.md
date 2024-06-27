**Plaindrome LinkedList**
```
class Solution{
    boolean isPalindrome(Node head) {
        if (head == null || head.next == null){
            return true;
        }
        Node slow = head, fast = head;
        while(fast!=null && fast.next!=null){
            slow = slow.next;
            fast = fast.next.next;
        }
        Node newhead = reverse(slow);
        Node first = head, second = newhead;
        while(newhead!=null){
            if(first.data!=newhead.data){;
                return false;
            }
            first = first.next;
            newhead = newhead.next;
        }
        reverse(second);
        return true;
    }
    Node reverse(Node newhead){
        Node prev = null;
        Node curr = newhead;
        Node next = null;
        while(curr!=null){
            next = curr.next;
            curr.next = prev;
            prev = curr;
            curr = next;
        }
        return prev;
    }
}

```
