# MUL - Arithmetic Flags

## Programs Tested

### mul1
Operation:

`25 × 10 = 250`

Result: `250`

### EFLAGS

- **CF (Carry Flag): Cleared** - The upper half of the multiplication result is zero, so the result fits in the lower half.
- **OF (Overflow Flag): Cleared** - The multiplication did not require the upper half to represent the result.
- **PF, AF, ZF, SF:** Undefined - The `MUL` instruction does not define these flags, so their displayed GDB values cannot be interpreted as results of the multiplication.

### mul2
Operation:

`3000 × 200 = 600000`

Result: `600000`

### EFLAGS

- **CF (Carry Flag): Set** - The result is too large to fit in the lower half of the destination register, so the upper half is non-zero.
- **OF (Overflow Flag): Set** - The multiplication produced a result requiring the upper half of the destination.
- **PF, AF, ZF, SF:** Undefined - These flags are not defined by the `MUL` instruction.
