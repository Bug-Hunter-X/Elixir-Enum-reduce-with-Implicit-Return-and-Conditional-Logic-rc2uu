# Elixir Enum.reduce Bug

This repository demonstrates a subtle but common error in Elixir when using `Enum.reduce` with conditional logic inside the anonymous function. The problem arises from an implicit return value when the conditional statement evaluates to `false`. This can lead to unexpected results, especially when working with more complex logic.

The `bug.exs` file contains the erroneous code, while `bugSolution.exs` provides a corrected version.

## Bug Description

The provided `Enum.reduce` attempts to sum only numbers greater than 3. The error happens because when `x <=3`, the anonymous function doesn't explicitly return a value and this causes `Enum.reduce` to accumulate unexpected results.