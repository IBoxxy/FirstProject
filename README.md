# Отключаем сокет-активацию
sudo systemctl stop ssh.socket
sudo systemctl disable ssh.socket

# Включаем обычную постоянную службу SSH
sudo systemctl enable --now ssh.service
