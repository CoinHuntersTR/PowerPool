# PowerPool
![Ekran görüntüsü 2023-08-21 190255](https://github.com/CoinHuntersTR/PowerPool/assets/111747226/a3c17b1b-4232-49ef-bd8a-719b32b11ae7)
## Ödüllü Testnete Katılım
* Ödüllü Testnete katılmak için [BURADAN]() formu doldurmayı UNTUMAYIN!
* Empowerchain [DİSCORD](https://discord.gg/5W5B2xTzzT) kanalına katılalım.

## Kurulum Öncesi Notlar
### Testnete seçilmediyseniz aşağıdaki adımları yapmanıza gerek yok.
### Bu adımlar testnete katılmaya hak kazananlar için hazırlanmıştır.

## Sistem gereksinimleri:
NODE TİPİ | CPU     | RAM      | SSD     |
| ------------- | ------------- | ------------- | -------- |
| PowePool | 4          | 8        | 200  |
 

![hetzner](https://github.com/CoinHuntersTR/EmpowerChain/assets/111747226/46d2e1ea-0714-4061-b5a2-476be023cfd0)

* Hetzner için bu gereksinimleri almka yeterli olacaktır.
Hetzner kaydınız yok ise [BURADAN](https://hetzner.cloud/?ref=ha9qP7tGjvcR) linke basıp 20€ değerinde ödül kazanıp, testnete katılabilirsiniz.

## Güncellemeleri yapıyoruz.
```
sudo apt update
```

```
sudo apt update
```


## Dappnode Kurulumu
```
sudo wget -O - https://prerequisites.dappnode.io | sudo bash
```
```
sudo wget -O - https://installer.dappnode.io | sudo bash
```

## Profili açıyoruz.
```
source /usr/src/dappnode/DNCORE/.dappnode_profile
```
```
dappnode_status
```

## WireGuard İndiriyoruz.
[BURADAN](https://www.wireguard.com/install/)
indiriyoruz ve bilgisayarımıza yüklüyoruz.

## Cüzdan Oluşturma;
```
empowerd keys add cüzdanadi
```
* "cüzdanadi" bölümüne istediğiniz bir isim verebilirsiniz.,
*  Cüzdanınızı oluşturduktan sonra size verilen gizli kelimelerinizi ve cüzdan adresinizi bir yere not etmeyi unutmayın.

## Sync Kontrolü
* False dönene kadar başka işlem yapmanıza gerek yok!
* False döndükten sonra validator kurulumu yapıyoruz. Validator kurulumu için aşağıdaki notları okumayı unutmayın!
* [BURADAN](https://empower.explorers.guru/) explorer giderek blok sayılarını kontrol edebilirsiniz.
```
empowerd status 2>&1 | jq .SyncInfo
```
![soncu](https://user-images.githubusercontent.com/111747226/243185688-d0a0386f-4c65-4b4a-a16c-476e36ff6036.jpg)

## Önemli Notlar.
* Şuan Faucet yok bu nedenle bu bölümü faucet açıldıktan sonra yapacaksınız.
* Şuan node kurup sync olmayı bekliyoruz. Faucet açıldıktan sonra aşağıdaki bölüme devam edeceğiz.

## Validator Oluşturma;

* "cüzdanadi" yazan yere kendi cüzdanadınızı yazacaksınız.
* "twitter adresinizi ekleyebilirsiniz." yazan yere " kalacak şekilde twitter adresinizi ekleyebilirsiniz.
```
empowerd tx staking create-validator \
  --amount=100000umpwr \
  --pubkey=$(empowerd tendermint show-validator) \
  --moniker=MonikerAdiniz \
  --details="discord kullanıcı adınız" \
  --website="twitter adresiniz olabilir" \
  --chain-id=circulus-1 \
  --commission-rate=0.10 \
  --commission-max-rate=0.20 \
  --commission-max-change-rate=0.01 \
  --min-self-delegation=1 \
  --from=cüzdanadi \
  --gas-prices=0.1umpwr \
  --gas-adjustment=1.5 \
  --gas=auto \
-y
```
