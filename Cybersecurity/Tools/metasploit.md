# Metasploit

Metasploit is the most widely used exploitation framework. 

The Metasploit Framework is a set of tools that serves the following purposes: 
- Information Gathering
- Scanning
- Exploitation
- Exploit Development
- Post-Exploitation

## Versions of Metasploit
- **Metasploit Pro**: Commercial version with GUI
- **Metasploit Framework**: The open-source version that works from the command line.


## Metasploit Components
- **msfconsole**: The main command line interface
- **Modules**: supporting modules such as exploits, scanners, payloads, etc.
- **Tools**: msfvenom, pattern_create, pattern_offset, etc.


## Terminology

- **Exploit**: Code that uses a vulnerability present on the target system.
- **Vulnerability**: A design, coding, or logic flaw affecting the target system.
- **Payload**: An exploit that will take advantage of a vulnerability, code that is run on a target system.


## Help
In the msfconsole you can get help with a command by simply typing help and the name of the command

`help set` 

You can also see the history of you commands with the history command

`history`

## Scanning

Port scanning is easy in the Metasploit framework. A handy way that you can search for different modules 
is by utilizing the keyword "search" 

`search portscan`

This will pull up all modules related to portscan

You can then choose a module with 

`use auxiliary/scanner/portscan/tcp`

This will put you into that specific module, where you can then use

`show options` 

in order to view the options for that specific module

```bash
msf6 auxiliary(scanner/portscan/tcp) > show options

Module options (auxiliary/scanner/portscan/tcp):

   Name         Current Setting  Required  Description
   ----         ---------------  --------  -----------
   CONCURRENCY  10               yes       The number of concurrent ports to check per host
   DELAY        0                yes       The delay between connections, per thread, in milliseconds
   JITTER       0                yes       The delay jitter factor (maximum value by which to +/- DELAY) in milliseconds.
   PORTS        1-10000          yes       Ports to scan (e.g. 22-25,80,110-900)
   RHOSTS                        yes       The target host(s), range CIDR identifier, or hosts file with syntax 'file:'
   THREADS      1                yes       The number of concurrent threads (max one per host)
   TIMEOUT      1000             yes       The socket connect timeout in milliseconds

msf6 auxiliary(scanner/portscan/tcp) >  
```

