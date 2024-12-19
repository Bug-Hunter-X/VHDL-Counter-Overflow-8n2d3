# VHDL Counter Overflow Bug
This repository demonstrates a common error in VHDL: counter overflow. The `counter.vhdl` file contains a simple counter that increments on each clock edge. However, it lacks proper handling of the maximum count value, potentially leading to unexpected behavior.

The solution, provided in `counter_fixed.vhdl`, addresses this issue by incorporating a check to prevent overflow.

## How to Reproduce
1. Compile and simulate `counter.vhdl`. Observe that the counter wraps around from 15 to 0.
2. Compile and simulate `counter_fixed.vhdl`. Observe that the counter stops incrementing at 15.

## Solutions
The solution file demonstrates how to resolve the overflow by adding a conditional statement to stop the counter's incrementation once the max value is reached.