** Check if LL is Circular**
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
