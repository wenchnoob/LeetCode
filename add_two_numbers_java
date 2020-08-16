/**
 * Definition for singly-linked list.
 * public class ListNode {
 *     int val;
 *     ListNode next;
 *     ListNode() {}
 *     ListNode(int val) { this.val = val; }
 *     ListNode(int val, ListNode next) { this.val = val; this.next = next; }
 * }
 */
class Solution {
    public ListNode addTwoNumbers(ListNode l1, ListNode l2) {
        return add(l1, l2);
    }
    
    private ListNode add(ListNode l1, ListNode l2){
        return add(0, l1, l2);
    }
    
    private ListNode add(int carry, ListNode l1, ListNode l2) {
        if (l1 == null && l2 == null)
            if (carry == 0) return null;
            else return new ListNode(1);
        
        if (l1 == null) {
            l2.val += carry;
            
            if (l2.val < 10)
                return l2;
            else {
                carry(l2);
                return l2;
            }
            
        }
        
        if (l2 == null) {
            l1.val += carry;
                
            if (l1.val < 10)
                return l1;
            else {
                carry(l1);
                return l1;
            }
        }
        
        ListNode ans;
        int sum = carry + l1.val + l2.val;
        
        if (sum >= 10){
            ans = new ListNode(sum - 10, add(1, l1.next, l2.next));
        } else {
            ans = new ListNode(sum, add(0, l1.next, l2.next));
        }
        
        return ans;
    }
    
    private void carry(ListNode node) {
        int carry = 0;
        
        if(node.val >= 10){
            carry = 1;
            node.val -= 10;
        }
            
        
        if(node.next == null && carry > 0) {
            node.next = new ListNode(1);
            return;
        }
        
        if (node.next != null) {
            node.next.val += carry;
            carry(node.next);
        }
        
    }
}
