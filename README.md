sudo ss -lntp

sudo iptables -t nat -L -n -v

sudo nft list ruleset

curl -v http://192.168.50.100:22

sudo tcpdump -ni enx00e04c36b393 -A -s 0 port 22
