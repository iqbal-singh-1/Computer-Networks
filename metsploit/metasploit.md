# What is Metasploit?

Metasploit is a widely used framework in cybersecurity. With various built-in features, it is one of the most powerful tools available. While it can perform multiple tasks, it is primarily known for its ability to conduct penetration testing. It is a powerful tool for gathering information about target machines, checking for vulnerabilities, and exploiting them to gain access to target systems.

## Types of Metasploit

1. **Metasploit Pro**
    - The commercial version of Metasploit used by security experts.
    - Automates penetration testing and many other tasks.
    - Allows users to collaborate on the same tasks, enabling multiple users to work on a project for faster completion.
    - Supports scheduling tests, facilitating the integration of various security tasks.
    - If you are a learner, it's recommended to practice with the Metasploit Framework before switching to Pro.

2. **Metasploit Framework**
    - An open-source version of Metasploit that uses a command-line interface for penetration testing, information gathering, and more.
    - Primarily used on Linux operating systems.
    - In this repo, we will focus on the Metasploit Framework.

## Components of Metasploit

There are three main components of the Metasploit Framework:

1. **msfconsole**
    - The command-line interface on which Metasploit runs.
    - Simply type `msfconsole` in Kali or any other Linux distribution to launch Metasploit.

2. **Modules**
    - The Metasploit Framework is divided into various modules, including payloads, exploits, auxiliary modules, and more.

3. **Tools**
    - Some of the tools used in Metasploit include penetration testing tools, pattern creation tools, `msfvenom`, and others.

## Modules

### Auxiliary Modules

Auxiliary modules provide additional support within the Metasploit Framework. They can be used for:

- Penetration testing
- Brute force attacks
- Scanning
- Service detection
- Security assessment of web applications

To view the sub-modules contained within the auxiliary module, you can use the following command:

```bash
cd /opt/metasploit-framework/embedded/framework/modules
tree -L 1 auxiliary/
auxiliary/
├── admin
├── analyze
├── bnat
├── client
├── cloud
├── crawler
├── docx
├── dos
├── example.py
├── example.rb
├── fileformat
├── fuzzers
├── gather
├── parser
├── pdf
├── scanner
├── server
├── sniffer
├── spoof
├── sqli
├── voip
└── vsploit

20 directories, 2 files
```
### Encoders
- These are the modules which helps in encoding an exploit or a payload.
- It can therefore be used to send the encoded malicious code to the target's machine hoping that it may bypass its security.
- It can be used by security professionals ethically to check the security of the system or may be used to gather information about our hacker.
- Overview of Encoders modules:-
```bash
tree -L 1 encoders/
encoders/
├── cmd
├── generic
├── mipsbe
├── mipsle
├── php
├── ppc
├── ruby
├── sparc
├── x64
└── x86

10 directories, 0 files
```
### Evasion modules 
- Helps in bypassing the system security.
- It's main focus is to provide stealth so that the payloads and exploits can be delivered into the target system without seeking much attention.
- It can alter the way exploits and payloads loo and work.
- Output modules:-
```bash
evasion/
└── windows
    ├── applocker_evasion_install_util.rb
    ├── applocker_evasion_msbuild.rb
    ├── applocker_evasion_presentationhost.rb
    ├── applocker_evasion_regasm_regsvcs.rb
    ├── applocker_evasion_workflow_compiler.rb
    ├── process_herpaderping.rb
    ├── syscall_inject.rb
    ├── windows_defender_exe.rb
    └── windows_defender_js_hta.rb

1 directory, 9 files
```
### Exploits
- Exploit word basically means a vulnerability or a backdoor that can be used to access a system's security.
- This module can be helpful in detecting which vulnerabilities are available in the system and can be used to access system using those.
- Here are some sub-modules available under exploit:-
```bash
exploits/
├── aix
├── android
├── apple_ios
├── bsd
├── bsdi
├── dialup
├── example_linux_priv_esc.rb
├── example.py
├── example.rb
├── example_webapp.rb
├── firefox
├── freebsd
├── hpux
├── irix
├── linux
├── mainframe
├── multi
├── netware
├── openbsd
├── osx
├── qnx
├── solaris
├── unix
└── windows

20 directories, 4 files
```

## payload
- These are the codes which run on target machine.
- It opens a terminal using which we can perform operations on target machine using our host device.
- Other examples include malware, backdoor to access the target system, running commands etc.
- There are 4 sub-modules in it :- 
1. Adaptors:- this module can be used to wrap the single payloads so that their format can be converted into useful format.
2. Single:- these paylopads do not need any additional resources to run. They are self contained.
3. Stagers:- these are the payloads which set a connection between host and target. Later, they download all the resources they need on the target machine.
Hence the name stagers.
4. Stage:- stagers download these resources we were talking about.(stagers set up their stage before giving their performance)

