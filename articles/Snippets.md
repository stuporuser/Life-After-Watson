Windows: How to See Currently Logged in Users in Windows 10 / 8 / 7
----------------------------------------------------------------

From cmd.exe:

```
C:\>query user
  USERNAME                SESSIONNAME     ID  STATE   IDLE TIME   LOGON TIME
 >tom                     console          8  Active          .   3/11/2017 12:24 AM
  test                                    11  Disc            .   3/11/2017 12:30 AM
```


Windows: Add domain user and add to domain group
---------------------------------------------------------

```
C:\>net user <username> <password> /add /domain
The command completed successfully.

C:\>net group <groupname> <username> /add /domain
The command completed successfully.
```


Windows: Add local user and add to local group
---------------------------------------------------------

```
C:\>net user <username> <password> /add
The command completed successfully.

C:\>net localgroup <groupname> <username> /add
The command completed successfully.
```


Windows: WMI commands
---------------------------------------

WMIC has a tricky syntax. The below commands and [this link](https://isc.sans.edu/diary/The+Grammar+of+WMIC/2376) should get you started with the essentials. Take note of which key elements are in quotes, such as hostnames with hyphens and group names with whitespace.

Example: From host "I-WILL-WEF", used WMIC to create a domain user remotely on "IWILL-WIN2K16-1" and then to add that user to Domain Admins. (Note that the output from these commands was sketchy, so I had to verify they worked via `net group "Domain Admins"`.

```
C:\>wmic /node:"IWILL-WIN2K16-1" process call create "cmd.exe /c net user domainadmin ladmin123!@# /add /domain"

C:\>wmic /node:"IWILL-WIN2K16-1" process call create 'cmd.exe /c net group "domain admins" domainadmin /add /domain'
```



Windows Exploitation: Golden Tickets, Silver Tickets, and More.
----------------------------------------------------------------

From [https://adsecurity.org/?p=1515](https://adsecurity.org/?p=1515).

That article has all relevant info about the tickets, so I'm not reproducing it here. It also contains mitigation/countermeasures for Kerberos ticket exploitation, and that's helpful for building less-detectable forged tickets.




