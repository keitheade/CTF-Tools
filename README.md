# CTF-Tools

### Steps to update fresh kali install

#### Update and upgrade
```bash
apt update && apt upgrade -y
```
#### install vscode
###### https://code.visualstudio.com/docs/setup/linux
```bash
https://go.microsoft.com/fwlink/?LinkID=760868
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
#### Install GDB
```bash
sudo apt install gdb -y 
```
#### Install Pwndbg
###### https://github.com/pwndbg/pwndbg
```bash
git clone https://github.com/pwndbg/pwndbg
cd pwndbg
sudo ./setup.sh
```
#### Install splitmind
###### https://github.com/jerdna-regeiz/splitmind
```bash
echo '''
(splitmind.Mind()
  .below(display="backtrace")
  .right(display="stack")
  .right(display="regs")
  .right(of="main", display="disasm")
  .show("legend", on="disasm")
).build()
''' >> ~/splitmind/gdbinit.py
```
*You need to run gdb within tmux for this to work*

#### install Rsa_Ctf_Tool
###### https://github.com/Ganapati/RsaCtfTool
```bash
git clone https://github.com/Ganapati/RsaCtfTool.git
sudo apt-get install libgmp3-dev libmpc-dev -y
cd RsaCtfTool
pip3 install -r "requirements.txt"
python3 RsaCtfTool.py
```
