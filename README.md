# Command Dasar

## 1. Folder
```
#Buat Folder
mkdir nama-folder
```
```
#Buat File
nano nama-file
```
```
#Cek Folder
ls
```
```
#Simpan File
CTRL + X + Y + ENTER
```
```
#Hapus File/Folder
rm -rf namafile/folder
```

## 2. Screen
```
#Install Screen
apt install screen
```
```
#Uninstall Screen
sudo apt remove screen
```
```
#Buat Screen
screen -S nama-screen
```
```
#Hapus Screen
screen -X -S namascreen quit
```
```
#Tutup Screen
CTRL + A + D
```
```
#Cek Screen
screen -ls
```
```
#Masuk Screen
screen -r nama-screen
```

## 3. Git
```
#Install Git
apt install git
```
```
#Uninstall Git
sudo apt remove git
```
```
#Cek Versi Git
git --version
```
```
#Clone GitHub
git clone link-github
```

## 4.Docker
```
#Install Docker
sudo apt-get install -y ca-certificates curl gnupg lsb-release && curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg && echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null && sudo apt-get update && sudo apt-get install -y docker-ce docker-ce-cli containerd.io && sudo apt-mark hold docker-ce docker-ce-cli containerd.io
```
```
#Uninstall Docker
sudo apt-mark unhold docker-ce docker-ce-cli containerd.io && sudo apt-get remove --purge -y docker-ce docker-ce-cli containerd.io && sudo rm -rf /var/lib/docker /var/lib/containerd && sudo rm /etc/apt/sources.list.d/docker.list && sudo apt-get autoremove -y && sudo apt-get autoclean
```
```
#Cek Docker
docker ps -a
```
```
#Hentikan Docker
docker stop <IDContainer>
```
```
#Hapus Docker
docker rm <IDContainer>
```

## 5.GO
```
#Install GO
LATEST_GO=$(curl -s https://go.dev/VERSION?m=text) && wget https://go.dev/dl/${LATEST_GO}.linux-amd64.tar.gz && sudo rm -rf /usr/local/go && sudo tar -C /usr/local -xzf ${LATEST_GO}.linux-amd64.tar.gz && echo "export PATH=\$PATH:/usr/local/go/bin:\$HOME/go/bin" >> ~/.bash_profile && source ~/.bash_profile && go version
```
```
#Uninstall GO
sudo rm -rf /usr/local/go && sed -i '/\/usr\/local\/go\/bin/d' ~/.bash_profile && sed -i '/\/go\/bin/d' ~/.bash_profile && source ~/.bash_profile
```

## 6. Node.js
```
#Install Node.js
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.4/install.sh | bash && source ~/.bashrc && nvm install node && nvm use node && node -v
```
```
#Uninstall Node.js
rm -rf ~/.nvm && sed -i '/NVM_DIR/d' ~/.bashrc && source ~/.bashrc
```
```
#Menjalankan Node.js
node namafile.js
```

## 7. Python
```
#Install Python
sudo apt-get update && sudo apt-get install -y software-properties-common && sudo add-apt-repository -y ppa:deadsnakes/ppa && sudo apt-get update && sudo apt-get install -y python3 python3-pip && python3 --version && pip3 --version
```
```
#Uninstall Python
sudo apt-get remove --purge -y python3.* && sudo apt-get autoremove -y && sudo apt-get autoclean
```
```
#Menjalankan Python
python3 namafile.py
```

## 8. Update Sistem VPS
```
sudo apt update && sudo apt upgrade -y
sudo apt install curl tar wget clang pkg-config libssl-dev jq build-essential bsdmainutils git make ncdu gcc jq chrony liblz4-tool -y
```
