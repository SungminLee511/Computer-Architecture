# The Ultimate Roadmap to Becoming a Systems / Kernel / Low-Level Developer

---

## Pre‑Stage: Prerequisites & Environment
- [ ] Set up a Linux distro (Ubuntu, Fedora, Arch) as primary or VM
- [ ] Learn basic shell (`bash`/`zsh`): navigation, pipes, redirection, scripting
- [ ] Master Git: cloning, branching, commits, rebasing, patch workflows
- [ ] Install core toolchain: `gcc`/`clang`, `make`/`ninja`, `gdb`, `qemu`, `bochs`
### Extra Books
- [ ] *The Linux Command Line* by William Shotts
- [ ] *Pro Git* by Scott Chacon & Ben Straub
### Extra Projects
- [ ] Write a custom `Makefile` with separate debug/release targets
- [ ] Automate a full toolchain install script for your distro

---

## Stage 0: Mindset
- [ ] Accept that you're going to learn what 99% of devs never touch
- [ ] Embrace patience: low‑level bugs can take days to root‑cause
- [ ] Adopt a systems‑thinking approach: hardware ↔ software interplay
### Extra Reads
- [ ] *The Practice of Programming* by Kernighan & Pike
- [ ] *Debugging* by David Agans
### Extra Exercises
- [ ] Review difficult bugs in your journal and write post-mortem notes
- [ ] Pair-program a challenging debugging session with a peer

---

## Stage 1: Linux & Toolchain Fluency
### Topics
- [ ] Filesystem layout (`/proc`, `/sys`, `/dev`)
- [ ] Package management (`apt`, `dnf`, `pacman`)
- [ ] Permissions, users/groups, capabilities
- [ ] Building from source: `./configure && make && make install`
- [ ] CI basics: Travis, GitHub Actions for C projects
### Mini‑Projects
- [ ] Bash script to automate compiling & testing a C program
- [ ] Dockerize a "Hello, world" C server
### Extra Projects
- [ ] GitLab CI pipeline that QEMU-tests your kernel
- [ ] Build a `.deb` or `.rpm` package for your C utility

---

## Stage 2: Master C & Systems Thinking
### Books
- [ ] **The C Programming Language** (K&R)
- [ ] **Computer Systems: A Programmer’s Perspective**
- [ ] **Learn C The Hard Way**
- [ ] *Expert C Programming: Deep C Secrets* (optional)
### Projects
- [ ] Reimplement `strlen`, `strcpy`, `malloc`
- [ ] Build a shell with `fork()`, `exec()`, `wait()`
- [ ] Clone `cat`, `ls`, `ps` from scratch
- [ ] Implement a mark-and-sweep garbage collector
- [ ] Build & benchmark your own arena allocator
### Challenge
- [ ] Implement a type-aware `printf()` clone

---

## Stage 3: Assembly & CPU Architecture
### Resources
- [ ] **PC Assembly Language** by Paul Carter
- [ ] godbolt.org – C to asm
- [ ] Intel/AMD manuals (optional)
### Concepts
- [ ] Registers (`rax`, `rbp`, `rsp`, etc.)
- [ ] Stack frames, SysV ABI
- [ ] Instructions: `mov`, `call`, `jmp`, `cmp`
### Exercises
- [ ] Write simple NASM functions, call from C
- [ ] Trace a C function in `gdb` (asm ↔ source)
### Extra Projects
- [ ] Write a JIT that emits runtime machine code
- [ ] Build a toy bytecode interpreter

---

## Stage 4: OS Internals Fundamentals
### Books
- [ ] **Operating Systems: Three Easy Pieces (OSTEP)**
- [ ] **Modern Operating Systems** (Tanenbaum)
- [ ] **Linux Kernel Development** (Robert Love)
### Concepts
- [ ] Processes, threads, scheduling
- [ ] Virtual memory, paging
- [ ] System calls, context switching, interrupts
- [ ] File systems, concurrency, spinlocks, RCU
### Extra Projects
- [ ] Modify Linux scheduler to add a new policy
- [ ] Build a journaling FS using FUSE

---

## Stage 5: Tiny OS Development
### Resources
- [ ] https://osdev.org/wiki/Bare_Bones
- [ ] https://github.com/cfenollosa/os-tutorial
### Projects
- [ ] x86 bootloader (`boot.asm`)
- [ ] C kernel that prints to screen
- [ ] Set up GDT & IDT
- [ ] Implement keyboard IRQ handler
- [ ] Add round-robin scheduler
- [ ] QEMU test with `-s -S` for KGDB
### Extra Projects
- [ ] Add shell + timer to your kernel

---

## Stage 6: Real OS Exploration
### Codebases
- [ ] [xv6](https://github.com/mit-pdos/xv6-public)
- [ ] [Linux](https://github.com/torvalds/linux)
- [ ] MINIX 3
### Focus Areas
- [ ] `init/`, `kernel/`, `mm/`, `fs/`, `drivers/`
### Extra Projects
- [ ] Backport a small xv6 feature
- [ ] Benchmark Linux slab allocator

---

## Stage 7: Kernel Modules & Drivers
### Projects
- [ ] Write a Hello World LKM
- [ ] Implement a char device driver
- [ ] FUSE file system
- [ ] Explore in-kernel Rust
### Extra Projects
- [ ] PCI driver that lists devices
- [ ] Debugfs-based control panel

---

## Stage 8: Debugging & Tracing
### Tools
- [ ] `gdb`, `kgdb`, `perf`, `ftrace`, `SystemTap`
- [ ] `valgrind`, `kmemleak`, `kunit`
### Exercises
- [ ] Profile your tiny OS
- [ ] Trace a syscall with `ftrace`
- [ ] Automate QEMU boot + test scripts

---

## Stage 9: Security & RE
### Topics
- [ ] Stack canaries, ASLR, NX, ROP
- [ ] Reverse engineering tools: `objdump`, Ghidra
### Projects
- [ ] Harden a module with stack protector
- [ ] Write a syscall sandbox with `seccomp`

---

## Stage 10: Virtualization & Containers
### Topics
- [ ] KVM, QEMU, Xen
- [ ] Namespaces, cgroups
### Projects
- [ ] Build a KVM user-space hypervisor
- [ ] OCI-compliant container runtime

---

## Stage 11: Embedded & RTOS
### Platforms
- [ ] ARM Cortex-M, RISC-V
### Projects
- [ ] Blink LED in FreeRTOS
- [ ] Port tiny OS to QEMU ARM
### Extra Projects
- [ ] FatFS integration
- [ ] Context switch latency benchmark

---

## Stage 12: Advanced Topics
### Topics
- [ ] DPDK, PMEM, seL4, PREEMPT_RT
### Extra Projects
- [ ] Userspace DPDK network stack
- [ ] TLA+ kernel model

---

## Suggested Timeline
- Months 1–2: Linux, C, memory functions
- Months 3–4: Assembly, disassembly, `gdb`
- Months 5–6: OSTEP, build shell, allocator
- Months 7–9: Tiny OS, QEMU/`kgdb` debugging
- Months 10–12: Linux/xv6, LKMs
- Year 2+: Specialize — security, RTOS, drivers, verification

> ✅ Pro Tip: Regularly contribute patches to Linux or xv6 — feedback from maintainers = rocket fuel for growth!
