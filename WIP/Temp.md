Make a windows binary (PE) from a python script on kali.

- download the python windows installer
- wine install python 2.7.9+ (I used 2.7.14 with wine msiexec /i ...)
- wine pip install pyinstaller
- follow the rest of the steps i did...just paste the cmds for 11581

Windows post-ex enum

- arp -a
- net view
- net use
- net share


!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!
!!                                 !!
!! NO FOLDING SECTIONS FOR GITBOOK !!
!!                                 !!
!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!



To-do
-------------------------------------------------------------------

- - - 

### Simple Buffer Overflow Attack.md

- [ ] Change H2 formats from `##` to `====`.

- - - 

### SQL Injection Basics.md

- [ ] Upload to Imgur and insert `[image alt]` for the login box.

- - - 

### Simple Buffer Overflow Attack.md

- [ ] Simplify Python scripts to get rid of gsstyle.
- [ ] Turn the iterations of fuzzing, buffer overflow, payload generation, sending hex values, using output to determine badchars, etc into a python tool. Then make it into a compiled binary for x86 Linux, x86 windows, and ARM.

- - -

### Table of Contents

- [ ] Build a TOC for this README file.

- - -

### Windows Post-Exploitation

- [ ] Steps you always do.
- [ ] Scripts/tools to run in general format of [toolname, where it works table, what it gives you, syntax, screenshots/examples]
- [ ] LM vs NTLM
- [ ] hash cracking (just point to hash cracking article)
- [ ] SAM and SYSTEM files > reg, reg backup, SAM.old SYSTEM.old, samdump2
- [ ] Transferring tools and data (just point to Windows file transfer article)

- - -

### Metasploit Framework

- [ ] Exploit choice construction
- [ ] Payload choice construction
- [ ] SOP start-up
- [ ] Run-through of start-up, ID, portscan, vulscan, exploit, meterpreter
- [ ] Meterpreter
- [ ] Pivoting
- [ ] Tools outside the console
- [ ] Porting modules to python/ruby standalone
- 

### Kali Tools

- [ ] Move "Tool Details" to individual pages, or pages by first letter of tool name
- [ ] Swap non-kali tools index and kali tools index so non-kali tools are listed first
- [ ] Consider turning the whole index into a table, somehow indicating non-kali tools, and renaming the page to "Tools Index"


