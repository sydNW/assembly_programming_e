# 04.asm – 32-bit Stack Frames

The program calls the `work` procedure using `call work`, which pushes the return address onto the stack.

Inside the procedure:
- `push ebp` saves the previous base pointer.
- `mov ebp, esp` creates a new stack frame.
- `sub esp, 8` reserves 8 bytes for local variables.
- The values 100 and 200 are stored at `[ebp-4]` and `[ebp-8]`.
- The values are loaded into EAX and EBX.

Before returning, `mov esp, ebp` releases the reserved space, `pop ebp` restores the previous base pointer, and `ret` returns to the main program.

 Stack Changes

 Instruction | ESP
 Initial          S 
 call work     S - 4 
 push ebp      S - 8 
 sub esp, 8    S - 16 
 mov esp, ebp  S - 8 
 pop ebp       S - 4 
 ret           S 

   Observations

I observed that ESP decreases when values are pushed or space is allocated and increases when the stack is restored. The program uses EBP to access local variables and successfully returns to the main program.
