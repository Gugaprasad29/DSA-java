**Remove Duplicates Nodes in Sorted LinkedList**
```
class Solution{
    Node removeDuplicates(Node head){
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
**Remove Duplicates Nodes in Unsorted LinkedList**
```
class Solution{
    public Node removeDuplicates(Node head) {
        Node curr = head;
        Node prev = null;
        HashSet<Integer> seen = new HashSet<>();
	while(curr!=null){
		if(seen.contains(curr.data))
	            prev.next = curr.next;
	        else{
	            seen.add(curr.data);
	            prev = curr;
	        }
	        curr = curr.next;
	}
	return head;
    }
}
```
