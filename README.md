# addition-and-subtraction-of-bfloat-16
This is a verilog project that adds or subtracts two bfloat-16 numbers. This is made to be implemented on FPGA basys3 board.

Code includes

MAIN module
It manages the sign bit for subtraction by changing the sign of second bit. Breaks down the operands as exponent and mantessa. It also detects special cases (zero, exception), and coordinates execution.

COMPARE AND SHIFT module
Aligns the mantissas by comparing exponents. It shifts the mantissa of the operand with the smaller exponent so that both operands can be added/subtracted correctly.

ADDITION module
Performs addition by considering the sign. If sign is negative then its 2's compliment is used in addition, so output is a 2's complement result.

NORMALISATION module
Converts the mantissa result back to normalized  loating-point format by adjusting the exponent and aligning the result to maintain leading 1 format.

Features and Enhancements
 1.Handles special cases like zero detection. 
 2.Input-triggered computation using edge-detection on buttons.
 3.Switches are used so that any input of our wish can be given, and these are stored in reg for use. 
 4.Two's compliments are used, so we can perform both addition and subtraction using the same modules, with just a sign change.

To be implemented on FPGA board, include topmodule and constraints in vivado for Basys3 board.
