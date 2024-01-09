## Closure Properties

1. Transpose:-
    - ❌, DCFL is not closed under transpose
    - Ex: L = $a^nb^n(a+b)^*$ is DCFL
      - a push, b cut, (a+b)^* => ignore further a's and b's
    - $L^T = (a+b^*)b^na^n$ is not DCFL
      - we don't know upto whcih b we have to ignore a's and b's

2. Union:-
   - ❌, DCFL is not closed under union

3. Intersection:-
   - ❌, DCFL is not closed under intersection

4. Concatenation:-
   - ❌, DCFL is not closed under concatenation
   - We can't know when tail of first string ends and head of second string starts.

5. Compliment:-
   - ✅, DCFL is closed under compliment

6. Set Difference:-
    - ❌, DCFL is not closed under set difference
  
7. Union with Regular Language:-
    - ✅, DCFL is closed under union with regular language

8. Intersection with Regular Language:-
    - ✅, DCFL is closed under intersection with regular language


## Table

| Operation | Regular | DCFL | CFL | CSL | REC | RE |
| --- | --- | --- | --- | --- | --- | --- |
| Transpose | ✅ | ❌ | ✅ | ✅ | ✅ | ✅ |
| Concatenation | ✅ | ❌ | ✅ | ✅ | ✅ | ✅ |
| Union | ✅ | ❌ | ✅ | ✅ | ✅ | ✅ |
| Intersection | ✅ | ❌ | ❌ | ✅ | ✅ | ✅ |
| Compliment | ✅ | ✅ | ❌ | ✅ | ✅ | ❌ |
| Set Difference | ✅ | ❌ | ❌ | ✅ | ✅ | ❌ |
| Union with Regular Language | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ |
| Intersection with Regular Language | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ |

## Ways to remember this table

1. Regular, CFL, REC are closed under all operations
2. DCFl $\rightarrow$ closed under compliment
3. CFL $\rightarrow$ Not closed under compliment, set difference, & intersection
4. RE $\rightarrow$ Not closed under compliment, & set difference
5. All are closed under union with regular language & intersection with regular language

# Questions

## DCFL $\cap$ DCFL
- DCFL is not closed under intersection
- So it can be intersection
- CFL is not closed under intersection
- So, it can be CSL
- CSL is closed under intersection
- So, Answer is `CSL` always & may or may not be CFL, DCFL

## DCFL $\cup$ CFL
- DCFL is not closed under union
- CFL is closed under union
- DCFL $\cup$ CFL we need to upgrade, so answer is `CFL`

## Regular $\cap$ DCFL
- Union & Intersection with regular language is closed for all
- So, answer is `DCFL`

## Wich is correct
- [ ] Regular $\cap$ DCFL = DCFL
- [ ] Regular $\cap$ DCFL = CFL
- [ ] Regular $\cap$ DCFL = CSL
- [ ] Regular $\cap$ DCFL = Regular

### Solution
- A, B, C


## DCFL $\cup$ DCFL
- DCFL is not closed under union
- So, it can be CFL
- CFL is closed under union
- So, Answer is `CFL`

