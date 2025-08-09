[link do problema](https://leetcode.com/problems/reverse-linked-list/description/)

# 206. Reverse Linked List

## 📖 Explicação do Algoritmo

O problema **206. Reverse Linked List** pede para inverter uma lista ligada simples.  
Ou seja, se a lista for:

1 → 2 → 3 → 4 → 5

O resultado precisa ser:

5 → 4 → 3 → 2 → 1

### Passo a passo do código

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

function reverseList(head: ListNode | null): ListNode | null {
    if (!head) return null;

    let newList: ListNode | null = null;

    while (head) {
        const nextNode: ListNode | null = head.next;
        head.next = newList;
        newList = head;
        head = nextNode;
    }

    return newList;
}
```

## 🧠 Entendendo o funcionamento

```typescript
if (!head) return null;
```
Se a lista estiver vazia (head === null), não há nada para inverter, então retornamos null.

```typescript
let newList: ListNode | null = null;
```
```typescript
while (head) {
    const nextNode: ListNode | null = head.next; // Guarda o próximo nó
    head.next = newList; // Invertemos a direção do ponteiro
    newList = head; // Atualizamos a cabeça da lista invertida
    head = nextNode; // Avançamos para o próximo nó
}
```
```typescript
return newList;
```
Ao final do loop, newList será a cabeça da lista invertida.
