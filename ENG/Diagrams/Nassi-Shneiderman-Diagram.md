# Table of Content
- [Table of Content](#table-of-content)
- [Nassi-Shneidermann / Structogram](#nassi-shneidermann--structogram)
  - [Explanation](#explanation)
  - [Diagram Blocks](#diagram-blocks)
    - [Process Symbol](#process-symbol)
    - [Decision Symbol](#decision-symbol)
      - [1. Possible Block](#1-possible-block)
      - [2. Possible Block](#2-possible-block)
      - [Example Nesting](#example-nesting)
      - [Case-Statement](#case-statement)
    - [Loops](#loops)
      - [Iteration Symbol](#iteration-symbol)

# Nassi-Shneidermann / Structogram
[^1]
## Explanation
A Nassi-Shneidermann diagram is a diagram type used to represent program designs within the method of Structured Programming.

Since Nassi-Shneidermann diagrams represent program structures and control structures, they are also referred to as __Structograms__.

## Diagram Blocks
Most of the following structure blocks can be nested within each other. The structogram composed of different structure blocks is rectangular as a whole, just as wide as its widest structure block.

### Process Symbol
[![Process Symbol](https://upload.wikimedia.org/wikipedia/commons/1/1e/LineareAnw.png "Process Symbol")](https://en.wikipedia.org/wiki/Nassi-Shneiderman_diagram#Process_Symbol)

- Each instruction is written in a rectangular structure block.
- The structure blocks are traversed one after the other from top to bottom.
- Empty structure blocks are only allowed in branches.
- Alternative terms: Sequence, Command sequence, Instruction sequence, Instruction block, Linear sequence, Sequence.

### Decision Symbol
Alternative terms: Branching, Alternative, Selection
#### 1. Possible Block

[![Decision Symbol 1](https://upload.wikimedia.org/wikipedia/commons/5/50/EinfAusw.png "Simple Selection")](https://en.wikipedia.org/wiki/Nassi-Shneiderman_diagram#Decision_Symbol)

- Only if the condition is true, the instruction block 1 is executed `(if)`. If the condition is not true, the execution continues without further instruction (exit at the bottom).
- Alternative terms: Conditional processing, Simple selection, Simple branching.

#### 2. Possible Block

[![Decision Symbol 2](https://upload.wikimedia.org/wikipedia/commons/7/73/ZweifAusw.png "Dual Selection")](https://en.wikipedia.org/wiki/Nassi-Shneiderman_diagram#Decision_Symbol)

- If the condition is true, the first instruction block is executed. If the condition is not true, the second instruction block is executed. `(if else)`
- Alternative terms: Simple alternative, Dual selection, Alternative branching/processing.

#### Example Nesting

[![Multiple Selection](https://upload.wikimedia.org/wikipedia/commons/5/5f/MehrfAusw.png "Multiple Selection")](https://en.wikipedia.org/wiki/Nassi-Shneiderman_diagram#Decision_Symbol)

- Nesting is possible in both the yes and no cases.

#### Case-Statement

[![Case-Statement](../../img/Nassi-Shneiderman/NassiShneiderman-case.svg.png "Case-Statement")](https://en.wikipedia.org/wiki/Nassi-Shneiderman_diagram#Decision_Symbol)

- The value of __Variable__ can be conditionally checked for equality as well as for ranges (greater/less for numbers). The corresponding applicable "case" with its associated instruction block is executed (`switch`, `select`).
- Alternative terms: Multiple alternatives, Case selection, Multiple selection, Case, Select.

### Loops

#### Iteration Symbol


[^1]: https://en.wikipedia.org/wiki/Nassi-Shneiderman_diagram
