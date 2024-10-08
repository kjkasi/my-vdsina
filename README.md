# my-vdsina

## setup
```
apt update
apt upgrade
shutdown -r now

# Add Docker's official GPG key:
sudo apt-get update
sudo apt-get install ca-certificates curl
sudo install -m 0755 -d /etc/apt/keyrings
sudo curl -fsSL https://download.docker.com/linux/ubuntu/gpg -o /etc/apt/keyrings/docker.asc
sudo chmod a+r /etc/apt/keyrings/docker.asc

# Add the repository to Apt sources:
echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.asc] https://download.docker.com/linux/ubuntu \
  $(. /etc/os-release && echo "$VERSION_CODENAME") stable" | \
  sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
sudo apt-get update

sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin

apt install git
git clone

cat <<EOF > .env
WG_HOST=0.0.0.0
WG_PASSWORD="<PSWD>"
#WG_ALLOWED_IPS=0.0.0.0
SHADOWSOCKS_PASSWORD="<PSWD>"
TS_PASSWORD="<PSWD>"
EOF

docker compose up -d
```