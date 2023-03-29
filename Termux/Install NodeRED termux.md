pkg update && pkg upgrade - y

pkg install openssh

passwd

sshd

from PC: ssh -p 8022 x.x.x.x

---

pkg install nodejs-lts build-essential binutils-is-llvm python

npm i -g --unsafe-perm node-red

termux-fix-shebang $(which node-red)

---

from HOME: nano .mosquitto.conf

listener 1883
allow_anonymous true

---

cd .termux

mkdir boot

cd boot

nano start.sh

#!/data/data/com.termux/files/usr/bin/sh
termux-wake-lock
sshd & mosquitto -c /data/data/com.termux/files/home/.mosquitto.conf & node-red
