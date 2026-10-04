# SUB - Arithmetic Flags

## Programs Tested

### sub1
Operation:

`50 - 80 = -30`

Result: `-30`

### EFLAGS

- **CF (Carry Flag): Set** - The subtraction required a borrow because 50 is smaller than 80.
- **PF (Parity Flag): Set** - The least significant byte of the result has an even number of 1 bits.
- **AF (Auxiliary Carry Flag): Cleared** - There was no borrow from bit 4.
- **ZF (Zero Flag): Cleared** - The result is not zero.
- **SF (Sign Flag): Set** - The result is negative, so the sign bit is 1.
- **OF (Overflow Flag): Cleared** - The result is within the signed range, so signed overflow did not occur.

### sub2
Operation:

`1000 - 2000 = -1000`

Result: `-1000`

### EFLAGS

- **CF (Carry Flag): Set** - A borrow was required because 1000 is smaller than 2000.
- **PF (Parity Flag): Set** - The least significant byte of the result has an even number of 1 bits.
- **AF (Auxiliary Carry Flag): Cleared** - There was no borrow from bit 4.
- **ZF (Zero Flag): Cleared** - The result is not zero.
- **SF (Sign Flag): Set** - The result is negative.
- **OF (Overflow Flag): Cleared** - -1000 is within the signed 16-bit range.
