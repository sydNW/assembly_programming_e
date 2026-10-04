# ADD - Arithmetic Flags

## Programs Tested

### add1
Operation:

`120 + 10 = 130`

Result: `130`

### EFLAGS

- **CF (Carry Flag): Cleared** - There was no unsigned carry out of the most significant bit.
- **PF (Parity Flag): Set** - The least significant byte of 130 is `0x82`, which has an even number of 1 bits.
- **AF (Auxiliary Carry Flag): Set** - There was a carry from the lower 4 bits during the addition.
- **ZF (Zero Flag): Cleared** - The result is 130, not zero.
- **SF (Sign Flag): Set** - The most significant bit of the 8-bit result `0x82` is 1, indicating a negative signed value in 8-bit representation.
- **OF (Overflow Flag): Set** - The positive operands produced a result that cannot be represented as a positive signed 8-bit value.

### add2
Operation:

`32000 + 500 = 32500`

Result: `32500`

### EFLAGS

- **CF (Carry Flag): Cleared** - There was no unsigned carry out of the most significant bit.
- **PF (Parity Flag): Cleared** - The least significant byte of the result does not contain an even number of 1 bits.
- **AF (Auxiliary Carry Flag): Cleared** - There was no carry from bit 3 to bit 4.
- **ZF (Zero Flag): Cleared** - The result is not zero.
- **SF (Sign Flag): Cleared** - The result is positive and its sign bit is 0.
- **OF (Overflow Flag): Cleared** - 32500 is within the signed 16-bit range, so signed overflow did not occur.
