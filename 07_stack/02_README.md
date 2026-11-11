# 02.asm – Stack Frames

The program calls the work procedure using call work, which pushes the return address onto the stack.

Inside the procedure:
- push rbp saves the previous base pointer.
- mov rbp, rsp creates a new stack frame.
- sub rsp, 16 reserves 16 bytes for local variables.
- The values 100 and 200 are stored at [rbp-8] and [rbp-16].
- The values are loaded into RAX and RBX.

Before returning, mov rsp, rbp releases the reserved space, pop rbp restores the previous base pointer, and ret returns to the main program.

 Stack Changes

  Instruction    RSP 

 Initial          S 
 call work      S - 8 
 push rbp       S - 16 
 sub rsp, 16    S - 32 
 mov rsp, rbp   S - 16 
 pop rbp        S - 8 
 ret               S 

 Observations

I observed that RSP decreases when space is allocated and increases when it is released.
 The program uses RBP to access local variables and restores the stack before returning
