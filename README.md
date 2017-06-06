peda
====

PEDA - Python Exploit Development Assistance for GDB

## Key Features:
* Enhance the display of gdb: colorize and display disassembly codes, registers, memory information during debugging.
* Add commands to support debugging and exploit development (for a full list of commands use `peda help`):
  * `aslr` -- Show/set ASLR setting of GDB
  * `checksec` -- Check for various security options of binary
  * `dumpargs` -- Display arguments passed to a function when stopped at a call instruction
  * `dumprop` -- Dump all ROP gadgets in specific memory range
  * `elfheader` -- Get headers information from debugged ELF file
  * `elfsymbol` -- Get non-debugging symbol information from an ELF file
  * `lookup` -- Search for all addresses/references to addresses which belong to a memory range
  * `patch` -- Patch memory start at an address with string/hexstring/int
  * `pattern` -- Generate, search, or write a cyclic pattern to memory
  * `procinfo` -- Display various info from /proc/pid/
  * `pshow` -- Show various PEDA options and other settings
  * `pset` -- Set various PEDA options and other settings
  * `readelf` -- Get headers information from an ELF file
  * `ropgadget` -- Get common ROP gadgets of binary or library
  * `ropsearch` -- Search for ROP gadgets in memory
  * `searchmem|find` -- Search for a pattern in memory; support regex search
  * `shellcode` -- Generate or download common shellcodes.
  * `skeleton` -- Generate python exploit code template
  * `vmmap` -- Get virtual mapping address ranges of section(s) in debugged process
  * `xormem` -- XOR a memory region with a key

## Symbolic Execution Features:
* Run triton engine parallel to GDB to visual the execution of a program while it is run over the symbolic engine.
  * `syminit` Initiate triton symbolic engine and its linkage with GDB
  * `syminput` Add symbolic input variables
  * `symuntil` Execute instructions until a given address
  * `symuntiljump` Execute instructions until a symbolized jump instruction is encountered
  * `symuntilinst` Execute instructions until a symbolized instruction is encountered
  * `symtake` Take symbolized jump
  * `symavoid` Avoid symbolized jump
  * `symsync` Sync GDB with Triton current state
  * `symreset` Reset triton memory with GDB current state
  * `symsnapshot` Save/restore snapshot of Triton+GDB memory state
  * `sympeek` Check memory content in Triton engine
  * `sympoke` Change memory content in Triton engine

* An illustration can be found here:
 [![asciicast](https://asciinema.org/a/FQ0rj7zhMNS8ZDnwwnoCz9NFX.png)](https://asciinema.org/a/FQ0rj7zhMNS8ZDnwwnoCz9NFX?speed=1.25)

## Installation

    git clone https://github.com/longld/peda.git ~/peda
    echo "source ~/peda/peda.py" >> ~/.gdbinit
    echo "DONE! debug your program with gdb and enjoy"

## Screenshot
![start](http://i.imgur.com/P1BF5mp.png)

![pattern arg](http://i.imgur.com/W97OWRC.png)

![patts](http://i.imgur.com/Br24IpC.png)
