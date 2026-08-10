markpro@markpro-server:~$ sudo journalctl -u ssh --since "10 minutes ago" --no-pager
-- No entries --
markpro@markpro-server:~$ sudo journalctl -u ssh -n 50 --no-pager
авг 07 15:30:50 markpro-server systemd[1]: Starting ssh.service - OpenBSD Secure Shell server...
авг 07 15:30:50 markpro-server sshd[8508]: Server listening on 0.0.0.0 port 22.
авг 07 15:30:50 markpro-server sshd[8508]: Server listening on :: port 22.
авг 07 15:30:50 markpro-server systemd[1]: Started ssh.service - OpenBSD Secure Shell server.
-- Boot 935d69e3cf6846529935c462d29984fa --
авг 07 15:59:52 markpro-server systemd[1]: Starting ssh.service - OpenBSD Secure Shell server...
авг 07 15:59:52 markpro-server sshd[1226]: Server listening on 0.0.0.0 port 22.
авг 07 15:59:52 markpro-server sshd[1226]: Server listening on :: port 22.
авг 07 15:59:52 markpro-server systemd[1]: Started ssh.service - OpenBSD Secure Shell server.
авг 07 16:19:11 markpro-server sshd[3475]: Connection closed by 127.0.0.1 port 36766 [preauth]
авг 07 16:19:38 markpro-server sshd[1226]: Received signal 15; terminating.
авг 07 16:19:38 markpro-server systemd[1]: Stopping ssh.service - OpenBSD Secure Shell server...
авг 07 16:19:38 markpro-server systemd[1]: ssh.service: Deactivated successfully.
авг 07 16:19:38 markpro-server systemd[1]: Stopped ssh.service - OpenBSD Secure Shell server.
авг 07 16:20:02 markpro-server systemd[1]: Starting ssh.service - OpenBSD Secure Shell server...
авг 07 16:20:02 markpro-server sshd[5147]: Server listening on 0.0.0.0 port 22.
авг 07 16:20:02 markpro-server sshd[5147]: Server listening on :: port 22.
авг 07 16:20:02 markpro-server systemd[1]: Started ssh.service - OpenBSD Secure Shell server.
авг 07 17:38:54 markpro-server sshd[45419]: Connection closed by authenticating user markpro 100.73.180.79 port 59212 [preauth]
авг 07 17:38:54 markpro-server sshd[45426]: Connection closed by authenticating user markpro 100.73.180.79 port 33248 [preauth]
авг 07 17:39:02 markpro-server sshd[45438]: Accepted password for markpro from 100.73.180.79 port 33258 ssh2
авг 07 17:39:02 markpro-server sshd[45438]: pam_unix(sshd:session): session opened for user markpro(uid=1000) by markpro(uid=0)
авг 07 17:39:02 markpro-server sshd[45438]: pam_unix(sshd:session): session closed for user markpro
авг 10 10:23:49 markpro-server systemd[1]: Stopping ssh.service - OpenBSD Secure Shell server...
авг 10 10:23:49 markpro-server sshd[5147]: Received signal 15; terminating.
авг 10 10:23:49 markpro-server systemd[1]: ssh.service: Deactivated successfully.
авг 10 10:23:49 markpro-server systemd[1]: Stopped ssh.service - OpenBSD Secure Shell server.
авг 10 10:23:49 markpro-server systemd[1]: Starting ssh.service - OpenBSD Secure Shell server...
авг 10 10:23:49 markpro-server sshd[71501]: Server listening on 0.0.0.0 port 22.
авг 10 10:23:49 markpro-server sshd[71501]: Server listening on :: port 22.
авг 10 10:23:49 markpro-server systemd[1]: Started ssh.service - OpenBSD Secure Shell server.
авг 10 10:27:30 markpro-server systemd[1]: Stopping ssh.service - OpenBSD Secure Shell server...
авг 10 10:27:30 markpro-server sshd[71501]: Received signal 15; terminating.
авг 10 10:27:30 markpro-server systemd[1]: ssh.service: Deactivated successfully.
авг 10 10:27:30 markpro-server systemd[1]: Stopped ssh.service - OpenBSD Secure Shell server.
авг 10 10:27:30 markpro-server systemd[1]: Starting ssh.service - OpenBSD Secure Shell server...
авг 10 10:27:30 markpro-server sshd[72131]: Server listening on 0.0.0.0 port 22.
авг 10 10:27:30 markpro-server sshd[72131]: Server listening on :: port 22.
авг 10 10:27:30 markpro-server systemd[1]: Started ssh.service - OpenBSD Secure Shell server.
markpro@markpro-server:~$ sudo journalctl -u ssh -n 20 --no-pager
авг 07 17:38:54 markpro-server sshd[45426]: Connection closed by authenticating user markpro 100.73.180.79 port 33248 [preauth]
авг 07 17:39:02 markpro-server sshd[45438]: Accepted password for markpro from 100.73.180.79 port 33258 ssh2
авг 07 17:39:02 markpro-server sshd[45438]: pam_unix(sshd:session): session opened for user markpro(uid=1000) by markpro(uid=0)
авг 07 17:39:02 markpro-server sshd[45438]: pam_unix(sshd:session): session closed for user markpro
авг 10 10:23:49 markpro-server systemd[1]: Stopping ssh.service - OpenBSD Secure Shell server...
авг 10 10:23:49 markpro-server sshd[5147]: Received signal 15; terminating.
авг 10 10:23:49 markpro-server systemd[1]: ssh.service: Deactivated successfully.
авг 10 10:23:49 markpro-server systemd[1]: Stopped ssh.service - OpenBSD Secure Shell server.
авг 10 10:23:49 markpro-server systemd[1]: Starting ssh.service - OpenBSD Secure Shell server...
авг 10 10:23:49 markpro-server sshd[71501]: Server listening on 0.0.0.0 port 22.
авг 10 10:23:49 markpro-server sshd[71501]: Server listening on :: port 22.
авг 10 10:23:49 markpro-server systemd[1]: Started ssh.service - OpenBSD Secure Shell server.
авг 10 10:27:30 markpro-server systemd[1]: Stopping ssh.service - OpenBSD Secure Shell server...
авг 10 10:27:30 markpro-server sshd[71501]: Received signal 15; terminating.
авг 10 10:27:30 markpro-server systemd[1]: ssh.service: Deactivated successfully.
авг 10 10:27:30 markpro-server systemd[1]: Stopped ssh.service - OpenBSD Secure Shell server.
авг 10 10:27:30 markpro-server systemd[1]: Starting ssh.service - OpenBSD Secure Shell server...
авг 10 10:27:30 markpro-server sshd[72131]: Server listening on 0.0.0.0 port 22.
авг 10 10:27:30 markpro-server sshd[72131]: Server listening on :: port 22.
авг 10 10:27:30 markpro-server systemd[1]: Started ssh.service - OpenBSD Secure Shell server.
markpro@markpro-server:~$ sudo sshd -T | grep -E '^(allowusers|denyusers|allowgroups|denygroups|passwordauthentication|pubkeyauthentication|usepam|authenticationmethods)'
usepam yes
pubkeyauthentication yes
passwordauthentication yes
authenticationmethods any
markpro@markpro-server:~$ getent passwd markpro
markpro:x:1000:1000:MarkPro:/home/markpro:/bin/bash
markpro@markpro-server:~$ sudo passwd -S markpro
markpro P 2026-08-10 0 99999 7 -1
markpro@markpro-server:~$ 
