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
**QuickSort in LinkedList**
```
class Solution{
    public static Node quickSort(Node node){
        if (node == null || node.next == null)
            return node;
        Node last = getLastNode(node);
        return Sort(node, last);
    }
    static Node getLastNode(Node node) {
        while (node != null && node.next != null) {
            node = node.next;
        }
        return node;
    }
    static Node Sort(Node node, Node last){
        if(node!=last && node!=null && last!=null && node!=last.next){
            Node pivot = partition(node, last);
            Node newHead = Sort(node, getPreviousNode(node, pivot));
            Node newTail = Sort(pivot.next, last);
            return newHead;
        }
        return node;
    }
    static Node getPreviousNode(Node low, Node target){
        Node prev = null;
        while (low != target) {
            prev = low;
            low = low.next;
        }
        return prev;
    }
    static Node partition(Node low, Node high){
        int pivot = high.data;
        Node i = low, j = low;

        while (j != high) {
            if (j.data < pivot) {
                int temp = i.data;
                i.data = j.data;
                j.data = temp;
                i = i.next;
            }
            j = j.next;
        }
        int temp = i.data;
        i.data = high.data;
        high.data = temp;
        return i;
    }
}
```
