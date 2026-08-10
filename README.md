sudo journalctl -u ssh --since "10 minutes ago" --no-pager

sudo journalctl -u ssh -n 50 --no-pager

sudo journalctl -u ssh -n 20 --no-pager
