[Link do problema](https://leetcode.com/problems/power-of-three/description/?envType=daily-question&envId=2025-08-14)

326. Power of Three
Solved
Easy
Topics
premium lock icon
Companies
Given an integer n, return true if it is a power of three. Otherwise, return false.

An integer n is a power of three, if there exists an integer x such that n == 3x.


Solução:

```typescript
function isPowerOfThree(n: number): boolean {
    if(n <= 0) return false;

    while(n % 3 === 0) {
        n /= 3;
    }

    return n === 1;
};
```
