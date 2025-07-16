     pkg update && pkg upgrade
    pkg install wget proot tar -y
wget https://github.com/cloudflare/cloudflared/releases/download/2021.11.0/cloudflared-linux-arm -O cloudflared
chmod +x cloudflared

./cloudflared --version
./cloudflared tunnel --url http://127.0.0.1:8080
