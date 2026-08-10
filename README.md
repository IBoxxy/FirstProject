markpro@markpro-server:~$ ip -br addr
lo               UNKNOWN        127.0.0.1/8 ::1/128 
enx00e04c36b393  UP             192.168.50.100/24 fe80::8d17:8d42:730a:6690/64 
markpro@markpro-server:~$ 
ip route
default via 192.168.50.1 dev enx00e04c36b393 proto dhcp src 192.168.50.100 metric 100 
192.168.50.0/24 dev enx00e04c36b393 proto kernel scope link src 192.168.50.100 metric 100 
markpro@markpro-server:~$ 
ip -br link
lo               UNKNOWN        00:00:00:00:00:00 <LOOPBACK,UP,LOWER_UP> 
enx00e04c36b393  UP             00:e0:4c:36:b3:93 <BROADCAST,MULTICAST,UP,LOWER_UP> 
markpro@markpro-server:~$ sudo ufw status verbose
Состояние: неактивен
markpro@markpro-server:~$ 
