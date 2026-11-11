# 01.asm – Basic Stack Operations

The program loads 100 into RAX and 200 into RBX.

- `push rax` places 100 onto the stack and decreases RSP by 8 bytes.
- `push rbx` places 200 on top of the stack and decreases RSP by another 8 bytes.
- `pop rcx` removes 200 and stores it in RCX.
- `pop rdx` removes 100 and stores it in RDX.
- The program then exits using the exit system call.

 Stack Changes

 Instruction  RSP 

 Initial      S 
 push rax   S - 8
 push rbx   S - 16 
 pop rcx    S - 8 
 pop rdx    S 

 Observations

I observed that the stack follows the Last In, First Out (LIFO) principle. The last value pushed is the first one popped. RSP returns to its original position after both values are removed.
