# Инструкция по установке WireGuard на сервере

- Подключаемся к серверу по SSH
- Выполняем по очередности следующие команды
```
apt install curl
apt install git
curl -fsSL https://get.docker.com -o get-docker.sh
sudo sh ./get-docker.sh
git clone https://github.com/Tirkai/wg-install.git /opt/wg-easy
cd /opt/wg-easy
echo "WG_HOST=INSERT_YOUR_IP_ADDRESS" >> ./.env
echo "PASSWORD=INSERT_YOUR_PASSWORD" >> ./.env
docker compose up -d
```
Переходим в браузере на http://наш_ip:51821