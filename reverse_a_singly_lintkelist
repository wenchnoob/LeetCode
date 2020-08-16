# Definition for singly-linked list.
# class ListNode(object):
#     def __init__(self, val=0, next=None):
#         self.val = val
#         self.next = next
class Solution(object):
    def addTwoNumbers(self, l1, l2):
        """
        :type l1: ListNode
        :type l2: ListNode
        :rtype: ListNode
        """
        
        if l1 == None or l1.val == 0 and l1.next == None:
            return l2
        if l2 == None or l2.val == 0 and l2.next == None:
            return l1
        
        head = ListNode()
        cur = head
        
        while (l1 != None or l2 != None):
            if cur.next != None:
                cur = cur.next
                
            if l1 != None and l2 != None:
                cur.val += l1.val + l2.val
                l1 = l1.next
                l2 = l2.next
                cur.next = ListNode()
                
            elif l1 != None:
                cur.val += l1.val
                l1 = l1.next
                cur.next = ListNode()
                
            else:
                cur.val += l2.val
                l2 = l2.next
                cur.next = ListNode()
                
            if cur.val > 9:
                cur.val -= 10
                cur.next.val += 1
                
        
        if cur.next.val == 0:
            cur.next = None
            
        return head
