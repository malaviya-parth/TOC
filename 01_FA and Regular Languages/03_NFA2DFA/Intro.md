NFA --Algorithm--> DFA

- Any NFA can be converte into DFA
- NFa and DFA have same power i.e. for any language if one can make NFA and it's DFA is also always possible
- It there are Q states in NFA then there are $2^{Q}$ states in DFA
- if there is "min NFA" with Q states then there the range of states in DFA is $[Q,2^{Q}]$

**Q. Construct DFA where $\Sigma = \{a,b\}$ and third symbol from left is a**

![DFA](image.png)

**Q. Construct DFA where $\Sigma = \{a,b\}$ and third symbol from right is a**

![NFA](image-1.png)

- For constructing DFA from NFA, now we will use algorithm

- First of all make a table of all states of NFA
- Here
    - ![Table](image-2.png)
- Step 1: Initial state of NFA = Initial state of DFA
- Step 2: For each state of DFA, find the states of NFA which are reachable from this state
    - If there are more than one state reacable from this state then make a new state in DFA
- Step 3: In horizontal serial manner, write the states which are reachable from the state of DFA
- Step 4: Repeat step 2 and 3 for all states of DFA
- Step 5: If there is a final state of NFA in the states of DFA then make all those the final state of DFA

- ![DFA Table](image-3.png)
- Now make DFA Diagram from this table
![DFA](image-4.png)
- Mark arrows with a and b from table

- If in initial, there is empty just replace it with dead state
**Q. String starting with a and ending with b**
![Whole](image-5.png)