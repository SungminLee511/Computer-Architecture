# Computer-Architecture

# Roadmap to Becoming a Systems / Kernel / Low-Level Developer

## Stage 0: Mindset
- [ ] Accept that you're going to learn what 99% of devs never touch
- [ ] Be ready to dive into C, Assembly, OS internals, and hardware-level thinking

## Stage 1: Master C & Systems Thinking
### Books
- [ ] The C Programming Language (K&R)
- [ ] Computer Systems: A Programmer’s Perspective
- [ ] Learn C The Hard Way

### Projects
- [ ] Implement `strlen`, `strcpy`, `malloc`
- [ ] Build your own shell using `fork()`, `exec()`, `wait()`
- [ ] Recreate utilities like `cat`, `ls`, `ps`
- [ ] Write a custom memory allocator using `sbrk()`

## Stage 2: Assembly + CPU Basics
### Resources
- [ ] PC Assembly Language by Paul Carter
- [ ] godbolt.org — compile C, view assembly
- [ ] `objdump`, `gdb`, `readelf` practice

### Concepts
- [ ] Registers: `rax`, `rsp`, `rbp`, etc.
- [ ] Stack frames and function calls
- [ ] Key instructions: `mov`, `call`, `ret`, `jmp`, etc.
- [ ] How C maps to instructions

## Stage 3: OS & Kernel Internals
### Books
- [ ] Operating Systems: Three Easy Pieces (OSTEP)
- [ ] Modern Operating Systems (Tanenbaum)
- [ ] Linux Kernel Development (Robert Love)

### Concepts
- [ ] Virtual memory, paging, page tables
- [ ] System calls and context switching
- [ ] Kernel vs user space
- [ ] Boot process, interrupts, file systems

## Stage 4: Write a Tiny OS
### Resources
- [ ] https://github.com/cfenollosa/os-tutorial
- [ ] https://osdev.org/wiki/Bare_Bones

### Projects
- [ ] Bootloader in x86 assembly (`boot.asm`)
- [ ] Kernel in C that prints to the screen
- [ ] Set up GDT and IDT
- [ ] Keyboard input + interrupts
- [ ] Build and boot with QEMU

## Stage 5: Study Real Operating Systems
### Explore
- [ ] https://github.com/mit-pdos/xv6-public
- [ ] https://github.com/torvalds/linux

### Files to focus on
- [ ] `init/` — Kernel entry point
- [ ] `fs/` — Filesystem code
- [ ] `mm/` — Memory management
- [ ] `kernel/` — Scheduler, syscalls

## Stage 6: Real Projects & Contributions
### Projects
- [ ] Write a Linux kernel module
- [ ] Build your own file system
- [ ] Port Linux to QEMU or Raspberry Pi
- [ ] Contribute to kernelnewbies or open source drivers
- [ ] Build a toy virtual CPU

## Tools to Learn
- [ ] `gcc`, `ld`, `make`
- [ ] `gdb`, `objdump`, `strace`
- [ ] `hexdump`, `xxd`, `readelf`
- [ ] `qemu`, `bochs` (virtual OS testing)
- [ ] `git` + patch-based workflows

## Suggested Weekly Plan
### Week 1–2
- C syntax + pointer practice
- Implement basic string/memory functions

### Week 3–4
- Assembly basics + function call tracing
- Use `objdump` to read compiled C functions

### Week 5–6
- Read OSTEP
- Build your own shell + memory allocator

### Week 7–9
- Follow os-tutorial
- Boot your kernel with QEMU

### Week 10+
- Dive into xv6 + Linux kernel
- Start real projects or contributions
