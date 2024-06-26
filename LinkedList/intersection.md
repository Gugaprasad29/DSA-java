**Intersection of Two Sorted LinkedList**
```
class Solution{
   public static Node findIntersection(Node head1, Node head2){
        Node head = new Node(0);
        Node in = head;
        while(head1!=null && head2!=null){
            if(head1.data==head2.data){
                in.next = new Node(head1.data);
                in = in.next;
                head1 = head1.next;
                head2 = head2.next;
            }
            else if(head1.data<head2.data)
                head1 = head1.next;
            else
                head2 = head2.next;
        }
        return head.next;
    }
}
```
**intersection Point of Two LinkedList**
```
class Intersect{
	int intersectPoint(Node head1, Node head2){
	    if(head1==null || head2==null)
	        return -1;
        Node temp1 = head1, temp2 = head2;
        while (temp1 != temp2) {
            temp1 = (temp1 == null) ? head2 : temp1.next;
            temp2 = (temp2 == null) ? head1 : temp2.next;
            if (temp1 == temp2 && temp1 != null)
                return temp1.data;
        }
        return -1;
	}
}
```
