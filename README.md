markpro@markpro-server:~$ hostname -I
192.168.50.100 
markpro@markpro-server:~$ sudo systemctl status ssh --no-pager
● ssh.service - OpenBSD Secure Shell server
     Loaded: loaded (/usr/lib/systemd/system/ssh.service; enabled; preset: enabled)
     Active: active (running) since Mon 2026-08-10 10:27:30 MSK; 56min ago
       Docs: man:sshd(8)
             man:sshd_config(5)
   Main PID: 72131 (sshd)
      Tasks: 1 (limit: 16545)
     Memory: 1.2M (peak: 1.9M)
        CPU: 14ms
     CGroup: /system.slice/ssh.service
             └─72131 "sshd: /usr/sbin/sshd -D [listener] 0 of 10-100 startups"

авг 10 10:27:30 markpro-server systemd[1]: Starting ssh.service - OpenBSD Secure Shell server...
авг 10 10:27:30 markpro-server sshd[72131]: Server listening on 0.0.0.0 port 22.
авг 10 10:27:30 markpro-server sshd[72131]: Server listening on :: port 22.
авг 10 10:27:30 markpro-server systemd[1]: Started ssh.service - OpenBSD Secure Shell server.
markpro@markpro-server:~$ whoami
markpro
markpro@markpro-server:~$ sudo ss -tulpn | grep :22
tcp   LISTEN 0      128          0.0.0.0:22         0.0.0.0:*    users:(("sshd",pid=72131,fd=3))            
tcp   LISTEN 0      128             [::]:22            [::]:*    users:(("sshd",pid=72131,fd=4))            
markpro@markpro-server:~$ 
