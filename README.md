# CSA1304 - Theory of Computation Lab Experiments

Comprehensive implementation of all 40 laboratory experiments for **CSA1304: Theory of Computation**, including Context-Free Grammars (CFG), Deterministic Finite Automata (DFA), Non-Deterministic Finite Automata (NFA), Pushdown Automata (PDA), and Turing Machines (TM).

---

## Index of Experiments

| Exp # | Model / Topic | Language / Problem Statement | Test Strings / Key Inputs |
| :---: | :---: | :--- | :--- |
| **EXP 1** | DFA | Strings starting with `a` and ending with `a` over $\Sigma = \{a, b\}$ | `a`, `aa`, `aba`, `abba` |
| **EXP 2** | DFA | Strings starting with `0` and ending with `1` over $\Sigma = \{0, 1\}$ | `01`, `001`, `0101` |
| **EXP 3** | CFG | $S \to 0A1, \; A \to 0A \mid 1A \mid \varepsilon$ ($0(0+1)^*1$) | `01`, `001`, `01101` |
| **EXP 4** | CFG | $S \to 0S0 \mid 1S1 \mid 0 \mid 1 \mid \varepsilon$ (Binary Palindromes) | `0`, `1`, `101`, `110011` |
| **EXP 5** | CFG | $S \to 0S0 \mid A, \; A \to 1A \mid \varepsilon$ ($0^n 1^m 0^n$) | `010`, `0011100`, `111` |
| **EXP 6** | CFG | $S \to 0S1 \mid \varepsilon$ ($0^n 1^n$) | `01`, `0011`, `000111` |
| **EXP 7** | CFG | $S \to A101A, \; A \to 0A \mid 1A \mid \varepsilon$ (Contains substring `101`) | `101`, `001011`, `11010` |
| **EXP 8** | NFA | Strings starting with `b` and ending with `a` ($b(a+b)^*a$) | `ba`, `bba`, `baba` |
| **EXP 9** | NFA | Strings starting with `0` and ending with `1` ($0(0+1)^*1$) | `01`, `001`, `0101` |
| **EXP 10** | NFA-$\varepsilon$ | Computation of $\varepsilon$-closure for all states (Interactive DFS) | Arbitrary $\varepsilon$-NFA |
| **EXP 11** | NFA-$\varepsilon$ | Computation of $\varepsilon$-closure using Warshall's Transitive Closure | Chained $\varepsilon$-transition NFA |
| **EXP 12** | DFA | Accept finite language $L = \{\text{"a"}, \text{"ac"}, \text{"bac"}\}$ | `"a"`, `"ac"`, `"bac"` |
| **EXP 13** | PDA | Pushdown Automaton accepting $a^n b^n$ | `"aabb"`, `"ab"`, `"aaabbb"` |
| **EXP 14** | PDA | Pushdown Automaton accepting $a^n b^{2n}$ | `"abb"`, `"aabbbb"` |
| **EXP 15** | TM | Turing Machine accepting $a^n b^n$ | `"aabb"`, `"ab"` |
| **EXP 16** | TM | Turing Machine accepting $a^n b^{2n}$ | `"abb"`, `"aabbbb"` |
| **EXP 17** | TM | Turing Machine accepting Palindrome $w = w^R$ | `"ababa"`, `"abba"` |
| **EXP 18** | TM | Turing Machine accepting language $w w$ | `"abab"`, `"aabbaabb"` |
| **EXP 19** | TM | Unary Addition ($a^m + a^n = a^{m+n}$) | `"aa+aaa"` $\to$ `"aaaaa"` ($2+3=5$) |
| **EXP 20** | TM | Unary Subtraction ($a^m - a^n$) | `"aaa-aa"` $\to$ `"a"` ($3-2=1$) |
| **EXP 21** | DFA | Accept even number of `a`'s over $\Sigma = \{a, b\}$ | `"aa"`, `"baab"`, `""` |
| **EXP 22** | DFA | Accept odd number of `a`'s over $\Sigma = \{a, b\}$ | `"a"`, `"baa"`, `"bab"` |
| **EXP 23** | DFA | Accept strings ending with `ab` over $\{a, b\}$ | $W = \text{"aaabab"}$ |
| **EXP 24** | DFA | Accept strings containing substring `ab` over $\{a, b\}$ | `"aab"`, `"bbab"`, `"ab"` |
| **EXP 25** | DFA | Accept strings starting with `a` or `b` over $\{a, b\}$ | `"a"`, `"b"`, `"aba"` |
| **EXP 26** | TM | Turing Machine accepting Palindrome | $W = \text{"bbabb"}$ |
| **EXP 27** | TM | Turing Machine accepting language $w c w$ | `"aca"`, `"bcab"`, `"abbcabb"` |
| **EXP 28** | DFA | Accept strings ending with `ab` over $\{a, b\}$ | $W = \text{"abbaabab"}$ |
| **EXP 29** | DFA | Accept finite language $L = \{\text{"c"}, \text{"bc"}, \text{"bcaaa"}\}$ | `"c"`, `"bc"`, `"bcaaa"` |
| **EXP 30** | NFA | Accept any number of `a`'s ($a^*$) over $\{a, b\}$ | `""`, `"a"`, `"aaa"` |
| **EXP 31** | PDA | Pushdown Automaton accepting $a^n b^n$ with trace | `"ab"`, `"aabb"`, `"aaabbb"` |
| **EXP 32** | TM | String comparison ($w_1 == w_2$) | $w = \text{"aba aba"}$ |
| **EXP 33** | DFA | Accept strings having substring `abc` over $\{a, b, c\}$ | `"abc"`, `"aabcb"`, `"cabc"` |
| **EXP 34** | DFA | Accept even number of `c`'s over $\{a, b, c\}$ | `"cc"`, `"abcc"`, `"cabc"` |
| **EXP 35** | DFA | Strings where `a`'s always appear tripled: $(b \mid aaa)^*$ | `"aaa"`, `"baaa"`, `"aaabaaa"` |
| **EXP 36** | NFA | Strings starting with `a` and ending with `b` ($a(a+b)^*b$) | $W = \text{"abaab"}$ |
| **EXP 37** | NFA | Strings starting and ending with different symbols | `"ab"`, `"ba"`, `"aab"`, `"bba"` |
| **EXP 38** | NFA | Accept finite language $L = \{\text{"c"}, \text{"bbc"}, \text{"bcaaa"}\}$ | `"c"`, `"bbc"`, `"bcaaa"` |
| **EXP 39** | DFA | Accept strings ending with `abc` over $\{a, b, c\}$ | $W = \text{"abbaababc"}$ |
| **EXP 40** | NFA | Accept any number of `b`'s ($b^*$) over $\{a, b\}$ | `""`, `"b"`, `"bbbb"` |

---

## How to Compile and Run

To compile any experiment using standard `gcc`:
```bash
gcc -x c "EXP 3" -o exp3
./exp3
```

Or on Windows PowerShell / Command Prompt:
```cmd
gcc -x c "EXP 13" -o exp13.exe
.\exp13.exe
```
