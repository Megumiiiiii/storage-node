<div align="center">
 
# CESS Storage Node

</div>

<div align="center">

[![](https://img.shields.io/static/v1?label=Sponsor&message=%E2%9D%A4&logo=GitHub&color=%23fe8e86)](https://github.com/sponsors/Megumiiiiii)

 <img align="top" src="https://komarev.com/ghpvc/?username=Megumiiiiii&color=ff69b4&style=plastic&label=Visitors" height='35'/>

</div>

#

<div align="center">
  
## ${\color{violet} COPAS \space SERTAIN \space SUMBER \space SU}$

### ${\color{violet} DIKIRA \space BIKIN \space GINIAN \space GAK \space PERLU \space USAHA \space APA}$ 

</div>

## Official Links
- [Docs](https://docs.cess.cloud/cess-build-book/storage-miner)
- [Discord](https://discord.gg/mj3u57BkDv)
- [Twitter](https://twitter.com/CESS_Storage)

#

## Spek Minimal

| Spek | Ukuran |
|----------|----------|
| CPU | 4 |
| RAM | 8 GB |
| SSD | 100 GB |
| Bandwith | 5 MB |

## Setup Awal

1. Buatlah 2 wallet di [Polkadot](https://polkadot.js.org/apps/?rpc=wss%3A%2F%2Ftestnet-rpc1.cess.cloud%2Fws%2F#/accounts)
2. Lalu ambil faucet [DISINI](https://testnet-faucet.cess.cloud/)
3. Wallet pertama digunakan untuk menerima hasil mining
4. Wallet kedua digunakan untuk mining

### Buka Port

```
sudo ufw allow ssh; sudo ufw allow 4001; sudo ufw allow 15001; sudo ufw enable
```

### Install Docker ( Skip kalo udah )

```
sudo apt update; sudo apt upgrade -y
```

```
sudo apt-get update && sudo apt install jq git && sudo apt install apt-transport-https ca-certificates curl software-properties-common -y && curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add - && sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu focal stable" && sudo apt-get install docker-ce docker-ce-cli containerd.io docker-compose-plugin
```

### Install CESS

```
mkdir -p /opt/cess
git clone https://github.com/CESSProject/cess-nodeadm
cd cess-nodeadm
git checkout tags/v0.4.4
./install.sh
```

### Set Config

- Paste ini

```
cess config set
```

- Ketik `storage` kemudian enter

- Masukan IP VPS

- Paste address dari wallet pertama

- Lalu paste pharse dari wallet kedua

- Ketik `/opt/cess`

- Terkahir, isi dengan `100`

## Start Node

```
cess reload
```

lalu

```
cess start
```

### Daftar Command

- Cek logs chain

```
docker logs -f chain
```

- Cek logs bucket

```
docker logs -f bucket
```

- Cek status

```
cess bucket stat
```
## Jika ada Update

- Versi terakhir node bisa cek [DISINI](https://github.com/CESSProject/cess-nodeadm/tags)

### Cara Update

#### Stop dulu

```
cess stop
cess down
```

#### Hapus

```
cess purge
```

#### Hapus folder dan file yang lama

Contoh akan menghapus versi 0.3.1
```
rm -rf cess-nodeadm
```

#### Setelah itu mulai kembali dari langkah [Set Config](https://github.com/Megumiiiiii/storage-node/blob/main/README.md#set-config)

## ⚠️ Jika ingin menghapus node ⚠️

```
cess down; cess purge
docker rmi cesslab/cess-bucket; docker rmi cesslab/cess-chain; docker rmi cesslab/config-gen; docker rmi containrrr/watchtower
```

#

<div id="header" align="center">
  <img src="https://media.giphy.com/media/v1.Y2lkPTc5MGI3NjExMzNmZTIxZmE3ZmY3MzRiMDcwNDJhYTQ5ZmNlY2YxMWE1OWIyYmVkNSZlcD12MV9pbnRlcm5hbF9naWZzX2dpZklkJmN0PWc/mVBlqOD4ra9jQiI3cC/giphy.gif" height="125" width="420"/>
</div>

