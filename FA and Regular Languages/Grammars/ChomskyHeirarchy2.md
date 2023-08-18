### Type 3: 

- Regular Grammars
- LHS -> RHS
- LHS is a single non-terminal
- RHS is non-terminal followed by any number of terminals or a single terminal $(NT^{*})/T^{*}$<br>**OR**<br> Any number of terminals followed by a non-terminal or a single terminal $(T^{*}N)/T^{*}$
>Note both, should accpet any one of the two

### Examples:
- A -> aS ✅
- A -> Sab ✅
- A -> aSb/ϵ ❌
- A -> aS/ϵ ✅

**Linear Grammars:** RHS of production rule should have atmost one non-terminal
- A -> aS ✅
- A -> aSb/ϵ ✅ (Contains only one non-terminal position does not matter in Linear Grammar)

- Type 3 Grammmars are subset of Linear Grammars

- The extreme position conditions in Type3 grammar
    - if it is of type $(NT^{*})/T^{*}$ then it is called **Left Linear Grammar**
    - if it is of type $(T^{*}N)/T^{*}$ then it is called **Right Linear Grammar**

### Extras

- Type 3 Grammar generates Regular Languages which are accepted by Finite Automata
- Tpye 2 Grammar generates Context Free Languages which are accepted by Push Down Automata
- Type 1 Grammar generates Context Sensitive Languages which are accepted by Linear Bounded Automata
- Type 0 Grammar generates Recursively Enumerable Languages which are accepted by Turing Machines

- A Language is called regular Language if and only if there exist a Regular Grammar that generates it **OR** Finite Automata that accepts it
- A Language is called Context Free Language if and only if there exist a Context Free Grammar that generates it **OR** Push Down Automata that accepts it
- A Language is called Context Sensitive Language if and only if there exist a Context Sensitive Grammar that generates it **OR** Linear Bounded Automata that accepts it
- A Language is called Recursively Enumerable Language if and only if there exist a Recursively Enumerable Grammar that generates it **OR** Turing Machine that accepts it