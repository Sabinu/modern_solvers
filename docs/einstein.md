## Overview

A [SAT Solver](https://en.wikipedia.org/wiki/Boolean_satisfiability_problem) is tool for finding solutions to problems that can be specified using [propositional logic formulas](https://en.wikipedia.org/wiki/Propositional_calculus).

Here’s an [example from Delmar E. Searls](http://dsearls.org/courses/M120Concepts/ClassNotes/Logic/130A_examples.htm).

Start with a problem statement, “If the tire is flat then I will have to remove it and take it to the gas station.”

Translate each basic statement to a variable so that P means “the tire is flat”, Q means “I have to remove the tire”, and R means “I have to take the tire to the gas station.

Next, write the statement in symbolic form: P → (Q ∧ R) and make a truth table that shows when the statements is satisfied:

| P   | Q   | R   | P → (Q ∧ R) |
| --- | --- | --- | ----------- |
| T   | T   | T   | T           |
| T   | T   | F   | F           |
| T   | F   | T   | F           |
| T   | F   | F   | F           |
| F   | T   | T   | T           |
| F   | T   | F   | T           |
| F   | F   | T   | T           |
| F   | F   | F   | T           |

Since there is at least one row that evaluates to `True`, we say the expression is _satisfiable_.

What a SAT solver does is determine whether an expression is _satisfiable_ and will generate one, some, or all of the rows that evaluate to true.

## Why Do We Care?

There are many otherwise difficult problems that can be expressed in propositional logic and computers have gotten good at solving them.

While the above example was simple, the problem grows exponentially with the number of variables. The amazing fact of the early 21st century is that a number of heuristics have been found that make the problem tractable for many practical examples, even ones with tens of thousands of variables.

One example is finding a layout to wire a printed circuit board in a way that doesn’t generate electrical interference.

## Tools
