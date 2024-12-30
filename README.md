# VHDL Counter Overflow Bug

This repository demonstrates a common error in VHDL code: an incorrect handling of counter overflow. The `buggy_counter.vhd` file contains a counter that does not properly transition from its maximum value back to 0, causing unexpected behavior. The `fixed_counter.vhd` file provides a corrected version that addresses this issue.

## Bug Description
The `buggy_counter` entity in `buggy_counter.vhd` is intended to count from 0 to 15 and then wrap around to 0. However, the current implementation has a flaw in the way it handles the transition from 15 to 0. This results in an incorrect count value or potential simulation failures.

## Bug Solution
The `fixed_counter.vhd` file presents a corrected version of the counter.  It correctly handles the transition from 15 to 0 using a modulo operation. This ensures a seamless and accurate count sequence. 

## How to Reproduce
1. Simulate the `buggy_counter.vhd` file. Observe the unexpected behavior when the counter reaches 15.
2. Simulate `fixed_counter.vhd`. Verify that the counter correctly wraps around from 15 to 0.