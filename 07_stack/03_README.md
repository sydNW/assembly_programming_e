# 03.asm – Stack and Procedure Calls

The program sets RAX to 10 and calls the `calculate` procedure. The `call` instruction pushes the return address onto the stack.

Inside the procedure:
- `add rax, 5` increases RAX from 10 to 15.
- `ret` pops the return address and returns execution to `after_call`.

The program then exits using the exit system call.

 Stack Changes

 Instruction      RSP 
 Initial           S 
 call calculate   S - 8 
 ret               S 

 Observations

I observed that call decreases RSP by 8 bytes because it pushes the return address onto the stack. The ret instruction increases RSP by 8 bytes by removing the return address. RAX contains 15 after the procedure returns.
