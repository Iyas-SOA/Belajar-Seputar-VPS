# Pembahasan
## 1. VPS
### Apa itu VPS
VPS (Virtual Private Server) adalah layanan hosting yang memberi kamu server virtual yang terpisah meski berada di server fisik yang sama dengan pengguna lain. Dengan VPS, kamu punya lebih banyak kontrol dan sumber daya sendiri, sehingga cocok untuk kebutuhan website yang lebih besar dan butuh performa lebih baik dibanding hosting biasa.
### Kegunaan VPS terhadap Node Airdrop
1. Menjalankan Bot Secara Terus-Menerus: VPS memungkinkan bot berjalan 24/7 tanpa gangguan. Karena VPS tidak terhubung langsung dengan komputer pribadi, bot bisa terus aktif tanpa perlu khawatir akan mati atau terhenti karena perangkat pribadi dimatikan atau mati listrik.
2. Kecepatan dan Kestabilan: VPS menyediakan koneksi internet yang lebih cepat dan stabil, yang penting untuk bot yang memerlukan respon cepat, misalnya saat ikut serta dalam airdrop atau transaksi kripto.
3. Menghindari Batasan IP: Dengan VPS, kamu bisa menggunakan IP yang berbeda untuk setiap bot, mengurangi risiko diblokir atau terdeteksi oleh platform yang mengadakan airdrop.
4. Kinerja Lebih Baik: VPS dengan sumber daya yang terdedikasi membuat bot dapat bekerja lebih cepat, menangani lebih banyak permintaan, dan mengurangi lag atau downtime.
5. Privasi dan Keamanan: VPS memberi lebih banyak kontrol terhadap pengaturan keamanan, seperti firewall atau enkripsi, yang penting saat menjalankan bot atau terlibat dalam airdrop yang memerlukan data pribadi atau kripto.
6. Mengelola Banyak Akun: Dengan VPS, kamu bisa menjalankan beberapa bot secara bersamaan tanpa masalah, sangat berguna jika kamu berencana untuk mengikuti banyak airdrop atau transaksi pada waktu yang sama.

## 2. PROXY
### Apa itu Proxy
Proxy itu perantara antara perangkatmu dan internet. Saat kamu browsing pakai proxy, permintaanmu lewat server proxy dulu sebelum sampai ke situs tujuan.
### Kegunaan Proxy terhadap Node Airdrop
1. Menyembunyikan IP Asli – Menghindari deteksi dan pemblokiran dari penyelenggara airdrop yang melarang banyak akun dari satu IP.
2. Mengelola Banyak Akun – Dengan proxy, kamu bisa menjalankan beberapa bot sekaligus tanpa terlihat mencurigakan.
3. Menghindari Rate Limit – Beberapa airdrop atau platform membatasi jumlah permintaan per IP. Dengan proxy, kamu bisa mendistribusikan trafik agar tidak kena batasan.
4. Keamanan Tambahan – Melindungi identitas dan data pribadi saat menjalankan bot atau node.
5. Mengakses Airdrop yang Dibatasi Wilayah – Jika suatu airdrop hanya tersedia di negara tertentu, proxy bisa digunakan untuk mengaksesnya dari lokasi yang diizinkan.

## 3. GIT, DOCKER, GO (GOLANG), NODE.JS & PYTHON
Git, Docker, Golang, Node.js, dan Python adalah teknologi yang sering digunakan dalam pengembangan bot atau node untuk airdrop dan blockchain.
Berikut penjelasannya dalam konteks bot dan node airdrop:
1. Git

Digunakan untuk mengelola dan berbagi kode bot atau node di platform seperti GitHub atau GitLab.
Developer biasanya meng-clone repository proyek airdrop untuk menjalankan node atau bot.

2. Docker

Memudahkan deployment bot atau node dalam container tanpa perlu menginstal semua dependency secara manual.
Banyak proyek blockchain menyediakan Docker image untuk menjalankan node dengan cepat.

3. Golang (Go)

Banyak blockchain seperti Cosmos, Polkadot, dan Ethereum menggunakan Golang untuk membangun node mereka.
Node validator atau full node sering kali berbasis Go.

4. Node.js

Sering digunakan untuk membuat bot otomatis yang berinteraksi dengan API blockchain atau smart contract.
Beberapa bot untuk airdrop menggunakan Node.js karena kemudahan integrasi dengan JavaScript.

5. Python

Digunakan untuk membuat bot airdrop, terutama untuk scrapping data, berinteraksi dengan API, atau mengotomatiskan transaksi di blockchain.
Banyak bot yang menggunakan Web3.py untuk berinteraksi dengan jaringan Ethereum dan EVM.


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

## 4. Docker
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

## 5. GO (Golang)
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
```
#Virtual Environment
python3 -m venv myvenv
```
## 8. Proxy
```
#Format Proxy
socks5://username:password@ip:port
socks4://username:password@host:port
http://username:password@host:port
```
## 9. Update Sistem VPS
```
sudo apt update && sudo apt upgrade -y
sudo apt install curl tar wget clang pkg-config libssl-dev jq build-essential bsdmainutils git make ncdu gcc jq chrony liblz4-tool -y
```
