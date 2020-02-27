# ssm-scripts
A simple repository of bash scripts to connect to machines using AWS Systems Manager

Prerequisites:

* bash
* aws cli

To use the Windows / RDP scripts as-is you need to be running in a bash environment that can execute mstsc.exe - so Ubuntu on WSL or cygwin.
Otherwise, just connect using your RDP client of choice to the local port, default 54000

The main scripts you will want to look at are:

* ssm-session
  * This will establish a shell session (/bin/sh) to Linux machines and a PowerShell session to Windows machines
* ssm-tunnel
  * This will establish a port forwarding session to the target machine
* ssm-rdp
  * This will establish a Remote Desktop connection to Windows machines.  If mstsc.exe and cmdkey.exe are available, it will automatically store the credentials and then attempt a connection to the remote machine.  If not, you can use the connection information and credentials that are echoed to stdout using any RDP client you may have.
* ssm-shell and ssm-ps
  * This will run a remote shell command or remote PowerShell command on the target machine
