**Find the First Node of the LinkedList**
```
class Solution {
    public static int findFirstNode(Node head){
        if(head==null || head.next==null)
            return -1;
        Node slow = head;
        Node fast = head;
        while(fast!=null && fast.next!=null){
            slow = slow.next;
            fast = fast.next.next;
            if(slow==fast){
                slow = head;
                while(slow!=fast){
                    slow = slow.next;
                    fast = fast.next;
                }
                return slow.data;
            }
        }
        return -1;
    }
}
```
**Find Middle Node of the LinkedList**
```
class Solution {
    public ListNode middleNode(ListNode head) {
        ListNode slow = head, fast = head;
        while(fast!=null && fast.next!=null){
            slow = slow.next;
            fast = fast.next.next;
        }
        return slow;
    }
}
```
