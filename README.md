# VHDL Signal Assignment Race Condition
This repository demonstrates a common error in VHDL: a race condition arising from improper signal assignments within a clocked process.  The original code exhibits flawed signal handling which could lead to unpredictable behavior. The solution illustrates a more robust and reliable approach to managing signal updates in a clocked process.  The focus is on preventing race conditions and ensuring data integrity.

## Original Code (bug.vhdl)
The original VHDL code contains a potential race condition. The simultaneous assignment of `internal_data` and `data_out` in the same `rising_edge` process might lead to inconsistencies. 

## Solution (bugSolution.vhdl)
The improved code separates the signal assignments to prevent the race condition.  This ensures that `data_out` is assigned the updated value of `internal_data` in the correct clock cycle, making the logic predictable and reliable.