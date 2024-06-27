**MergeSort in LinkedList**
```
class Solution{
    static Node mergeSort(Node head){
        if(head==null || head.next==null)
            return head;
        Node slow = head, fast = head.next;
        while(fast!=null && fast.next!=null){
            slow = slow.next;
            fast = fast.next.next;
        }
        Node middle = slow;
        Node right = middle.next;
        middle.next = null;
        Node left = head;
        left = mergeSort(left);
        right = mergeSort(right);
        return Sort(left, right);
    }
    static Node Sort(Node l, Node r){
        Node curr = new Node(-1);
        Node temp = curr;
        while(l!=null && r!=null){
            if(l.data<r.data){
                temp.next = l;
                temp = l;
                l = l.next;
            }
            else{
                temp.next = r;
                temp = r;
                r = r.next;
            }
        }
        if(l!=null)
            temp.next = l;
        else
            temp.next = r;
        return curr.next;
    }
}
```
