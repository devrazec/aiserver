# aiserver
Localhost AI Server

# Hardware

Dell Optiplex 3050
Processor i7 7700 
Memory 32GB DDR4
HDD 500GB
SSD NVME 256GB
Realtek ALC3234 High Definition Audio Codec
Realtek RTL8111HSD-CG Gigabit Ethernet LAN 10/100/1000
USB 3.1
Slot M2

# Install Ubuntu


-- Install Ubuntu Server
https://www.youtube.com/watch?v=2Btkx9toufg

sudo apt update && sudo apt upgrade -y

-- Install Tools

sudo apt install lxde-core lxappearance -y
sudo apt install xrdp -y
sudo apt install tasksel -y
sudo apt install python3 python3-pip git - 

-- Install Cockpit

sudo apt install cockpit cockpit-machines -y
sudo systemctl enable --now cockpit.socket
systemctl status cockpit.socket
sudo ufw allow 9090

-- Install Samba

sudo apt install samba -y
sudo smbpasswd -a username
sudo systemctl restart smbd.service

-- Install Virtualization
https://www.freecodecamp.org/news/turn-ubuntu-2404-into-a-kvm-hypervisor/

sudo apt install qemu-kvm libvirt-clients libvirt-daemon-system virt-manager ovmf swtpm-tools virtiofsd bridge-utils -y

-- Install Docker

-- Install Ollama

curl -fsSL https://ollama.com/install.sh | sh
ollama --version
ollama serve
systemctl status ollama

-- Install Ollama.cpp

git clone https://github.com/ggerganov/llama.cpp
cd llama.cpp
cmake -B build
cmake --build build --config Release -j

-- LLMs Studio

curl -fsSL https://lmstudio.ai/install.sh | bash

-- Models

-- Qwen3-8B-Q4_K_M.gguf
-- Qwen3-14B-Q4_K_M.gguf

-- Docker Models Running Locally

# Install Windows 11

-- Hyper-V
-- WS2
-- Docker
-- Visual Code
-- Git
-- GitHub Desktop
-- Chrome
-- Python
-- Nodejs
-- Postman

# Docker Commands 

docker-compose build

docker-compose up -d

docker-compose down

docker-compose up -d --build

docker-compose restart llama

docker-compose up -d llama

docker-compose logs --tail=50 llama

