# Computer Architecture

# The Ultimate Roadmap to Becoming a Systems / Kernel / Low-Level Developer

## Pre‑Stage: Prerequisites & Environment
- [x] Set up a Linux distro (Ubuntu, Fedora, Arch) as primary or VM
- [x] Learn basic shell (`bash`/`zsh`): navigation, pipes, redirection, scripting
- [x] Master Git: cloning, branching, commits, rebasing, patch workflows
- [ ] Install core toolchain: `gcc`/`clang`, `make`/`ninja`, `gdb`, `qemu`, `bochs`

## Stage 0: Mindset
- [x] Embrace patience: low‑level bugs can take days to root‑cause
- [ ] Adopt a systems‑thinking approach: hardware ↔ software interplay
- [x] Accept that you're going to learn what 99% of devs never touch

## Stage 1: Linux & Toolchain Fluency
### Topics
- [ ] Filesystem layout (`/proc`, `/sys`, `/dev`)
- [ ] Package management (`apt`, `dnf`, `pacman`)
- [ ] Permissions, users/groups, capabilities
- [ ] Building from source: `./configure && make && make install`
- [ ] CI basics: setting up Travis/Circle/GitHub Actions for C projects

### Mini‑Projects
- [ ] Write a Bash script to automate compiling and testing a C program
- [ ] Containerize a “Hello, world” web server with Docker

## Stage 2: Master C & Systems Thinking
### Books
- [ ] **The C Programming Language** (K&R)
- [ ] **Computer Systems: A Programmer’s Perspective**
- [ ] **Learn C The Hard Way**
- [ ] *Optional:* Expert C Programming: Deep C Secrets

### Projects
- [ ] Reimplement `strlen`, `strcpy`, `malloc`
- [ ] Build a shell with `fork()`, `exec()`, `wait()`
- [ ] Clone `cat`, `ls`, `ps` from scratch
- [ ] Static analysis: run `clang‑tidy`, `cppcheck` on your code

## Stage 3: Assembly & CPU Architecture
### Resources
- [ ] **PC Assembly Language** by Paul Carter
- [ ] godbolt.org (compile C ↔ view asm)
- [ ] Intel/AMD manuals (optional deep dive)

### Concepts & Tools
- [ ] Registers: `rax`, `rbp`, `rsp`, …
- [ ] Stack frames, calling conventions (SysV, MS)
- [ ] Instructions: `mov`, `call`, `ret`, `jmp`, `cmp`, `je/jne`
- [ ] Tools: `objdump`, `readelf`, `gdb`, `strace`

### Exercises
- [ ] Write simple functions in NASM; call them from C
- [ ] Trace a C function end‑to‑end in `gdb` showing asm ↔ source

## Stage 4: OS Internals Fundamentals
### Books
- [ ] **Operating Systems: Three Easy Pieces** (OSTEP)
- [ ] **Modern Operating Systems** (Tanenbaum)
- [ ] **Linux Kernel Development** (Robert Love)

### Core Concepts
- [ ] Processes, threads, scheduling algorithms
- [ ] Virtual memory, paging, page tables
- [ ] System calls, context switching, interrupts
- [ ] File systems, VFS layer
- [ ] Concurrency: spinlocks, mutexes, RCU

## Stage 5: Tiny OS Development
### Tutorials
- [ ] https://osdev.org/wiki/Bare_Bones
- [ ] https://github.com/cfenollosa/os-tutorial

### Projects
- [ ] Bootloader in x86 assembly (`boot.asm`)
- [ ] Minimal C kernel that prints to screen
- [ ] Set up GDT and IDT
- [ ] Implement keyboard interrupt handler
- [ ] Add a simple round‑robin scheduler
- [ ] Test/debug under QEMU with `-s -S` (KGDB)

## Stage 6: Real OS Exploration
### Codebases
- [ ] MIT xv6 public repository
- [ ] Linux kernel (`torvalds/linux`)
- [ ] MINIX 3 source (microkernel perspective)

### Focus Areas
- [ ] `init/`, `kernel/` (entry, scheduling, syscalls)
- [ ] `mm/` (memory management)
- [ ] `fs/` (filesystem implementations)
- [ ] `drivers/` (device driver examples)

## Stage 7: Kernel Modules & Device Drivers
### Projects
- [ ] Write a “Hello, world” Linux kernel module
- [ ] Implement a char‑device driver (`misc`, `cdev`)
- [ ] Build a simple FUSE filesystem in user space
- [ ] Explore in‑kernel Rust modules (optional)

## Stage 8: Debugging, Tracing & Testing
### Tools & Techniques
- [ ] `gdb`/`kgdb` for live kernel debugging
- [ ] `perf`, `ftrace`, `SystemTap` for profiling/tracing
- [ ] `valgrind`, `kmemleak` for memory checking
- [ ] Kernel selftests and KUnit

### Exercises
- [ ] Profile your tiny OS scheduler under load
- [ ] Write a `ftrace` script to trace a syscall path
- [ ] Set up QEMU snapshots + automated boot tests

## Stage 9: Security & Reverse Engineering
### Topics
- [ ] Stack canaries, NX bit, ASLR, SELinux
- [ ] Exploit development basics (buffer overflows, ROP)
- [ ] Reverse‑engineering with `objdump`, Ghidra

### Projects
- [ ] Harden a simple kernel module with stack protector
- [ ] Craft a minimal ROP chain against a toy vulnerable driver

## Stage 10: Virtualization & Containers
### Concepts
- [ ] Hypervisors: KVM/QEMU, Xen basics
- [ ] Container runtimes: namespaces, cgroups
- [ ] Paravirtualization vs full virtualization

### Mini‑Projects
- [ ] Write a user‑space hypervisor using the KVM API
- [ ] Build a minimal OCI‑compliant container runtime

## Stage 11: Embedded Systems & RTOS
### Platforms
- [ ] ARM Cortex‑M (STM32, nRF52)
- [ ] RISC‑V dev boards

### RTOS
- [ ] FreeRTOS or Zephyr Hello‑World
- [ ] Task scheduling, ISRs, low‑power modes

### Projects
- [ ] Blink LED under FreeRTOS with two competing tasks
- [ ] Port your tiny OS to run on QEMU’s ARM machine

## Stage 12: Advanced Specializations
- [ ] High‑performance networking (DPDK, RDMA)
- [ ] Persistent memory & filesystems (Intel PMEM)
- [ ] Formal verification (seL4, TLA⁺)
- [ ] Real‑time kernels (PREEMPT_RT)
- [ ] Research papers: read SOSP/OSDI conference proceedings

---

## Tools to Master
- Compilers/linkers: `gcc`/`clang`, `ld`, `llvm-binutils`
- Debuggers: `gdb`, `kgdb`, `lldb`
- Profilers/tracers: `perf`, `ftrace`, `bpftrace`
- Binary tools: `objdump`, `readelf`, `hexdump`, `xxd`
- Virtualization: `qemu`, `bochs`, KVM
- Version control & CI: `git`, GitHub Actions, Buildroot, Yocto
- Fuzzers: AFL, libFuzzer, syzbot (for kernel fuzzing)

## Suggested Timeline
- **Months 1–2:** Linux fluency, C basics, string/memory functions  
- **Months 3–4:** Assembly deep‑dive, inline asm, objdump/gdb tracing  
- **Months 5–6:** OS theory (OSTEP), build shell & allocator  
- **Months 7–9:** Tiny OS dev, KGDB/QEMU debugging  
- **Months 10–12:** xv6/Linux exploration, kernel modules  
- **Year 2+:** Advanced topics: security, virtualization, RTOS, contributions  

> **Pro Tip:** Regularly contribute small patches upstream—real feedback from kernel maintainers accelerates learning faster than any tutorial!  
