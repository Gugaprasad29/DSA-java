**Adding 1 to a Number Represented as LinkedList**
```
class Solution{
    public static Node addOne(Node head){ 
        Stack<Node> s = new Stack<>();
        Node curr = head;
        int carry = 1;
        while(curr!=null){
            s.push(curr);
            curr = curr.next;
        }
        while(!s.isEmpty()){
            curr = s.pop();
            int sum = curr.data+carry;
            carry = sum/10;
            curr.data = sum%10;
        }
        if (carry > 0){
            Node newHead = new Node(carry);
            newHead.next = head;
            head = newHead;
        }
        return head;
    }
}
```
