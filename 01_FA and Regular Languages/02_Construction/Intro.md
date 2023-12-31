## FA

- It is abbrevation of finite automata
- As soon as we give valid input it starts running
- Like if $\Sigma$ = {a,b} then String input of abc is invalid

- Ther are two types of automata
    1. Finite Automata (Discrete Automata) Example: Digital Speedometer
    2. Infinite Automata (Continuous Automata) Example: Analog Speedometer
    - Decided based on the number of stages

- There are three main things to take care in finite Automata
    1. Input (String)
    2. State
    3. Output (Y: String is accepted, N:String is rejected)

- It is represented by **"5 Tuple"**
- Those 5 tuple are Q,$\Sigma,\delta,q_{0},f$
    - Q = Non-Empty finite state of States
    - $\Sigma$ = Imput Alphabet (Finite and Non-Empty set of Symbols)
    - $q_{0}$ = initial state (without reading any input symbol) $q_{0}$ belongs to Q
    - f = finite set of final states
        - f subset or = to Q
    - $\delta$ states the rules and regulation of in which next state FA will go after reading the input

- FA consist a tape of infinite length divided into cells, each cell can store one symbol at a time.
- We have a read head, one end is connected to the tape and other end is connected to a buffer called Finite State Control Mechanism(store current state of FA).
- Read head moves from left to right or right to left so only in one direction and one symbol at a time.

- According to $\delta$ FA is divided into 2 categories
    1. DFA (Deterministic Finite Automata)
    2. NFA (Non-Deterministic Finite Automata)

- DFA function is represented by Q x $\Sigma$ -> Q
- Example: Q = {$q_{0}, q_{1}, q_{2}$}
           $\Sigma$ = {a,b}
    then: 
    Q x $\Sigma$ = ${ (q_{0},a), (q_{0},b), (q_{1},a), (q_{1},b), (q_{2},a), (q_{2},b) }$
    and it is mapped Many-to-one to Q = {$q_{0},q_{1},q_{2}$}

    - Functions are written as:
        - $\delta(q_{0},a) = q_{0}$
        - $\delta(q_{0},b) = q_{2}$
        - etc...

- For every input symbol we get a unique move

- NFA is represented as Q x $\Sigma$ -> $2^{Q}$
- Example: Q = {$q_{0}, q_{1}$}
           $\Sigma$ = {a,b}
    then:
        Q x $\Sigma$ =  ${ (q_{0},a), (q_{0},b), (q_{1},a), (q_{1},b) }$ is mapped to $2^{Q}$, where
        $2^{Q}$ = ${ \phi, {q_{0}}, {q_{1}}, {q_{0},q_{1}} }$

    - Functions are written same as above
    - $\delta(q_{1},a) = \phi$
    - $\delta(q_{0},a)$ = { $q_{0}$ }
    - $\delta(q_{0},b)$ = { $q_{1}$ }
    - There is a condition where we get to $\phi$ such state is called **Dead Configuration State** possible only in NFA.
    - ALso $4^{th}$ element we could in such state we get option of where to move.

- DFA definition is itself inside NFA
- DFA is special case of NFA where Dead Configuration and Multiple choices are not allowed
- By Default FA means NFA