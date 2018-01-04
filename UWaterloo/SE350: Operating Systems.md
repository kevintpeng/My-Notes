# Operating Systems
- [learn](https://learn.uwaterloo.ca/d2l/le/content/372772/Home)
### Summary
OS provides abstraction
- often a cost vs. complexity tradeoff

### [Overview](https://learn.uwaterloo.ca/d2l/le/content/372772/viewContent/2065318/View)
- OS is an abstraction the enbles the use of hardware
- CPUs, Memory, I/O modules, timers, interrupt controller, system bus
- Processing Unit has
  - **Memory Address Register (MAR)** address for read/write
  - **Memory Buffer Register** (MBR) contains data 
  - I/O address + buffer registers

User-visible registers (1 to 64 depending on architecture)
- compilers control them
- **data registers** store data
- **address register** points to memory 
- invisible registers
  - program counter cannot be directly modified by the user
  - Instruction register is invisible (the instruction itself)
  - Program status word contains status information, like coditions, exit codes, flags

### Interupts for Peripherals (ISRs)
- non blocking solution 
- processor checks for interrupt, store snapshot on stack and execute interrupt handler
  - simple model just disables interrupts while running a handler
- lean ISR vs heavy ISR gives you control of what state need be preserved (lean specifies registers to preserve)