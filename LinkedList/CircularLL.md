**Check if LL is Circular**
```
class Solution{
    boolean isCircular(Node head){
    	if(head==null || head.next==null)
    	    return false;
    	Node temp = head;
    	do{
    	    temp = temp.next;
    	    if(temp==head)
    	        return true;
    	}while(temp!=head && temp!=null);
    	return false;
    }
}
```
**Split Circular LL into Two Halves**
```
class Solution{
	void splitList(circular_LinkedList list){
        Node head=list.head;
        Node head1=null;
        Node head2=null;
        if(head==null || head.next==null){
            head1 = head;
            if(head1!=null)
                head1.next = head1;
            list.head1=head1;
            list.head2=head2;
            return;
        }
        Node slow = head;
        Node fast = head;
        while(fast.next!=head && fast.next.next!=head){
            slow = slow.next;
            fast = fast.next.next;
        }
        head1 = head;
        head2 = slow.next;
        slow.next = head1;
        Node curr = head2;
        while(curr.next!=head){
            curr = curr.next;
        }
        curr.next = head2;
        list.head1=head1;
        list.head2=head2;
	}
}
```
