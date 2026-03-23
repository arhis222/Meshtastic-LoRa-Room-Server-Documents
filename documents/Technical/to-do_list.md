# Meshtastic Room Server - Implementation Guide

# 1. Update Linux System

sudo apt update && sudo apt upgrade -y

# 2. Install Python pip (if not installed)

sudo apt install python3-pip

# Path to python and main.py

ExecStart=/usr/bin/python3 /home/pi/room_server/main.py

# Important: WorkingDirectory ensures SQLite DB is created in the right place

WorkingDirectory=/home/pi/room_server/

# Logging

StandardOutput=inherit
StandardError=inherit


sudo systemctl daemon-reload
sudo systemctl enable room_server.service
sudo systemctl start room_server.service


Check Service Status:

sudo systemctl status room_server.service
(You should see "active (running)" if everything is correct).



View Logs:
sudo journalctl -u roomserver -f
(This will show real-time logs from the service).

# 1. Stop the python server to free the USB port

sudo systemctl stop room_server.service

# 2. Set the exact same channel name

meshtastic --ch-set name "Project-S8" --ch-index 0

# 3. Set the encryption key (Must be prefixed with '0x')

# Replace the string below with your actual Meshcore secret key

meshtastic --ch-set psk "0x26471a28695f6f6bc5b90d27ae1149a7" --ch-index 0

# 4. Restart the python server

sudo systemctl start room_server.service


# Stop the service first

sudo systemctl stop roomserver.service

# Run the cleaner tool

python3 reset_db.py

# Restart service

sudo systemctl start roomserver

### Commandes de MAJ Raspberry Pi

ssh pi@raspberrypi.local
cd ~/Desktop/repertoire/ProjetS8/Src
scp *.py pi@raspberrypi.local:/home/pi/room_server/
