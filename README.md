# Mawari

![GYahA_raUAA2i5y](https://github.com/user-attachments/assets/1bad4a09-6812-4f18-8ac8-723c73ffd8a1)

| X        | Minimum              |
|------------------|----------------------------|
| **CPU**          | 4++ |
| **RAM**          | 5++ GB                    |
| **Disk**      | 50 GB+ NVME GB SDD                   |
| **Internet Speed**      | 100 Mbps (1 Gbps+ recommended) |


| Server         | Link              | Features |
|------------------|----------------------------|----------------------------|
| **Contabo**          | [Link](https://www.dpbolvw.net/click-101330552-12454592)                     | Cheap / Paypal  |
| **NetCup**          | [Link](https://www.netcup.com/en/?ref=261820) | Cheap / Paypal |

## Proje Sosyal Medyası : 
- Twitter : [https://x.com/multisynq](https://x.com/mawariXR)

## Web İşlemleri

- Yeni Metamask Açtım - Burner Cüzdan Kullandım.
- Faucet : https://hub.testnet.mawari.net/

<img width="1023" height="301" alt="image" src="https://github.com/user-attachments/assets/0fbb79c7-5dd7-46ab-84a5-a724c5820c84" />

- Mint ; 
- Link : https://testnet.mawari.net/mint  3 Tane Mint Yapıyoruz.
<img width="1294" height="874" alt="image" src="https://github.com/user-attachments/assets/bc3efc75-ffb3-4a41-8ede-6f6a7626c3c4" />


## Server Güncelleme : 

```bash
sudo apt update -y && sudo apt upgrade -y
```
## Paketleri İndirelim :

```bash
sudo apt install htop ca-certificates zlib1g-dev libncurses5-dev libgdbm-dev libnss3-dev tmux iptables curl nvme-cli git wget make jq libleveldb-dev build-essential pkg-config ncdu tar clang bsdmainutils lsb-release libssl-dev libreadline-dev libffi-dev jq gcc screen file unzip lz4 -y
```

## Docker ; 

```bash
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg
echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
sudo apt-get update
sudo apt-get install docker-ce docker-ce-cli containerd.io -y
docker version
```

## Docker Compose : 

```bash
VER=$(curl -s https://api.github.com/repos/docker/compose/releases/latest | grep tag_name | cut -d '"' -f 4)
curl -L "https://github.com/docker/compose/releases/download/$VER/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
chmod +x /usr/local/bin/docker-compose
docker-compose --version
```

## Docker User

```bash
sudo groupadd docker
sudo usermod -aG docker $USER
```

## Dosya / Konfigirasyon ; 
```bash
export MNTESTNET_IMAGE=us-east4-docker.pkg.dev/mawarinetwork-dev/mwr-net-d-car-uses4-public-docker-registry-e62e/mawari-node:latest
```

- Burada Cüzdan Adresi Mint Yaptığınız Faucet Aldığınız Adres ile degistirin

```bash
export OWNER_ADDRESS=0xbenidegistircuzdanadresingelsin
```

- Örnek ; 

<img width="1079" height="81" alt="image" src="https://github.com/user-attachments/assets/cf155243-086b-45ff-8691-085d35b89d24" />


## Çalıştırma ;
```bash
mkdir -p ~/mawari && docker run -d --pull always -v ~/mawari:/app/cache  -e OWNERS_ALLOWLIST=$OWNER_ADDRESS $MNTESTNET_IMAGE
```

- Örnek ; 

<img width="1057" height="182" alt="image" src="https://github.com/user-attachments/assets/c7781b16-b55e-4c15-8548-fea1dc18dba4" />

## Genel Kontrol ;

- ID Alalın ; 

```bash
docker ps -a
```

<img width="885" height="71" alt="image" src="https://github.com/user-attachments/assets/0ec0f8bd-b3a5-4ad6-b777-0d8520b8dfdd" />

- Container ID Görünen kısımı resimdeki gibi sizdeki Mawari'nin ID'si ile değiştiriyoruz.

```bash
docker logs -f containerid
```

- Örnek "root@provider:~# docker logs -f ce37cc0c241e"


<img width="1165" height="539" alt="image" src="https://github.com/user-attachments/assets/e31b16e6-11aa-49e9-a0ff-baf3fa7fdb7a" />

- CTRL C İle logları durdurup yukarı doğru çıkın gösterdiğim bölüme erişin.
- Burner Wallet Adresini Kopyalıyoruz. O adresi kullanacağoz.
- Ayrıca Faucet almıştık cüzdan adresimize BURNER Adresede Kendimiz token yolluyoruz. 2 Tane Token veriliyor 1 Tanesi ona gönderiyoruz.
- Delege Yok Demesi normal, Delege Yapacağız.

## Delege / Node Kaitf Etme ; 

- Link : https://app.testnet.mawari.net/licenses

<img width="1358" height="821" alt="image" src="https://github.com/user-attachments/assets/c5cd4c86-924b-4c24-b90d-dc13268e5d9e" />

- 3'ünü Seçip Delegate'e basıyoruz.
- Yukarıda Burner Wallet'i kopyalamıştık onu yapıştırıp Delegate Tuşuna basıyoruz ; 

<img width="1383" height="817" alt="image" src="https://github.com/user-attachments/assets/f13574d3-69cb-4a6e-9dc8-c3ea74a9ac6b" />

- Cüzdan Onayı ; 

<img width="368" height="599" alt="image" src="https://github.com/user-attachments/assets/b3190ad3-21d4-4f41-b267-b015086dd75b" />

