markpro@markpro-server:~$ sudo ss -lntp

sudo iptables -t nat -L -n -v

sudo nft list ruleset

curl -v http://192.168.50.100:22

sudo tcpdump -ni enx00e04c36b393 -A -s 0 port 22
State     Recv-Q    Send-Q       Local Address:Port        Peer Address:Port    Process                                                                         
LISTEN    0         4096            127.0.0.54:53               0.0.0.0:*        users:(("systemd-resolve",pid=18579,fd=17))                                    
LISTEN    0         4096         127.0.0.53%lo:53               0.0.0.0:*        users:(("systemd-resolve",pid=18579,fd=15))                                    
LISTEN    0         4096             127.0.0.1:631              0.0.0.0:*        users:(("cupsd",pid=65347,fd=7))                                               
LISTEN    0         128                0.0.0.0:22               0.0.0.0:*        users:(("sshd",pid=72131,fd=3))                                                
LISTEN    0         128                   [::]:22                  [::]:*        users:(("sshd",pid=72131,fd=4))                                                
LISTEN    0         4096                 [::1]:631                 [::]:*        users:(("cupsd",pid=65347,fd=6))                                               
Chain PREROUTING (policy ACCEPT 0 packets, 0 bytes)
 pkts bytes target     prot opt in     out     source               destination         

Chain INPUT (policy ACCEPT 0 packets, 0 bytes)
 pkts bytes target     prot opt in     out     source               destination         

Chain OUTPUT (policy ACCEPT 0 packets, 0 bytes)
 pkts bytes target     prot opt in     out     source               destination         

Chain POSTROUTING (policy ACCEPT 8744 packets, 679K bytes)
 pkts bytes target     prot opt in     out     source               destination         
table ip filter {
	chain INPUT {
		type filter hook input priority filter; policy accept;
		counter packets 5137 bytes 4274083 jump ufw-before-logging-input
		counter packets 5137 bytes 4274083 jump ufw-before-input
		counter packets 4745 bytes 4190555 jump ufw-after-input
		counter packets 4709 bytes 4171115 jump ufw-after-logging-input
		counter packets 4709 bytes 4171115 jump ufw-reject-input
		counter packets 4709 bytes 4171115 jump ufw-track-input
	}

	chain FORWARD {
		type filter hook forward priority filter; policy accept;
		counter packets 0 bytes 0 jump ufw-before-logging-forward
		counter packets 0 bytes 0 jump ufw-before-forward
		counter packets 0 bytes 0 jump ufw-after-forward
		counter packets 0 bytes 0 jump ufw-after-logging-forward
		counter packets 0 bytes 0 jump ufw-reject-forward
		counter packets 0 bytes 0 jump ufw-track-forward
	}

	chain OUTPUT {
		type filter hook output priority filter; policy accept;
		counter packets 5099 bytes 1252792 jump ufw-before-logging-output
		counter packets 5099 bytes 1252792 jump ufw-before-output
		counter packets 4717 bytes 1188054 jump ufw-after-output
		counter packets 4717 bytes 1188054 jump ufw-after-logging-output
		counter packets 4717 bytes 1188054 jump ufw-reject-output
		counter packets 4717 bytes 1188054 jump ufw-track-output
	}

	chain ufw-before-logging-input {
	}

	chain ufw-before-logging-output {
	}

	chain ufw-before-logging-forward {
	}

	chain ufw-before-input {
	}

	chain ufw-before-output {
	}

	chain ufw-before-forward {
	}

	chain ufw-after-input {
	}

	chain ufw-after-output {
	}

	chain ufw-after-forward {
	}

	chain ufw-after-logging-input {
	}

	chain ufw-after-logging-output {
	}

	chain ufw-after-logging-forward {
	}

	chain ufw-reject-input {
	}

	chain ufw-reject-output {
	}

	chain ufw-reject-forward {
	}

	chain ufw-track-input {
	}

	chain ufw-track-output {
	}

	chain ufw-track-forward {
	}
}
table ip nat {
	chain POSTROUTING {
		type nat hook postrouting priority srcnat; policy accept;
	}
}
table ip6 filter {
	chain INPUT {
		type filter hook input priority filter; policy accept;
		counter packets 1 bytes 93 jump ufw6-before-logging-input
		counter packets 1 bytes 93 jump ufw6-before-input
		counter packets 1 bytes 93 jump ufw6-after-input
		counter packets 1 bytes 93 jump ufw6-after-logging-input
		counter packets 1 bytes 93 jump ufw6-reject-input
		counter packets 1 bytes 93 jump ufw6-track-input
	}

	chain FORWARD {
		type filter hook forward priority filter; policy accept;
		counter packets 0 bytes 0 jump ufw6-before-logging-forward
		counter packets 0 bytes 0 jump ufw6-before-forward
		counter packets 0 bytes 0 jump ufw6-after-forward
		counter packets 0 bytes 0 jump ufw6-after-logging-forward
		counter packets 0 bytes 0 jump ufw6-reject-forward
		counter packets 0 bytes 0 jump ufw6-track-forward
	}

	chain OUTPUT {
		type filter hook output priority filter; policy accept;
		counter packets 3 bytes 189 jump ufw6-before-logging-output
		counter packets 3 bytes 189 jump ufw6-before-output
		counter packets 2 bytes 141 jump ufw6-after-output
		counter packets 2 bytes 141 jump ufw6-after-logging-output
		counter packets 2 bytes 141 jump ufw6-reject-output
		counter packets 2 bytes 141 jump ufw6-track-output
	}

	chain ufw6-before-logging-input {
	}

	chain ufw6-before-logging-output {
	}

	chain ufw6-before-logging-forward {
	}

	chain ufw6-before-input {
	}

	chain ufw6-before-output {
	}

	chain ufw6-before-forward {
	}

	chain ufw6-after-input {
	}

	chain ufw6-after-output {
	}

	chain ufw6-after-forward {
	}

	chain ufw6-after-logging-input {
	}

	chain ufw6-after-logging-output {
	}

	chain ufw6-after-logging-forward {
	}

	chain ufw6-reject-input {
	}

	chain ufw6-reject-output {
	}

	chain ufw6-reject-forward {
	}

	chain ufw6-track-input {
	}

	chain ufw6-track-output {
	}

	chain ufw6-track-forward {
	}
}
table ip6 nat {
	chain POSTROUTING {
		type nat hook postrouting priority srcnat; policy accept;
	}
}
table ip mangle {
	chain PREROUTING {
		type filter hook prerouting priority mangle; policy accept;
	}

	chain OUTPUT {
		type route hook output priority mangle; policy accept;
	}
}
table ip6 mangle {
	chain PREROUTING {
		type filter hook prerouting priority mangle; policy accept;
	}

	chain OUTPUT {
		type route hook output priority mangle; policy accept;
	}
}
*   Trying 192.168.50.100:22...
* Connected to 192.168.50.100 (192.168.50.100) port 22
> GET / HTTP/1.1
> Host: 192.168.50.100:22
> User-Agent: curl/8.5.0
> Accept: */*
> 
* Received HTTP/0.9 when not allowed
* Closing connection
curl: (1) Received HTTP/0.9 when not allowed
tcpdump: verbose output suppressed, use -v[v]... for full protocol decode
listening on enx00e04c36b393, link-type EN10MB (Ethernet), snapshot length 262144 bytes

^C
0 packets captured
0 packets received by filter
0 packets dropped by kernel
markpro@markpro-server:~$ ^[[200~sudo tcpdump -ni enx00e04c36b393 -A -s 0 port 22~
sudo: команда не найдена
markpro@markpro-server:~$ sudo tcpdump -ni enx00e04c36b393 -A -s 0 port 22
tcpdump: verbose output suppressed, use -v[v]... for full protocol decode
listening on enx00e04c36b393, link-type EN10MB (Ethernet), snapshot length 262144 bytes
^C
0 packets captured
0 packets received by filter
0 packets dropped by kernel
markpro@markpro-server:~$ sudo tcpdump -ni enx00e04c36b393 -A -s 0 port 22
tcpdump: verbose output suppressed, use -v[v]... for full protocol decode
listening on enx00e04c36b393, link-type EN10MB (Ethernet), snapshot length 262144 bytes
^C
0 packets captured
0 packets received by filter
0 packets dropped by kernel
markpro@markpro-server:~$ 
