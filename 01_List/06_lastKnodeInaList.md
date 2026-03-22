![题面](题面/06_1.png)
![题面](题面/06_2.png)
```cpp
/**
 * struct ListNode {
 *	int val;
 *	struct ListNode *next;
 *	ListNode(int x) : val(x), next(nullptr) {}
 * };
 */
class Solution {
public:
    /**
     * 代码中的类名、方法名、参数名已经指定，请勿修改，直接返回方法规定的值即可
     *
     * 
     * @param pHead ListNode类 
     * @param k int整型 
     * @return ListNode类
     */
    ListNode* FindKthToTail(ListNode* pHead, int k) {
        ListNode* head = pHead;
        ListNode* tail = pHead;
        while(k)
        {
            if(!head) return nullptr;
            head = head->next;
            k--;
        }
        while(head)
        {
            head = head->next;
            tail = tail->next;
        }
        return tail;
    }
};
```