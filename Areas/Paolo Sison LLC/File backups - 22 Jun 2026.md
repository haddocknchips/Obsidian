### GnuCash: Time Machine ssh into tailnet

- Temporary, will shift to external SSD eventually
- Pasting vim note here
- Started new account with new accounts heirarhy wizard for Business Accounts, to be adjusted later based on [m365CP recommendations](https://m365.cloud.microsoft/chat/agent/Notebook_T0RTUHxwYW9sb3Npc29uLnNoYXJlcG9pbnQuY29tfGIhS0Q0QWpGRnBQMC1ZMmVxYjZRZ0VBNEhvZEVuOVZJeE92ck9qVlpQeGlER0tlc0pSN2tCMlM2Z1dCR3N5QzhXOHwwMTNISDVUQ1NTSkpFS1ZSSVhZQkhaUUFLMlVNUlpCSTZNfENvcGlsb3ROb3RlYm9va3MvZTE3YjEzODAtZjk3Ny00NzA0LThmNDMtNWU0YThhMjA4OTc2X25i/conversation/f555ccf4-36f5-44cf-b881-281ba4c668d1)
- ToDo: need to decide where to back it up => GitHub for now
- Also setting up Time Machine for backups:
	- On Himpapawid:
		- creating these backup folders see [here](https://m365.cloud.microsoft/chat/conversation/346b2e5d-58cd-46a3-82c4-6cff38d709c4):
			- /home/tmuser/timemachine
			- /home/tmuser/backups
- Installed dropbear-initramfs and cryptsetup-initramfs to be able to reboot Himpapawid and unlock LUKS
```
sudo apt update
sudo apt install dropbear-initramfs cryptsetup-initramfs
```
- Note that dropbear port is separate: 2222; this is the default **do not change to your ssh port!**
- During boot, use:
	`ssh -p 2222 root@<ip>`
- After boot, use:
	`ssh -p <your-normal-port> youruser@<ip>

