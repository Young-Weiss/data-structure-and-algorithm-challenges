[link do problema](https://leetcode.com/problems/linked-list-cycle/description/)

# 141. Linked List Cycle

Para encontrar se uma lista encadeada tem um loop, pode se usar um hash map para conter todos os nodos e verificar se for repetir porém esse código utiliza a técnica de dois ponteiros com velocidades difentes e verificar se eles se encontram


```typescript
/**
 * Definition for singly-linked list.
 * class ListNode {
 *     val: number
 *     next: ListNode | null
 *     constructor(val?: number, next?: ListNode | null) {
 *         this.val = (val===undefined ? 0 : val)
 *         this.next = (next===undefined ? null : next)
 *     }
 * }
 */

function hasCycle(head: ListNode | null): boolean {
    let fast = head;
    let slow = head;

    while(fast && fast.next) {
        fast = fast.next.next;
        slow = slow.next;

        if(fast === slow) return true;
    }
    return false
};
```
