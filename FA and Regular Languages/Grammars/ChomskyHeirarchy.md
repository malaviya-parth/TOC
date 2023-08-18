## Chomsky divided Grammmar in 4 categories

- Type 0
- Type 1
- Type 2
- Type 3

### Type 0: Unrestricted / Universal Grammar
    - No restriction on the rules
    - For LHS -> RHS
    - LHS can be any string with atleat one non-terminal symbol
    - RHS can be any string
    - Example: aA -> acbd
               aABcd -> acbDE

### Type 1: Length Increasing/ Context Sensitive/ Non-Contracting
    - Def: Grammar must be type 0
    -  |LHS| <= |RHS|

Example: aA -> acbd
         aABcd -> acbDE

- Now we know length of $\epsilon$ is 0 although S-> $\epsilon$ is accepted provided S must be reused i.e. not appear in RHS of any rule (So only allowed with start symbol)

Example: <br>
1. S --> $\epsilon$/A ✅
2. S --> $\epsilon$/ab/aBcD ✅

3. S -> $\epsilon$/A <br>
A -> aS ❌

### Context Sensitivity

- $\alpha$ A $\beta$ -> $\alpha\gamma\beta$ where $\gamma$ is not $\epsilon$
- $\alpha$ and $\beta$ are (N + T)*
- A is a non-terminal symbol
- $\gamma$ = $(N + T)^{+}$

### Example:
- aA -> aBc (This is only left context sensitive)
- Ab -> aBb (This is only right context sensitive)
- aAb -> aBb (This is both left and right context sensitive)

## Type 2: Context Free Grammar

- Def: Grammar must be type 1
- LHS must be a single non-terminal symbol

### Examples:

| Grammar | Type 2 | Type 1 | Type 0 |
|---------|--------|--------|--------|
| A -> aSb | ✅ | ✅ | ✅ |
| aA -> aBc | ❌ | ✅ | ✅ |
| aA -> b | ❌ | ❌ | ✅ |
| aa -> abc | ❌ | ❌ | ❌ |
| S -> ϵ | ✅ | ✅ | ✅ |
| A -> ϵ | ✅ | ❌ | ✅ | 
- Last one is exception states Type-2 allows null production but not Type-1

### Why Null Production is not allowed in Type-2?
#### Answer: There is an algorithm to remove Nul production from the Grammar keeping the language same, but it runs only on Type-2 and Type-3 Grammar

