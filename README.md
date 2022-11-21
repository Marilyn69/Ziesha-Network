<h1 align="center"> ℤiesha Network | The Groth Testnet </h1>

![Ziesha4 (1)](https://user-images.githubusercontent.com/101149671/203003235-f72d7629-d029-45de-814c-397fc6329794.jpg)

<h1 align="center"> Selamlar, Ziesha'nın test ağı başladı, bu testnette neler yapacağız? </h1>

## Bu testnetnette yapacaklarımız ve önemli konular:

* Bu testnette isteyen madenci olabilecek isteyen node kurabilecek (ikisi de ödüllü)
* Çok uzun süredir bir PoW chainin testnetine katılmıyorduk ve madenci olmuyorduk. (En son geçen sene IronFish) 
* Hem öğrenmeniz için önemli hemde diğer testnetlerden (cosmos, docker) sıkılmış birisi olarak farklı testnetlere ihtiyacımız var.
* Madenci olmanın 3 yolu var: 1- Solo madencilik, 2- Madenci havuzuna dahil olup madenci olmak, 3- Madenci havuzunu oluşturmak
* Node kuranlar ile madenciler iki ödülüde alır mı? -Evet, node ödülü alırsın ve ağda kazıdığın tokenler kadar (sayılar random) ödül alırsın.
* En altta node kurduktan sonra madencilik hakkında rehberler olacak.
* Testnet 43200 blokta sonlanacak.
* Nodu güncel olmayan cüzdanlar ödül alamayacak.
* Node rehberi ile başlıyoruz:

## Sistem gereksinimleri:

```
2 CPU
2 RAM
20 SSD
```

## Sunucuzda daha önce Ziesha kurduysanız, eski adı Zeeka, silelim onu:
* Bir şey kaydetmenize gerek yok
```
systemctl stop  zeeka zoro uzi
systemctl disable zeeka zoro uzi
rm -rf /root/bazuka
rm -rf /root/.bazuka-debug
rm -rf /root/zoro
rm -rf /root/uzi
rm ~/.bazuka.yaml
```
## Kurulum:
* Komutları tek tek girin:
```
sudo apt-get update && sudo apt-get upgrade
sudo apt install -y build-essential libssl-dev cmake
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
git clone https://github.com/ziesha-network/bazuka
source "$HOME/.cargo/env"
cd bazuka
cargo install --path .
```

## Nodu başlatacağız:
* Bu komutu girdikten sonra 12 kelime verecek size, not edin lütfen.
```
bazuka init --network groth --bootstrap 65.108.193.133:8765
```

* Daha önce madenci olduysanız 12 kelimenizi import edebilirsiniz bu komutla:
* Aynı zamanda node taşımak isterseniz eski mnemoniclerinizi (12 kelime) girmeniz yeterli, otomatik node taşınır.
```sh
bazuka init --network groth --bootstrap 65.108.193.133:8765 --mnemonic "Eski MNEMONICLER"
```

## Şimdi nodu çalıştıracağız:

* Tırnak içersine discord adınızı girin
* Ziesha'nın discordunda olmak zorundasınız: [Link](https://discord.gg/zieshanetwork)

```
apt install screen
screen -S bazuka
```

```sh
bazuka node start --discord-handle "YOUR DISCORD HANDLE"
```

## Çalıştığını nasıl anlarız?

* Görselde ki gibi olacak
* Ama bu görsel ağ başlamadan önce ki hali
* Siz ağ başladıktan sonra kuracağınız için height ve acitve nodes sayısı artacak
* Artmazsa sorun vardır. (ağ başlar başlamaz artmaz, bir kaç blok üretildikten sonra)

![image](https://user-images.githubusercontent.com/101149671/203009309-5f9d033e-453f-494a-8a49-39a6f41f8ffb.png)




























































