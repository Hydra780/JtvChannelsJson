pkg update && pkg upgrade
pkg install wget tar proot -y

wget https://github.com/cloudflare/cloudflared/releases/latest/download/cloudflared-linux-arm
mv cloudflared-linux-arm cloudflared
chmod +x cloudflared
mv cloudflared $PREFIX/bin/

    ./cloudflared-linux-arm --version
    ./cloudflared tunnel --url http://127.0.0.1:8080
