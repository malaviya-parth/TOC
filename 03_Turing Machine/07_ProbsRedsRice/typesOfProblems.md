## Problems
- Problems means the questions which are asked like
  - Ambiguity problem in CFG
  - Hamiltonian Graph Problem
  - Equivalence problem of R.L.

## Instance of Problem:
- A question example asked is called instance of a problem.
  - S -> aS|SS|$\epsilon$, whether this is Ambiguous or not

## Relation b/w language & problem
- Language is a set of yes instances of a problem encoded in binary.
- Problems can be of two types
  - **Optimization Problem:** Find a string w $\in$ L(G) s.t. it has 2 or more parse tree.
  - **Decision Problem:** Is the given CFG Ambiguous.
- Every decision problem has optimized version of it and vice versa. [These problems are interconvertible.]

## Types of Decision Problems
- **Decidable Problem:**
  - Langugae corresponding to it is REC.
  - There exist Algo which always say yes or no
  - Halting Turing Machine exists for this
  - Ex: Is given no. prime?, Is given no. perfect?
- **Semi-Decidable:**
  - RE but not REC
  - There exists procedure which always say YES but in case of NO it may halt.
  - Turing Mahcine or Procedure exits for this.
- **Undecidable:**
  - Non-RE
  - No procedure which can say YES.

- Problems for which you can make program in computer and get answer YES or NO are decidable.
- We will consider Semi-decidable and Undecidable as Undecidable only.
- Properly differentiate in Rice's Theorem.
- Problem is decidable $\Leftrightarrow$ L is REC $\Leftrightarrow$ There exisits HTM accepting L.
- Problem is Undecidable $\Leftrightarrow$ L is not REC $\Leftrightarrow$ There does not exist HTM acepting L.

## Membership Problem
- Given some Language L & W $\in$ $\Sigma^{*}$, Does w $\in$ L?
- Let's go according to the class of Languages

### Membership problem of Regular Languages is Decidable?
- If membership problem of Regular langauges is decidable then there exists algorithm which will take a regular language and a string w as I/P & gives O/P YES if w $\in$ L & NO if w $\notin$ L.
- Regular Language can contain infite string then how to give as input, so instead we provide representation of the Language like FA, RE, etc.
- Like we give binary encoding of FA as I/P to Algo & string (w) also in binary.
- Hence, this problem is decidable.

#### Similarly there exists other machines for otherr class of Languages like DPDA for DCFL, PDA for CFL, LBA for CSL, HTM for REC.
- Hence, Regular, DCFL, CFL, CSL & REC all have decidable membership problems.

#### This Language which check merbership set of REG, CFL, CSL, REC is a REC Language.
#### Compliment of Membership problem will also be decidable because if L is REC hen L' also REC.

> If Language is decidable then it's compliment will also be decidable.  
> If Language is undecidable then it's complimen is also undecidable.

## Emptiness Problem
- Is given L empty or not?

### For REG, DCFL and CFL it is Decidable
### For CSL, REC, RE it is Undecidable
### Compliment of Emptiness probelm
- Is the given L != $\phi$
### Same goes for compliment as Decidable L are REC and REC' = REC

## Completeness Problem
- Is given L = $\Sigma^{*}$
- If L is $\Sigma^{*}$, then L' = $\phi$

### Therefore REG, DCFL are decidable.
### CFL, CSL, REC, RE are Undecidable
### CFL is undecidable because it is not closed under compliment(It has chances to be CSL).
### Compliment of Completeness Problem
- Is the given L != $\Sigma^{*}$

## Equality Problem
- Given two languages L1 & L2 of same type, is L1 = L2?
- Check L1 $\cap$ L2' = $\phi$
- AND L2 $\cap$ L1' = $\phi$
### REG and DCFL are Decidable.
### Other are Undecidable.
### Compliment of Problem:
- Given two languages L1 & L2 of same type, is L1 != L2?

## Disjointness Problem
- Given two languages L1 & L2 of same type, is L1 $\cap$ L2 = $\phi$

### Decidable for REG
### Undecidable for DCFL, CFL, CSL, REC, RE.
### Intesection of DCFL is not closed it can even be CSL, and CSL is Undecidable in Emptiness.

## Finiteness Problem
- Is the given L finite?

### Decidable for REG, DCFL, CFL.
### Undecidable for the rest.

## Subset Problem
- Given two languages L1 & L2 of same type, is L1 subset of L2?
- Similar to equality problem and concept of Disjointness

### Decidable only for REG.
### Undecidable for the rest.

## Ambiguity Problem
- Is given Language Ambiguous?
- Ambiguous Language means we cannot write Unambiguous grammar for it.
  - L = a^nb^nc^m $\cup$ a^nb^mc^m
  - Grammar: S -> S1/S2 and other stuff
  - Now if W = aabbcc, we can get it through either S1 or S2 hence, ambiguity.

### Decidable for REG and DCFL
### Undecidable for the rest.

- Is the given Grammar Ambiguous?

### Decidable for R.G.
### Undecidable for C.F.G., C.S.G., U.G.
### LR Grammar is always unambiguous, so it is decidable.

## Regularity Problem:
- Is the given L regular?

### Decidable for REG and DCFL
### Undecidable for the rest

## Compliment Problem
- Is Compliment of L same type?

### Decidable for REG, DCFL, CSL and REC
### Undecidable for CFL and RE
- In case of RE if specified that it is RE as well as REC or RE but not REC then it is decidable
  - Because if RE as well as REC then compliment always REC
  - If RE but not REC then compliment always Non-RE

## Intersection Problem
- Given 2 Languages, L1 and L2 of same type is L1 $\cap$ L2 of same type.

### Decidable for REG, CSL, REC, RE.
### Undecidable for DCFL, CFL.

# Table
| | Regular | DCFL | CFL | CSL | REC | RE |
|--|--|--|--|--|--|--|
| Membership | ✅ | ✅ | ✅ | ✅ | ✅ | ❌ |
| Emptiness | ✅ | ✅ | ✅ | ❌ | ❌ | ❌ |
| Completeness | ✅ | ✅ | ❌ | ❌ | ❌ | ❌ |
| Equality | ✅ | ✅ | ❌ | ❌ | ❌ | ❌ |
| Subset | ✅ | ❌ | ❌ | ❌ | ❌ | ❌ |
| DisJointness | ✅ | ❌ | ❌ | ❌ | ❌ | ❌ |
| Finiteness | ✅ | ✅ | ✅ | ❌ | ❌ | ❌ |
| Compliment | ✅ | ✅ | ❌ | ✅ | ✅ | ❌ |
| Insertion | ✅ | ❌ | ❌ | ✅ | ✅ | ✅ |
| Regularity | ✅ | ✅ | ❌ | ❌ | ❌ | ❌ |
| Ambiguity | ✅ | ✅ | ❌ | ❌ | ❌ | ❌ |

# Practice Questions on Decidability

1. Given 2 PDA accept same language?
  - Equality problem of CFL
  - L1 = L2 $\implies$ L1 $\cap$ L2' = $\phi$ $\And$ L2 $\cap$ L1' = $\phi$
  - Intersection in CFL is not closed it can be CSL
  - CSL in emptiness is non-decidable
  - Hence, it is not Decidable

2. Given 2 FA accept same language?
   - Equality of REG
   - It is decidable

3. Given string w accepted by TM?
   - Membership set of RE
   - Hence it is Undecidable

4. Given string w accepted by PDA?
   - Membership of CFL
   - It is decidable

5. Given string w generated by CFG?
   - Membership of CFL
   - It is decidable

6. Conversion of PDA to CFG?
   - Same power so conversion algo possible.
   - Hence, it is decidable.
  
7. Conversiomn of NDTM to DTM?
   - It is decidable

8. Conversion of NDPDA to DPDA?
   - It is not decidable because power of both not same.

9. Conversion of DPDA to NDPDA?
    - We can go from less power to more power
    - So, it is Decidable.

10. Conversion of DFA to NFA?
  - It is Decidable.

11. Given FA and PDA accept same language?
  - We can convert FA to PDA
  - Equality of PDA means equality of CFL
  - It is Undecidable.

12. Given PDA accept regular language?
  - Checking regularity of CFL
  - It is undecidable

13. Given CFG generate regular Language?
  - Regularity of CFL
  - It is undecidable

14. Is given PDA accept ambiguous language?
  - Ambiguity of CFL
  - It is Undecidable

15. Is given PDA accept non-regular language?
  - Compliment of Regularity of CFL
  - It is Undecidable

16. Givne TM accept non-empty language?
  - Compliment of emptiness of RE
  - Undecidable

17. Given PDA accpet at least one string?
  - Compliment of Emptiness of CFL
  - It is Decidable

18. Given L = { <G> | is type 3 & L(G) is finite}. Is L REC?
  - Checking Finiteness of Regular
  - It is Decidable
  - Hence, L is REC.

19. L = {<M,W> | W $\in$ L(M)}. Here M is binary encoding of TM & W $\in$ {0,1}*. Is L REC?
  - This langugae is compliment of Diagonalization Language.
  - Given language is RE but not REC as Diagonalization Languages as Non-RE.
  - Hence, it is NOT REC.

20. L = {<G> | G is tyoe1 & L(G) is finite}. Is L REC?
  - Checking Finiteness of CSL
  - It is Undecidable.
  - Hence, It is not REC

21. L = {<G1,G2> | L(G1) $\cap$ L(G2) = $\phi$, where G1 is CFG & G2 is CSG}
  - Disjointness problem
  - Different type given so update
  - Disjointness of CSL
  - It is not Decidable

22. L = {<G1,G2> | L(G1) $\subseteq$ L(G2) = $\phi$, where G1 is CFG & G2 is CSG}
  - Subsetness of CSL
  - It is Undecidable

23. L1 $\subseteq$ L2 (L1 is Regular and L2 is DCFL)
  - Chekcing Subsetness of DCFL
  - It is undecidable

24. L1 U L2 is DCFL ( L1 & L2 are DCFL)
  - DCFL in Union is not closed and can go upto CFL.
  - Hence, checking DCFl -> CFL
  - It is Undecidable

25. Is given CFG Regular grammar?
  - We can check those as grammar is finite.
  - Note here we are checking grammar not the languages.
  - If checking languages then Undecidable.
  - It is decidable.

26. Is the givne CSG, CFG?
  - It is Decidable
  - Note here we are checking grammar not the languages.
  - If checking languages then Undecidable.