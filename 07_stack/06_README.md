# 06.asm – 32-bit Stack Operations

The program loads two values into EAX and EBX.

- `push eax` places the first value onto the stack and decreases ESP by 4 bytes.
- `push ebx` places the second value on top of the stack and decreases ESP by another 4 bytes.
- `pop ebx` removes the top value and restores it into EBX.
- `pop eax` removes the next value and restores it into EAX.
- The program then exits using the 32-bit exit system call.

 Stack Changes

 Instruction  ESP 
 Initial   S 
 push eax  S - 4 
 push ebx  S - 8 
 pop ebx   S - 4 
 pop eax   S 

Observations

I observed that the stack follows the Last In, First Out (LIFO) principle. The last value pushed is the first one popped. ESP returns to its original position after both values are removed.
