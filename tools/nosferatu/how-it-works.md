---
layout: default
title: How it works
parent: nosferatu
grand_parent: Tools
nav_order: 1
---

## How it works

First, the DLL is injected into the `lsass.exe` process, and will begin hooking authentication WinAPI calls. The targeted function is `MsvpPasswordValidate()`, located in `NtlmShared.dll`. In the pursuit of not being detected, the hooked function will call the original function and allow for the normal flow of authentication. Only after seeing that authentication has failed will the hook swap out the actual NTLM hash with the backdoor hash for comparison.
