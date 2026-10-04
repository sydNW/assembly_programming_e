# DIV - Arithmetic Flags

## Programs Tested

### div1
Operation:

`100 ÷ 7 = 14 remainder 2`

Result:

- Quotient = `14`
- Remainder = `2`

### EFLAGS

- **CF:** Undefined
- **PF:** Undefined
- **AF:** Undefined
- **ZF:** Undefined
- **SF:** Undefined
- **OF:** Undefined

The `DIV` instruction does not define these arithmetic flags. Therefore, the values displayed by GDB after division cannot be used to determine whether the division produced a particular flag state.

### div3
Operation:

`300,000,000 ÷ 1,000 = 300,000 remainder 0`

Result:

- Quotient = `300,000`
- Remainder = `0`

### EFLAGS

- **CF:** Undefined
- **PF:** Undefined
- **AF:** Undefined
- **ZF:** Undefined
- **SF:** Undefined
- **OF:** Undefined

Like `div1`, `DIV` does not define the arithmetic flags. The quotient and remainder are stored in the appropriate registers, but the arithmetic EFLAGS should not be interpreted from the values shown by GDB.
