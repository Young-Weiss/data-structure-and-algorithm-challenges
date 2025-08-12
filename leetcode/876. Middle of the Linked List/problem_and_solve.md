[Link do problema](https://leetcode.com/problems/middle-of-the-linked-list/description/)

# 876. Middle of the Linked List
Given the head of a singly linked list, return the middle node of the linked list.

If there are two middle nodes, return the second middle node.


Para conseguir pegar o item do meio de uma linked list sem precisar percorrer toda ela e armazenar o tamanho, posso andar com dois ponteiros, um andando um nodo para frente outro andando dois, assim quando o mais "rápido" chegar ao fim o mais "lento" ira estar na metade.

Minha solução:
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

function middleNode(head: ListNode | null): ListNode | null {
    let fasterHead = head;

    while(fasterHead && fasterHead.next) {
        fasterHead = fasterHead.next.next;
        head = head.next;
    }

    return head;
};
```
