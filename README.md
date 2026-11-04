# TCS Self-Learning Assignment — JFLAP Automata Practical

## Student Details

| Field | Details |
| --- | --- |
| **Name** | Pranav Kule |
| **Roll Number** | 22 |
| **Class** | D12C |
| **Subject** | Theory of Computer Science |
| **Subject Code** | 26CMPC51 |
| **Academic Year** | 2026–2027 |

---

## Introduction

This repository contains the JFLAP files for the **Theory of Computer Science
Self-Learning Assignment**. It covers finite automata, regular languages,
conversion algorithms, and finite-state machines with output.

Each experiment is provided as a real **JFLAP `.jff` file** that can be opened
directly in JFLAP. The automata are complete, use the language definitions from
the practical report, and include correctly placed states, transitions, initial
states, and final states.

---

## Objectives

- Understand the working of deterministic and nondeterministic finite automata.
- Apply the subset construction to convert an NFA into an equivalent DFA.
- Minimize a DFA by removing unreachable states and merging equivalent states.
- Convert a DFA into a regular grammar and a regular expression.
- Construct automata for language operations, including intersection.
- Convert a regular expression into a DFA.
- Model finite-state machines with output using Mealy and Moore machines.
- Gain practical experience with JFLAP as an automata-theory tool.

---

## Software Requirements

| Requirement | Details |
| --- | --- |
| **JFLAP** | JFLAP 7.1 or newer (also compatible with JFLAP 6.4+ file format) |
| **Java** | Java 8 or newer |
| **Operating System** | Windows, Linux, or macOS |
| **Additional Libraries** | None |

---

## Downloading and Installing JFLAP

1. Open the official JFLAP website: <https://www.jflap.org/>.
2. Go to the **Download** section and download the JFLAP archive.
3. Install Java if it is not already available on the system.
4. Extract the downloaded archive and locate `JFLAP.jar`.
5. Start JFLAP by double-clicking `JFLAP.jar`, or run:

   ```bash
   java -jar JFLAP.jar
   ```

6. Verify that the JFLAP main menu appears.

---

## List of Experiments

All `.jff` filenames follow the faculty-prescribed format:
`Roll_No._Name_Topic_DOP.jff` with DOP `05-11-2026`.

| No. | Experiment | File(s) | Brief Description |
| --- | --- | --- | --- |
| 1 | **Deterministic Finite Automata (DFA)** | `JFLAP_Files/22_Pranav_Kule_DFA_05-11-2026.jff` | DFA over `{a, b, c}` that accepts strings beginning **and** ending with `c`. |
| 2 | **Nondeterministic Finite Automata (NFA)** | `JFLAP_Files/22_Pranav_Kule_NFA_05-11-2026.jff` | NFA over `{a, b}` that accepts strings ending in `aa`, using an ε-transition for concatenation. |
| 3 | **NFA to DFA Conversion** | `JFLAP_Files/22_Pranav_Kule_NFA_to_DFA_05-11-2026.jff` | Subset construction for the practical's worked example: strings ending in `ab`. Resulting DFA states are `A = {q0}`, `B = {q0, q1}`, and `C = {q0, q2}`. |
| 4 | **DFA Minimization** | `JFLAP_Files/22_Pranav_Kule_DFA_Minimization_05-11-2026.jff` and `JFLAP_Files/22_Pranav_Kule_DFA_Minimized_05-11-2026.jff` | Original five-state DFA and its minimized two-state equivalent. Minimization removes unreachable state `q4` and merges `{q0, q1}` into `P` and `{q2, q3}` into `Q`. The language is strings ending in `b`. |
| 5 | **DFA to Regular Grammar** | `JFLAP_Files/22_Pranav_Kule_DFA_to_Regular_Grammar_05-11-2026.jff` | Right-linear grammar for the DFA accepting strings ending in `ab`: `A → aB \| bA`, `B → aB \| bC`, `C → aB \| bA \| ε`. |
| 6 | **DFA to Regular Expression** | `JFLAP_Files/22_Pranav_Kule_DFA_to_Regular_Expression_05-11-2026.jff` | JFLAP regular-expression file for the DFA accepting strings ending in `ab`. The expression is `(a+b)*ab` in JFLAP syntax, which is `(a\|b)*ab` in standard notation. |
| 7 | **Combining Automata** | `JFLAP_Files/07_Combining_Automata/22_Pranav_Kule_Odd_A_05-11-2026.jff`, `22_Pranav_Kule_No_AB_05-11-2026.jff`, and `22_Pranav_Kule_Combined_Automata_05-11-2026.jff` | DFA for an odd number of `a`s, DFA for strings with no `ab` substring, and their product automaton for **intersection**. |
| 8 | **Regular Expression to DFA** | `JFLAP_Files/22_Pranav_Kule_Regular_Expression_to_DFA_05-11-2026.jff` | Subset-construction DFA for `(a\|b)*ab`. The four-state DFA can be minimized by merging equivalent states `A` and `D`, producing the standard three-state DFA. |
| 9 | **Mealy Machine** | `JFLAP_Files/22_Pranav_Kule_Mealy_Machine_05-11-2026.jff` | Mealy machine over `{a, b}` that outputs `1` whenever the symbol just read completes the substring `ab`, and `0` otherwise. For input `aab`, the output is `001`. |
| 10 | **Moore Machine** | `JFLAP_Files/22_Pranav_Kule_Moore_Machine_05-11-2026.jff` | Moore machine over `{a, b}` that outputs `1` when the last two symbols read are `ab`, and `0` otherwise. For input `aab`, the output is `0001`; dropping the start-state output gives `001`. |

---

## Folder Structure

```text
TCS-Self-Learning-JFLAP/
│
├── README.md
├── TCS_JFLAP_Practical.pdf
│
└── JFLAP_Files/
    ├── 22_Pranav_Kule_DFA_05-11-2026.jff
    ├── 22_Pranav_Kule_NFA_05-11-2026.jff
    ├── 22_Pranav_Kule_NFA_to_DFA_05-11-2026.jff
    ├── 22_Pranav_Kule_DFA_Minimization_05-11-2026.jff
    ├── 22_Pranav_Kule_DFA_Minimized_05-11-2026.jff
    ├── 22_Pranav_Kule_DFA_to_Regular_Grammar_05-11-2026.jff
    ├── 22_Pranav_Kule_DFA_to_Regular_Expression_05-11-2026.jff
    ├── 07_Combining_Automata/
    │   ├── 22_Pranav_Kule_Odd_A_05-11-2026.jff
    │   ├── 22_Pranav_Kule_No_AB_05-11-2026.jff
    │   └── 22_Pranav_Kule_Combined_Automata_05-11-2026.jff
    ├── 22_Pranav_Kule_Regular_Expression_to_DFA_05-11-2026.jff
    ├── 22_Pranav_Kule_Mealy_Machine_05-11-2026.jff
    └── 22_Pranav_Kule_Moore_Machine_05-11-2026.jff
```

---

## Opening `.jff` Files in JFLAP

1. Start JFLAP.
2. Select **File → Open**.
3. Choose the required `.jff` file from the `JFLAP_Files` folder.
4. The automaton, grammar, or regular expression opens in the appropriate
   JFLAP editor.

### Experiment-Specific Instructions

- **DFA / NFA (Experiments 1 and 2):** Use **Input → Multiple Run** to test
  several strings at once. For the NFA, **Input → Step with Closure** shows the
  ε-closure and all possible computation paths.
- **NFA to DFA (Experiment 3):** The file contains the resulting DFA. Compare
  its transition table with the subset-construction table in the practical.
- **DFA Minimization (Experiment 4):** Open
  `22_Pranav_Kule_DFA_Minimization_05-11-2026.jff` and select
  **Convert → Minimize DFA** to obtain the minimal DFA. Open
  `22_Pranav_Kule_DFA_Minimized_05-11-2026.jff` to view the minimized result
  directly.
- **Regular Grammar (Experiment 5):** Use **Input → Brute Force Parse** and
  enter a string such as `aab`. The derivation is displayed step by step.
- **Regular Expression (Experiment 6):** Open the file and use
  **Convert → Convert to NFA** to obtain an equivalent automaton. JFLAP uses
  `+` for union, so the expression is written as `(a+b)*ab` rather than
  `(a|b)*ab`.
- **Combining Automata (Experiment 7):** Open
  `22_Pranav_Kule_Combined_Automata_05-11-2026.jff` to view the intersection
  directly. The two component DFAs are also provided separately.
- **Regular Expression to DFA (Experiment 8):** Test strings such as `ab`,
  `aab`, `bab`, and `aba` using **Input → Multiple Run**.
- **Mealy / Moore Machines (Experiments 9 and 10):** Use **Input → Step** or
  **Input → Multiple Run**. JFLAP displays the produced output on a separate
  output tape.

---

## Verification Notes

- All `.jff` files are valid JFLAP XML files and were parsed successfully by
  JFLAP's automaton, grammar, and regular-expression readers.
- Every automaton was checked against representative accepted and rejected
  strings.
- The combined automaton in Experiment 7 is the product intersection: it accepts
  exactly those strings that have an **odd number of `a`s** and **no `ab`
  substring**.
- `22_Pranav_Kule_DFA_Minimization_05-11-2026.jff` intentionally includes
  unreachable state `q4` so that the minimization step can demonstrate its
  removal.
- Experiment 3 follows the subset-construction example worked in the practical
  report (strings ending in `ab`). Experiment 2 separately defines the NFA for
  strings ending in `aa`, as specified in the report.
- Experiment 6 uses the mathematically correct equivalent expression `(a+b)*ab`
  in JFLAP syntax for the language of strings ending in `ab`.
- No test-case files, implementation code, screenshots, or additional
  documentation files are included.
