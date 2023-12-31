# Basic Terms

### Symbol 
- It can be a character.
- It is a basic unit of a language.
- Example: a, b, c, 1, 2, 3, +, -, *, /, etc.

### Alphabet
- It is a <b>non-empty</b> <b>finite</b> set of <b>symbols</b>.
- It is denoted by Σ.
- Example: {a, b, c}, {0, 1}, {a, b, c, 0, 1}, etc.

### String
- It is a <b>finite</b> sequence of <b>symbols</b> from an <b>alphabet</b>.
- It is denoted by w.
- Given an alphabet Σ, the set of all strings over Σ is denoted by Σ*.
- Example: Σ = {a, b, c}, w = ab, w = abc, w = aab, etc. but w = aabbb..., w = acd, etc. are not strings. (Because one is infinite and another is not from the alphabet Σ.)
- $\epsilon$ is a string which contains no symbol. It is called the empty string.
- If $S_{1}$ = $0^{4}$, then $S_{1}$ = 0000.
- If $S_{2}$ = $2^{0}$, then $S_{2}$ = ε (empty string).
- If $S_{3}$ = $0^{-1}$, then $S_{3}$ = undefined.
- If $S_{4}$ = $0^{a}$, where a is a real number, then $S_{4}$ = undefined.
- If $S_{5}$ = $2^{5}$ and $S_{6}$ = $0^{4}$ are two strings, then $S_{5}$ . $S_{6}$ is the concatenation of $S_{5}$ and $S_{6}$ which is equal to 222220000.

### Length of a String
- It is the number of symbols in a string.
- It is denoted by |w|.
- Example: w = ab, |w| = 2, w = abc, |w| = 3, w = aaabccc, |w| = 7, etc.

### Substring
- It is a sequence of consecutive symbols of a string.
- Null string is a substring of every string.
- Proper substring is a substring which is not equal to the string itself.
- Example: w = ab, substrings of w are a, b, ab, ε, etc. but proper substrings of w are a, b, ε, etc.
- Note: The number of substrings of a string of length n is n(n+1)/2.

### Language
- It is a set of strings.
- Example: Σ = {a, b, c}
    - Set of Strings of length 1: {a, b, c}
    - Set of Strings of length 2: {aa, ab, ac, ba, bb, bc, ca, cb, cc}
- Language is denoted by L.
- Language can be finite or infinite.
- $\phi$ is a language which contains no string. It is called the empty language.

- $\Sigma^{*}$ is union of all languages of all lengths. It is called the Kleene Closure of $\epsilon$. Also called Universal Language.
- $\Sigma^{+}$ is union of all languages of all lengths except the empty string. It is called the Positive Closure of $\epsilon$.

**Important Examples of Languages**
- For Σ = {a,b,0}
- String with even number of 0s: {ε, 00, 0000, 000000, ...}
- String starting with a: {a, aa, a0b, a0a, a0b0, a0b0a, ...}
- String starting with a and ending with b: {ab, aab, a0b, a0ab, a0b0b, a0b0ab, ...}
- Language of Strings of zero length: {ε}

> Every Symbol is a String &#x2611; <br>
> Every String is a Symbol &#x2612; <br>
> Every Alphabet is a String &#x2612; <br>

**Note:** <br>
    - $a^0 = ε$ <br>
    - $\Sigma^{0}$ = {ε} <br>
    - $\epsilon \not \in \sum$ <br>
    - When we write $u \in \sum$, it means that u is a string of length 1. <br>
    - When we write $u \in \Sigma^{*}$, it means that u is a string of any length including 0. <br>
    - When we write $u \in \Sigma^{+}$, it means that u is a string of any length except 0. <br>

## Questions

1. String is of length n and is made up of 'n' symbols then number of Substrings are: <br>
    - [] n <br>
    - [] n+1 <br>
    - [x] n(n+1)/2 + 1<br>
    - [] n(n-1)/2 <br>

    **Solution:** n(n+1)/2 <br>
    **Explanation:** S = abc <br>
    Substrings of S are a, b, c, ab, bc, abc, ε

2. String with length n and all symbols are same then number of substrings are: <br>
    - [] n <br>
    - [] 1 <br>
    - [x] n+1 <br>
    - [] n(n+1)/2 <br>

    **Solution:** n+1 <br>
    **Explanation:** S = aaaa <br>
    Substrings of S are a, aa, aaa, aaaa, ε

3. How many Strings of length 'n' can be made using 'k' different symbols
    - [] k <br>
    - [] k+1 <br>
    - [x] $k^{n}$ <br>
    - [] $k^{n+1}$ <br>

    **Solution:** $k^{n}$ <br>
    **Explanation:** S = {a, b, c} <br>
    Strings of length 2 are aa, ab, ac, ba, bb, bc, ca, cb, cc <br>
    Here we think of n=2 places in which k=3 elements can be put. <br>
    So, total number of strings = $k^{n}$ = $3^{2}$ = 9
