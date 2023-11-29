# Operations on Strings

1. Power of Strings
2. Concatenation of Strings
3. Reverse of a String
4. Prefix of a String
5. Suffix of a String

## Power of Strings

- It is the concatenation of a string with itself n times.
- It is denoted by $S^{n}$.
- Set-Builder Notation: $S^{n}$ | n $\ge$ 0
- Example: S = ab, $S^{2}$ = abab, $S^{3}$ = ababab, etc.

#### Properties of Power of Strings

- $S^{0}$ = ε
- (ab)$^{2}$ $\neq$ a$^{2}$b$^{2}$
- (ab)$^{2}$ $\neq$ (ba)$^{2}$
- (ab)$^{2}$. (ab)$^{3}$ = (ab)$^{5}$ = (ab)$^{3}$. (ab)$^{2}$
- $((ab)^{2})^{3}$ = (ab)$^{6}$ 

#### Proof of No Negative Power of Strings

- We know that $S^{0}$ = ε
- We also know that $S^{n}$ . $S^{-n}$ = $S^{0}$
- But there is nothing that we can concatenate with $S^{n}$ to get $S^{0}$.
- Hence, $S^{-n}$ does not exist.

#### Why $s^{0}$ = ε?

- Like 0 is the identity element of addition, 1 is the identity element of multiplication
- $\epsilon$ is the identity element of concatenation.
    - Let $S^{2}$ = abab
    - Now $S^{2}$ . $S^{0}$ = $S^{2+0}$ = $S^{2}$ = abab
    - Also, $\epsilon$ . $S^{2}$ = $S^{0+2}$ = $S^{2}$ = abab  
    - Hence, $S^{0}$ = ε

#### Power of $\epsilon$

- Let $\epsilon$ = {a,b}
- $\epsilon^{0}$ = {ε}, It is a language which contains all the strings of length 0.
- $\epsilon^{1}$ = {a,b}, It is a language which contains all the strings of length 1.
- $\epsilon^{2}$ = {aa,ab,ba,bb}, It is a language which contains all the strings of length 2.
- $\epsilon^{3}$ = {aaa,aab,aba,abb,baa,bab,bba,bbb}, It is a language which contains all the strings of length 3.
- $\epsilon^{*}$ is union of all languages of all lengths. It is called the Kleene Closure of $\epsilon$. It is largest possible language and hence, also called Universal Language.
- $\epsilon^{+}$ is union of all languages of all lengths except the empty string. It is called the Positive Closure of $\epsilon$.
<br><br>
- $\epsilon^{*}$ is Countably Infinite.
- Every Language is a subset of $\epsilon^{*}$.
- If L is a set of Languages in $\epsilon^{*}$, then L is Uncountably Infinite. Number of elements in L = $2^{|\epsilon^{*}|}$
- If L is a set of Languages in $\epsilon$^{+}, then Number of elements in L = $2^{|\epsilon^{*}|} - 1$
- $\epsilon^{+}$ = $\epsilon^{*} - {ε}$

## Concatenation of Strings

- It is denoted by S.T
- Set-Builder Notation: S.T | S $\in$ A, T $\in$ B
- Example: S = ab, T = cd, S.T = abcd

#### Properties of Concatenation of Strings

- S.ε = ε.S = S
- S.T may or may not be equal to T.S
- If Strings are palindromes, then S.T = T.S else not.
- |S.T| = |T.S| = |S| + |T|
- (S.T).U = S.(T.U) = S.T.U

> If we concatenate n string in any order, the resultant length will be same for all the orders.

#### Question
Q. Consider a string u.v where u $\in \sum and v \in \Sigma^{*}$. Which of the following is true?
1. |u| $\le$ |v|
2. |u| $\ge$ |v|
3. |u| = |v|
4. None of the above

    **A. |u| $\le$ |v|** <br>
    **Explanation:** |u| $\le$ |v| is true because u is a single character and v is a string of length 0 or more.

Q. Consider a string u.v where u $\in \sum and v \in \Sigma^{*}$. What can be the length of u.v?
1. |u| + |v|
2. 1 + |v|
3. Both 1 and 2
4. None of the above

    **C. Both 1 and 2** <br>
    **Explanation:** ,<br>
    u belongs to sigma, sigma is a set of symbol. Hence, |u| = 1. <br> 
    |u| + |v| is the length of u.v. Also, |u| = 1. Hence, 1 + |v| is also the length of u.v.

## Reverse of a String

- It is denoted by $S^{R}$
- Set-Builder Notation: $S^{R}$ | S $\in$ A

#### Properties of Reverse of a String

- (S.T)$^{R}$ = $T^{R}.S^{R}$
- $(S^{R})^{R}$ = S
- |S| = $|S^{R}|$
- $(S^{n})^{R}$ = $(S^{R})^{n}$
- If $\sum$ = {a} and u $\in \sum^{*}$, then u = $u^{R}$
- For case of palindromes, S = $S^{R}$

### Palindrome

- Can be even palindrome or odd palindrome
- Even palindrome Notation: U . $U^{R}$ | U $\in \sum^{*}$
- Odd palindrome Notation: U . V . $U^{R}$ | U $\in \sum^{*}$, V $\in \sum$, V $\neq$ ε

#### Question

Q. Number of strings of length n which are even binary palindromes?
1. $2^{n}$
2. $2^{n-1}$
3. $2^{n+1}$
4. $2^{n/2}$

    **Answer: $2^{n/2}$** <br>
    **Explanation:** <br>
    Let n = 4, now U will be of length 2 and $U^{R}$ will also be of length 2. <br>
    For binary strings, U can be 00, 01, 10, 11. <br>
    Also, U^{R} will be same as of U. <br>
    Hence, total number of strings = 4. <br>

Q. Number of strings of length n which are odd binary palindromes?
1. $2^{n}$
2. $2^{n-1}$
3. $2^{n+1}$
4. $2^{(n+1)/2}$

    **Answer: $2^{(n+1)/2}$** <br>
    **Explanation:** <br>
    Let n = 5, now U will be of length 2 and $U^{R}$ will also be of length 2. <br>
    For binary strings, U can be 00, 01, 10, 11. <br>
    Also, U^{R} will be same as of U. <br>
    Hence, total number of strings = 4. <br>
    Now, V can be 0 or 1. <br>
    Hence, total number of strings = 4 * 2 = 8. <br>

## Prefixes and Suffixes

- Prefixes of a string S are all the strings which can be obtained by removing 0 or more characters from the end of S.
- Suffixes of a string S are all the strings which can be obtained by removing 0 or more characters from the beginning of S.
- Proper Prefixes of a string S are all the strings which can be obtained by removing 1 or more characters from the end of S.
- Proper Suffixes of a string S are all the strings which can be obtained by removing 1 or more characters from the beginning of S.
- Example: S = abc, Prefixes of S = {ε,a,ab,abc}, Proper Prefixes of S = {ε,a,ab}, Suffixes of S = {ε,c,bc,abc}, Proper Suffixes of S = {ε,c,bc}
- Number of Proper Prefixes/Suffixes of a string S = |S|
- Number of Prefixes/Suffixes of a string S = |S| + 1

>> All Prefixes can be substring but all substrings cannot be prefixes.
>> Example: S = abc, Substrings of S = {ε,a,b,c,ab,bc,ac,abc}, Prefixes of S = {ε,a,ab,abc}

**Notations**
- Prefix(U) = {x | U=xy}
- Suffix(U) = {x | U=yx}
- Substring(U) = {x | U=yxz}

#### Question

Q. Number of substrings of a string S of length n?

1. Let's take an example, $\sum$ = {A...Z}, n = 5, S = NITIN
- Substrings of length 0 = 1 ,i.e., ε
- Substrings of length 1 = 3, i.e., N, I, T (Removed I and N as repeated)
- Substrings of length 2 = 4, i.e., NI, IT, TI, IN (now here since no repetition occurred further no need to check for repetition)
- Substrings of length 3 = 3(prev-1), i.e., NIT, ITI, TIN
- Substrings of length 4 = 2(prev-1), i.e., NITI, ITIN
- Substrings of length 5 = 1(prev-1), i.e., NITIN
- Total number of substrings = 1 + 3 + 4 + 3 + 2 + 1 = 14 = ${n(n+1)\over 2} +1 - 2$, here 2 is subtracted because of repeated I and N

**Always calculate like above, never do with formula as it changes according to the string**

2. Calculate for S = MISSISSIPPI
- Substrings of length 0 = 1 ,i.e., ε
- Substrings of length 1 = 4, i.e., M, I, S, P (Removed I, S, P and M whenver they came as repeated)
- Substrings of length 2 = 7, i.e., MI, IS, SS, SI, IP, PI, PP (Removed other substring repetitions)
- Substrings of length 3 = 7, i.e. MIS, ISS, SSI, SIS, SIP, IPP, PPI (Removed other substring repetitions)
- Substrings of length 4 = 7, i.e., MISS, ISSI, SSIS, SISS, SSIP, SIPP, IPPI (Removed other substring repetitions)
- Substrings of length 5 = 7, i.e., MISSI, ISSIS, SSISS, SISSI, ISSIP, SSIPP, SIPPI (No repetition here, hence furhter won't be any repetition)
- Substrings of length 6 = 6(Prev-1), i.e., MISSIS, ISSISS, SSISSI, SISSIP, ISSIPP, SSIPPI
- Substrings of length 7 = 5(Prev-1), i.e., MISSISS, ISSISSI, SSISSIS, SISSISS, ISSIPPI
- Substrings of length 8 = 4(Prev-1), i.e., MISSISSI, ISSISSIS, SSISSISS, SISSIPPI
- Substrings of length 9 = 3(Prev-1), i.e., MISSISSIS, ISSISSISS, SSISSIPPI
- Substrings of length 10 = 2(Prev-1), i.e., MISSISSISS, ISSISSISSI
- Substrings of length 11 = 1(Prev-1), i.e., MISSISSISSI
- Total number of substrings = 1 + 4 + 7 + 7 + 7 + 7 + 6 + 5 + 4 + 3 + 2 + 1 = 54.
