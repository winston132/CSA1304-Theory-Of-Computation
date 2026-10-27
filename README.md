# CSA1304 - Theory of Computation Lab Experiments

Comprehensive implementation of all 40 laboratory experiments for **CSA1304: Theory of Computation**, including Context-Free Grammars (CFG), Deterministic Finite Automata (DFA), Non-Deterministic Finite Automata (NFA), Pushdown Automata (PDA), and Turing Machines (TM).

---

## Index of Experiments

| Exp # | Model / Topic | Language / Problem Statement | Test Strings / Key Inputs | Output Screenshot |
| :---: | :---: | :--- | :--- | :---: |
| **EXP 1** | DFA | Strings starting with `a` and ending with `a` over $\Sigma = \{a, b\}$ | `a`, `aa`, `aba`, `abba` | [![Output](screenshots/EXP_1.png)](screenshots/EXP_1.png) |
| **EXP 2** | DFA | Strings starting with `0` and ending with `1` over $\Sigma = \{0, 1\}$ | `01`, `001`, `0101` | [![Output](screenshots/EXP_2.png)](screenshots/EXP_2.png) |
| **EXP 3** | CFG | $S \to 0A1, \; A \to 0A \mid 1A \mid \varepsilon$ ($0(0+1)^*1$) | `01`, `001`, `01101` | [![Output](screenshots/EXP_3.png)](screenshots/EXP_3.png) |
| **EXP 4** | CFG | $S \to 0S0 \mid 1S1 \mid 0 \mid 1 \mid \varepsilon$ (Binary Palindromes) | `0`, `1`, `101`, `110011` | [![Output](screenshots/EXP_4.png)](screenshots/EXP_4.png) |
| **EXP 5** | CFG | $S \to 0S0 \mid A, \; A \to 1A \mid \varepsilon$ ($0^n 1^m 0^n$) | `010`, `0011100`, `111` | [![Output](screenshots/EXP_5.png)](screenshots/EXP_5.png) |
| **EXP 6** | CFG | $S \to 0S1 \mid \varepsilon$ ($0^n 1^n$) | `01`, `0011`, `000111` | [![Output](screenshots/EXP_6.png)](screenshots/EXP_6.png) |
| **EXP 7** | CFG | $S \to A101A, \; A \to 0A \mid 1A \mid \varepsilon$ (Contains substring `101`) | `101`, `001011`, `11010` | [![Output](screenshots/EXP_7.png)](screenshots/EXP_7.png) |
| **EXP 8** | NFA | Strings starting with `b` and ending with `a` ($b(a+b)^*a$) | `ba`, `bba`, `baba` | [![Output](screenshots/EXP_8.png)](screenshots/EXP_8.png) |
| **EXP 9** | NFA | Strings starting with `0` and ending with `1` ($0(0+1)^*1$) | `01`, `001`, `0101` | [![Output](screenshots/EXP_9.png)](screenshots/EXP_9.png) |
| **EXP 10** | NFA-$\varepsilon$ | Computation of $\varepsilon$-closure for all states (Interactive DFS) | Arbitrary $\varepsilon$-NFA | [![Output](screenshots/EXP_10.png)](screenshots/EXP_10.png) |
| **EXP 11** | NFA-$\varepsilon$ | Computation of $\varepsilon$-closure using Warshall's Transitive Closure | Chained $\varepsilon$-transition NFA | [![Output](screenshots/EXP_11.png)](screenshots/EXP_11.png) |
| **EXP 12** | DFA | Accept finite language $L = \{\text{"a"}, \text{"ac"}, \text{"bac"}\}$ | `"a"`, `"ac"`, `"bac"` | [![Output](screenshots/EXP_12.png)](screenshots/EXP_12.png) |
| **EXP 13** | PDA | Pushdown Automaton accepting $a^n b^n$ | `"aabb"`, `"ab"`, `"aaabbb"` | [![Output](screenshots/EXP_13.png)](screenshots/EXP_13.png) |
| **EXP 14** | PDA | Pushdown Automaton accepting $a^n b^{2n}$ | `"abb"`, `"aabbbb"` | [![Output](screenshots/EXP_14.png)](screenshots/EXP_14.png) |
| **EXP 15** | TM | Turing Machine accepting $a^n b^n$ | `"aabb"`, `"ab"` | [![Output](screenshots/EXP_15.png)](screenshots/EXP_15.png) |
| **EXP 16** | TM | Turing Machine accepting $a^n b^{2n}$ | `"abb"`, `"aabbbb"` | [![Output](screenshots/EXP_16.png)](screenshots/EXP_16.png) |
| **EXP 17** | TM | Turing Machine accepting Palindrome $w = w^R$ | `"ababa"`, `"abba"` | [![Output](screenshots/EXP_17.png)](screenshots/EXP_17.png) |
| **EXP 18** | TM | Turing Machine accepting language $w w$ | `"abab"`, `"aabbaabb"` | [![Output](screenshots/EXP_18.png)](screenshots/EXP_18.png) |
| **EXP 19** | TM | Unary Addition ($a^m + a^n = a^{m+n}$) | `"aa+aaa"` $\to$ `"aaaaa"` ($2+3=5$) | [![Output](screenshots/EXP_19.png)](screenshots/EXP_19.png) |
| **EXP 20** | TM | Unary Subtraction ($a^m - a^n$) | `"aaa-aa"` $\to$ `"a"` ($3-2=1$) | [![Output](screenshots/EXP_20.png)](screenshots/EXP_20.png) |
| **EXP 21** | DFA | Accept even number of `a`'s over $\Sigma = \{a, b\}$ | `"aa"`, `"baab"`, `""` | [![Output](screenshots/EXP_21.png)](screenshots/EXP_21.png) |
| **EXP 22** | DFA | Accept odd number of `a`'s over $\Sigma = \{a, b\}$ | `"a"`, `"baa"`, `"bab"` | [![Output](screenshots/EXP_22.png)](screenshots/EXP_22.png) |
| **EXP 23** | DFA | Accept strings ending with `ab` over $\{a, b\}$ | $W = \text{"aaabab"}$ | [![Output](screenshots/EXP_23.png)](screenshots/EXP_23.png) |
| **EXP 24** | DFA | Accept strings containing substring `ab` over $\{a, b\}$ | `"aab"`, `"bbab"`, `"ab"` | [![Output](screenshots/EXP_24.png)](screenshots/EXP_24.png) |
| **EXP 25** | DFA | Accept strings starting with `a` or `b` over $\{a, b\}$ | `"a"`, `"b"`, `"aba"` | [![Output](screenshots/EXP_25.png)](screenshots/EXP_25.png) |
| **EXP 26** | TM | Turing Machine accepting Palindrome | $W = \text{"bbabb"}$ | [![Output](screenshots/EXP_26.png)](screenshots/EXP_26.png) |
| **EXP 27** | TM | Turing Machine accepting language $w c w$ | `"aca"`, `"bcab"`, `"abbcabb"` | [![Output](screenshots/EXP_27.png)](screenshots/EXP_27.png) |
| **EXP 28** | DFA | Accept strings ending with `ab` over $\{a, b\}$ | $W = \text{"abbaabab"}$ | [![Output](screenshots/EXP_28.png)](screenshots/EXP_28.png) |
| **EXP 29** | DFA | Accept finite language $L = \{\text{"c"}, \text{"bc"}, \text{"bcaaa"}\}$ | `"c"`, `"bc"`, `"bcaaa"` | [![Output](screenshots/EXP_29.png)](screenshots/EXP_29.png) |
| **EXP 30** | NFA | Accept any number of `a`'s ($a^*$) over $\{a, b\}$ | `""`, `"a"`, `"aaa"` | [![Output](screenshots/EXP_30.png)](screenshots/EXP_30.png) |
| **EXP 31** | PDA | Pushdown Automaton accepting $a^n b^n$ with trace | `"ab"`, `"aabb"`, `"aaabbb"` | [![Output](screenshots/EXP_31.png)](screenshots/EXP_31.png) |
| **EXP 32** | TM | String comparison ($w_1 == w_2$) | $w = \text{"aba aba"}$ | [![Output](screenshots/EXP_32.png)](screenshots/EXP_32.png) |
| **EXP 33** | DFA | Accept strings having substring `abc` over $\{a, b, c\}$ | `"abc"`, `"aabcb"`, `"cabc"` | [![Output](screenshots/EXP_33.png)](screenshots/EXP_33.png) |
| **EXP 34** | DFA | Accept even number of `c`'s over $\{a, b, c\}$ | `"cc"`, `"abcc"`, `"cabc"` | [![Output](screenshots/EXP_34.png)](screenshots/EXP_34.png) |
| **EXP 35** | DFA | Strings where `a`'s always appear tripled: $(b \mid aaa)^*$ | `"aaa"`, `"baaa"`, `"aaabaaa"` | [![Output](screenshots/EXP_35.png)](screenshots/EXP_35.png) |
| **EXP 36** | NFA | Strings starting with `a` and ending with `b` ($a(a+b)^*b$) | $W = \text{"abaab"}$ | [![Output](screenshots/EXP_36.png)](screenshots/EXP_36.png) |
| **EXP 37** | NFA | Strings starting and ending with different symbols | `"ab"`, `"ba"`, `"aab"`, `"bba"` | [![Output](screenshots/EXP_37.png)](screenshots/EXP_37.png) |
| **EXP 38** | NFA | Accept finite language $L = \{\text{"c"}, \text{"bbc"}, \text{"bcaaa"}\}$ | `"c"`, `"bbc"`, `"bcaaa"` | [![Output](screenshots/EXP_38.png)](screenshots/EXP_38.png) |
| **EXP 39** | DFA | Accept strings ending with `abc` over $\{a, b, c\}$ | $W = \text{"abbaababc"}$ | [![Output](screenshots/EXP_39.png)](screenshots/EXP_39.png) |
| **EXP 40** | NFA | Accept any number of `b`'s ($b^*$) over $\{a, b\}$ | `""`, `"b"`, `"bbbb"` | [![Output](screenshots/EXP_40.png)](screenshots/EXP_40.png) |

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