---
layout: default
title: Installation
parent: vishnu
grand_parent: Cross Platform
nav_order: 1
---

# Linux
There is one static value that is needed in order for this to work properly on Linux. It is listed below:

- The string value being returned, found in `spec/spec_linux.go`, in the `GetAdapter()` function. It is set to return `"ens160"` by default. Modify this value as you see fit.

To compile, you need libpcap. On linux, you can install by running `sudo apt install libpcap-dev`. 

For the port opening, make sure you have `inetd` installed. If you are not sure, run `apt install openbsd-inetd`.

Then you can use `make agent-linux` to generate the binary.
# Windows
In order for the binary to work correctly on Windows, `npcap / winpcap` needs to be installed. You can find it here: https://nmap.org/npcap/

Once this is done, run `make agent-windows` to create the executable.

# Customizations
There are few other modifications that can be made in the targetInfo struct. Go to the `sInit` function in `main.go` and modify the values as you see fit listed below:
- `secretPorts` : this int array holds the ports that will be used for knocking
- `connectBack` : boolean value for linux for a bind or connectback shell
- `connectBackPort` : if connectback is being used, this string value is the port that will be utilized.

# Connectback Shell Info

You can optionally have the backdoor operate in connectback mode - where after successfully knocking a shell is sent back to the knocking IP on a predetermined port. 

Be careful doing this behind NAT as while knocking will work, the shell won't get back to you. You'll need to do port forwarding or listen for the shell on a public IP.

For use on Windows, the connectback method is used.
