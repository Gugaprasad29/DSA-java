**Remove Duplicates Nodes in Sorted LinkedList**
```
class Solution{
    Node removeDuplicates(Node head)
    {
	    Node curr = head;
	    while(curr!=null && curr.next!=null){
	        if(curr.data==curr.next.data)
	            curr.next = curr.next.next;
	       else
	            curr = curr.next;
	    }
	    return head;
    }
}
```
