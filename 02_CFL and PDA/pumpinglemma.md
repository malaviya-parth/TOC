## Important Points:
- It gives necessary condition but not sufficient condition for CFL.
- So if L passes pumping lemma test for CFL then L may or may not be CFL but if this tests fails then L is not CFL.
- Hence evry CFL passes pumping lemma test.
- If L be CFL & W $\in$ L such that |w| $\geq$ n for some +ve integer n then w can be decomposedd into 5 parts w = abcde such that:
    - |bd| $\gt$ 0 [|b| can be 0 & |d| can be 0, but |bd| $\neq$ 0]
    - 1 $\leq$ |bcd| $\leq$ n
    - $\forall i \geq 0$ ab$^i$cd$^i$e $\in$ L

## L = {$x^ny^nz^n$ | n $\geq$ 0} is not CFL. by pumping lemma.
- we can only take b and d two variables here we need to maintain 3 variables eqaul so not possible.