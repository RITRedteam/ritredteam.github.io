---
layout: default
title: Limitations
parent: Nosferatu
grand_parent: Windows
nav_order: 3
---

## Limitations

In an Active Directory environment, authentication via RDP, runas, or the lock screen does not work with the `nosferatu` password. Authentication using SMB, WinRM, and WMI is still possible. 

In a non-AD environment, authentication works for all aspects.