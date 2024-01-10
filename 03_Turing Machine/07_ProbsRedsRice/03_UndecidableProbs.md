# Halting Problem of Turing Machine
- Given a Turing Machine and string w, while processing w TM will halt?

- To check whether TM halt or not we need to give input to a universal TM of string and Binary encoding of the TM to be checked, now since the input TM will not halt and if goes to infinite loop, then how can we know whether The input will Halt or not.
- Hence, Universal TM also goes in infinite loop.
- So, it is undecidable.
- It is RE but not REC, because it halts at Yes instance, but not Halts at No instance.

### Compliment of Halting Problem
- Given a Turing Machine and string w, while processing w TM will not Halt?
- It's Language will be Non-RE as original was RE but not REC.

## Linking with Diagonalization Language
- The $L_{u}$ Language learnt in Diagonalization is subset of Halting problem.
- $L_{u}$ accpets w of TM, where TM accept w and hence halt
- Halt Prob accepts w of TM, where TM accept or reject w but halt.

# Blank Tape Halting Problem
- If an arbitary TM is started on blank tape will it eventually halt?
- RE but not REC
- In blank tape TM removes two blanks with a and b and then check will TM halt
- So, it will resemble to Halting Problem.
- Hence, it is Undecidable.

## How to prove given problem P is Undecidable?
- Reduce a known Undecidable Problem to P.

## How to prove P is Decidable?
- Reduce P to a known Decidable problem.

# State Entry Problem
- Given a TM(M) & string (w), while processing w, m will enter state q?
- RE but not REC
- We can also call it as, From any halted state if w enters state q will it halt?
- Hence, resembles to Halting problem, So it is Undecidable.

# Post's Correspondence Problem
- Given two list, is there any solution, means picking two strings from each row again and again untill aggregate string picked from both List becomes same.
- RE but not REC
- It is unDecidable Problem

# RE membership Problem
- RE but not REC
- $L_{u}$ is reduce to this Problem.
- It is Undecidable.