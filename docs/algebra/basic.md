# Basic Algebra

`Basic Algebra` teaches you how to find unknowns and balance equations.

In machine learning, these concepts govern how optimization loops adjust parameters

<br/>

## Equations and Variables

`Concept`: A variable (like (x) or (y)) is a placeholder for a number. An equation states that two expressions are equal.

`The Rule`: Whatever operation you do to one side of the equation, you must do to the other side to keep it balanced.

`Example`:
    - Find `x` in `3x + 5 = 11`
    - Subtract `5` from both sides: `3x = 6`
    - Divide both sides by `3: x = 2`

`ML Application`: This is exactly how we rearrange equations to solve for model weights analytically (e.g., normal equations in linear regression).

<br/>

## Functions and Graphs

`Concept`: A function f(x) takes an input x, applies a rule, and delivers one output.

`Linear Function`: `y = mx + b`

- `m` is the slope (how steep the line is).
- `b` is the y-intercept (where the line crosses the vertical axis).

`ML Application`: This is the literal architecture of a single neuron.

In ML terms, we rewrite it as `y = wx + b`, where `w` is the weight (slope) and b is the bias (intercept).
