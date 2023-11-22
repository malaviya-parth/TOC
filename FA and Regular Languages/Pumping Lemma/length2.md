## Clarification regarding last point 9

- $L = L_{1} \cup L_{2}$ & $L_{1} \cap L_{2} = \phi$ then M.P.L.(L) = max(M.P.L. for $L_{1}$, M.P.L. for $L_{2}$).
    - L = { $a^{n} | n \geq 2 \cup b^{n}$ | n $\geq$ 4}, then P.L. = 5
    - P.L. for first is 3, P.L. for second is 5 $\therefore$ P.L. for L is 5.  
  
**Here union of two language is as it is, no new string is added, hence we can take = sign over here.**
**If union of both produces new strings then we have to take $\leq$ sign.**

- Example:
  - L = { $aa \cup aaaa*$ } $L_{1} \cap L_{2} = \phi$
  - L = {aaa*}
  - Here we need to calculate as L is aaa* and not both are joined together. So we need to take $\leq$ sign.
  - M.P.L. for L = 3.
  - Taking max it must have come 4 but as new string are not added we take $\leq$ sign.

## Q1 MPL for 0001*
- $w_{min}$ = 000
- M.P.L. $\gt w_{min}$ = 3
- M.P.L. = 4

## Q2 0*1*
- $w_{min}$ = $\epsilon$
- M.P.L. $\gt w_{min}$ = 1

## Q3 001 $\cup$ 0*1*
- 001 $\in$ L
- 001 $\cup$ 0*1* = 0*1*
- $w_{min}$ = $\epsilon$
- M.P.L. $\gt w_{min}$ = 1

## (01)*
- $w_{min}$ = $\epsilon$
- M.P.L. $\geq w_{min}+1 = 1$
- For MPL = 1
  - For string of length 1 we have 0 and 1, both are not present in the language. Test Passed.
  - For string of length 2 we have 01 which is present in the language. Now we need to check keeping length of pattern 1 that whether pumping the pattern generate the strings present in the language.
    - Keeping 0 as pattern we get strings, 001, 0001, etc. which are not present in the language. 
    - Keeping 1 as pattern we get strings, 011, 0111, etc. which are not present in the language.
    - Test Failed.
- For MPL = 2
  - For string of Length 2 we have 01 which is present in the language. Now we need to check keeping length of pattern 2 that whether pumping the pattern generate the strings present in the language.
    - Keeping 01 as pattern we get strings, 0101, 010101, etc. which are present in the language.
    - Test Passed.
- Hence MPL = 2.

## Q4 1*01*01*
- $w_{min}$ = 00
- M.P.L. $\geq w_{min}+1 = 3$
- Let MPL = 3
  - For string of length 3 we have 010, 100, 001 which are not present in the language.
    - Keeping 1 as pattern we get strings, 0110, 01110, etc. which are present in the language.
- Hence MPL = 3.

## Q5 10(11*0)*0
- $w_{min}$ = 100
- M.P.L. $\geq w_{min}+1 = 4$
- Let MPL = 4
  - For string of length 4 we have no string present in the language. Test Passed.
  - For string of length 5 we have 10100 which is present in the language. We can have pattern 10 which if we keep repeating we get strings present in the language.
  - For string of length 6 we have 101110 which have pattern 110 which if we keep repeating we get strings present in the language.
- Hence MPL = 4.

## Q6 1011 + 101011
- Finite Length string are present in the language.
- MPL = | $w_{max}$ | + 1 = 6 + 1 = 7

## Q7 All possible strings over except strings of length 3
- L = { $\epsilon$ , a, b, ab, ba, aa, bb} $\cup$ (a+b)(a+b)(a+b)(a+b)(a+b)*
- MPL( $L_{1}$ ) = | $w_{max}$ | + 1 = 2 + 1 = 3
- MPL( $L_{2}$ ) = | $w_{min}$ | + 1 = 4 + 1 = 5
- MPL(L) = max(MPL($L_{1}$), MPL($L_{2}$)) = 5
<br/> <br/>

# GATE Question
## Q8 L = { $x | x = a^{3+2k} || x = b^{10+12k}$ }

- L = { $a^{3}, a^{5}, a^{7}, ... \cup b^{10}, b^{22}, b^{34}, ...$ }
- MPL($L_{1}$) = | $w_{min}$ | + 1 = 3 + 1 = 4
  - No 4 length string so test passed.
  - For 5 length string we have aaaaa which is present in the language and from the equation we could se that if we keep on pumping aa we get strings present in the language.
  - Same goes for other so, MPL( $L_{1}$ ) = 4
- MPL( $L_{2}$ ) = | $w_{min}$ | + 1 = 10 + 1 = 11
  - No 11 length string so test passed.
  - For string of length 22, we can't keep on pumping b with pattern length 11 as it will generate string of length 23 which is not present in the language.
  - We need to pump with pattern length 12, so we get string of length 22 which is present in the language.
  - Just like above whichever strings are present in the language if we keep on pumping 12b we get strings present in the language.
  - Same goes for other, so MPL( $L_{2}$ ) = 12
- Also, when we combine both the language we won't get conflicting strings as both are different.
- So = sign can be used.
- MPL(L) = max(MPL( $L_{1}$ ), MPL( $L_{2}$ )) = 12
