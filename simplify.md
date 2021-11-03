- [*] Replace copyin() with a call to copyin_new first, and make it work, before moving on to copyinstr.

- [*] At each point where the kernel changes a process's user mappings, change the process's kernel page table in the same way. Such points include fork(), exec(), and sbrk().

- [*] Don't forget that to include the first process's user page table in its kernel page table in userinit.

- [*] What permissions do the PTEs for user addresses need in a process's kernel page table? (A page with PTE_U set cannot be accessed in kernel mode.)

- [*] Don't forget about the above-mentioned PLIC limit.