# Invoker

Penetration testing utility.

The goal is to use this tool when access to some Windows OS features through GUI is restricted.

Some features require administrative privileges.

Capabilities:

* invoke the Command Prompt and PowerShell,
* download a file,
* add a registry key,
* schedule a task,
* connect to a remote host,
* terminate a running process,
* run a new process,
* inject bytecode into a running process,
* inject DLL into a running process,
* enable access token privileges,
* duplicate access token of a running process,
* list unquoted service paths and restart a running service,
* replace Sticky Keys.

Built with Dev-C++ IDE v5.11 (64 bit), compiled with TDM-GCC v4.9.2 (64 bit) and tested on Windows 10 Enterprise OS (64 bit). Download Dev-C++ from [here](https://sourceforge.net/projects/orwelldevcpp/files/Portable%20Releases/).

Made for educational purposes. I hope it will help!

## Invoker Library

Check all the capabilities [here](https://github.com/ivan-sincek/invoker/tree/master/src/lib/invoker). Feel free to use the library.

## PowerShell Scripts

Check all the PowerShell scripts used in the main C++ program [here](https://github.com/ivan-sincek/invoker/tree/master/ps).

## How to Run

Run ['\\exec\\Invoker.exe'](https://github.com/ivan-sincek/invoker/tree/master/exec).

## Bytecode Injection

Elevate privileges by injecting bytecode into a higher-privileged process.

This tool can parse an HTTP response and extract the payload from a custom element, i.e. from `<img class="bc" src="data:image/gif;base64,payload" alt="bc" hidden="hidden">` where `payload` is a binary code/file encoded in Base64.

This might be useful if antivirus is constantly deleting your local payloads.

You can also specify your own custom element but you will have to modify the program source code and recompile it.

Check an example at [pastebin.com/raw/Nd1tCBv6](https://pastebin.com/raw/Nd1tCBv6).

**Bytecode provided will most certainly not work for you.**

## Generate a Reverse Shell Payload

Find out how to generate a reverse shell payload from my other [project](https://github.com/ivan-sincek/penetration-testing-cheat-sheet#generate-a-reverse-shell-payload).

## Get the LocalSystem Account (NT AUTHORITY\SYSTEM)

Run the Invoker.exe as administrator.

Enable all access token privileges.

Duplicate the access token from e.g. Windows Logon Application (winlogon.exe) and run a new instance of Invoker.exe.

Within the new Invoker.exe instance, open the Command Prompt and run `whoami`, you should now see `nt authority\system`.

Enable all access token privileges once again.

Close the old instance of Invoker.exe.

P.S. You get more access token privileges from Local Security Authority Subsystem Service (lsass.exe).

## Images

![Invoker](https://github.com/ivan-sincek/invoker/blob/master/img/invoker.jpg)

![Registry](https://github.com/ivan-sincek/invoker/blob/master/img/registry.jpg)

![Injection](https://github.com/ivan-sincek/invoker/blob/master/img/injection.jpg)

![Privileges](https://github.com/ivan-sincek/invoker/blob/master/img/privileges.jpg)
