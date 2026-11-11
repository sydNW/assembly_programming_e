# 05.asm 

The program loads two values into RAX and RBX.

- `push rax` places the first value onto the stack and decreases RSP by 8 bytes.
- `push rbx` places the second value on top of the stack and decreases RSP by another 8 bytes.
- `pop rbx` removes the top value and restores it into RBX.
- `pop rax` removes the next value and restores it into RAX.
- The program then exits using the exit system call.

 Stack Changes
 Instruction      RSP 

 Initial    S 
 push rax  S - 8 
 push rbx  S - 16 
 pop rbx  S - 8 
 pop rax  S 

 Observations

I observed that the stack follows the Last In, First Out (LIFO) principle. The last value pushed is the first one popped. RSP returns to its original position after both values are removed.
