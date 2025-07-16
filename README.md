pkg update && pkg upgrade
pkg install wget tar proot -y

wget https://github.com/cloudflare/cloudflared/releases/latest/download/cloudflared-linux-arm
mv cloudflared-linux-arm cloudflared
chmod +x cloudflared
mv cloudflared $PREFIX/bin/

