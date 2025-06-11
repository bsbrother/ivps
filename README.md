## win11 container
```bash
git clone https://github.com/dockur/windows
cd windows
# Auto install win11.iso first.
docker compose -f compose.yml up -d

# RDP connect(fast, with clipboard)
sudo apt update; apt install -y remmina remmina-plugin-rdp
remmina -c 172.20.0.1:13389 # custom: 1280*768
login: Docker@admin

# Web VNC connect(slow, not clipboard)
http://172.20.0.1:8006
```

## ivps
github collaborate to create win10 VPS.

Get FREE Unlimited Lifetime VPS From Github No Credit Card Required | Full Admin SSH Access
https://www.youtube.com/watch?v=mcKFs-UMrO4

Unlock the secrets to a FREE VPS with our step-by-step guide! 🚀 In this 5-minute video, we'll show you how to access a legal and lifetime VPS service from GitHub without the need for a credit card. Say goodbye to overpriced online tools and hello to fast, secure Remote Desktop Protocol (RDP) access that can elevate your projects. Whether you're a student, developer, or simply looking to save money, this method is perfect for you! Don't miss out on this game-changing opportunity—watch now and take control of your online resources!

```bash
# Download newlest ~/Downloads/rustdesk.deb, see ~/webos/base/kasm*.sh
https://github.com/bsbrother ->Add resposity: ivps ->Public
https://github.com/bsbrother/ivps ->Action ->Add workflow: upload from ~/Downloads/'Windows 10 - RustDesk.yml'
-> Click workflow ->building ...

cd ~/apps/ivps
vi .github/workflow/*.yml
  timeout-minutes: 999999
git push
```
