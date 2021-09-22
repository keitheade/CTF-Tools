# CTF-Tools

### Steps to update fresh kali install

#### Update and upgrade
```bash
apt update && apt upgrade -y
```
#### install vscode
###### https://code.visualstudio.com/docs/setup/linux
```bash
wget -qO- https://packages.microsoft.com/keys/microsoft.asc | gpg --dearmor > packages.microsoft.gpg
sudo install -o root -g root -m 644 packages.microsoft.gpg /etc/apt/trusted.gpg.d/
sudo sh -c 'echo "deb [arch=amd64,arm64,armhf signed-by=/etc/apt/trusted.gpg.d/packages.microsoft.gpg] https://packages.microsoft.com/repos/code stable main" > /etc/apt/sources.list.d/vscode.list'
rm -f packages.microsoft.gpg
sudo apt install apt-transport-https
sudo apt update
sudo apt install code # or code-insiders
```
#### install java
```bash
sudo apt-get install default-jdk -y
```
#### install ghidra
###### https://github.com/NationalSecurityAgency/ghidra/releases
```bash
wget https://github.com/NationalSecurityAgency/ghidra/releases/download/Ghidra_10.0.3_build/ghidra_10.0.3_PUBLIC_20210908.zip
unzip ghidra_10.0.3_PUBLIC_20210908.zip
```
#### install Rsa_Ctf_Tool
###### https://github.com/Ganapati/RsaCtfTool
```bash
git clone https://github.com/Ganapati/RsaCtfTool.git
sudo apt-get install libgmp3-dev libmpc-dev -y
cd RsaCtfTool
pip3 install -r "requirements.txt"
python3 RsaCtfTool.py
```
