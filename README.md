# PowerPool
![Ekran görüntüsü 2023-08-21 190255](https://pbs.twimg.com/media/F23kSdDWsAE6uPA?format=png&name=small)
## Ödüllü Testnete Katılım
* Ödüllü Testnete katılmak için [BURADAN](https://twitter.com/CoinHuntersTR/status/1688258870689329152) formu doldurmayı UNTUMAYIN!
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
* Hangi tip bilgisayar kullanıyorsanız ona uygun olmalı.

## WireGuard Arayüzü
* Bu komut ile verilecek olan bilgileri bir yere not edin.
```
dappnode_wireguard
```
![Ekran görüntüsü 2023-08-21 190255](https://640488913-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MJqrcOKqAefjDPcq_0d%2Fuploads%2FiWtiBVajYPYCcmbKmtL6%2Fimage.png?alt=media&token=39a5fe23-c5d0-42e5-8c5b-9587e72fb39d
)
* Buna benzer bir çıktı alıyoruz. Bu çıktıyı bir yere kayıt edelim.
* WireGuard açıyoruz.
![tunel](https://github.com/CoinHuntersTR/PowerPool/assets/111747226/0aa43878-6e51-4636-a962-4af7b49fb451)
* Buradan boş bir tunel açıp, gelen bilgileri siliyoruz ve kurulum yaparken aldığınız bilgileri buraya ekleyip, isim verip etkinleştiriyoruz.
* Etklinleştirme işlemini yaptıktan sonra;
* [BURADAKİ](http://my.dappnode/) adresten kurduğumuz node arayüzüne erişiyoruz.
* İlk girişte bize username soracak admin yazıyoruz.
* Şifremizi beliyoruz.
* DİKKAT!! bu adımları tamamladıktan sonra size bir kod verecek şifrenizi yenilemeniz gerektiğinde bu koda ihtiyacınız olacak o nedenle kayıt etmeyi unutmayın.
* Tekrar VPS panelimize dönelim.
   
## Gerekli Yazılımları yüklüyoruz.

```
sudo apt install nodejs
```
```
sudo apt install npm
```
```
sudo apt install git
```

## PowerPool indiriyoruz
```
git clone https://github.com/powerpool-finance/powerpool-agent-v2-compose
```
```
cd powerpool-agent-v2-compose
```
## npm yüklüyoruz

```
npm i
```
## Bu Bölüme DİKKAT
* İki farklı metamask adresine ihityacımız var.
* Birinci adresimiz Admin adres olacak. (Bu adrese test tCVP ve Sepoila ETH istememiz gerekiyor.)
* İkinci adres Worker adresi olacak. Worker adresin Private key'ni alıyoruz ve bir yere not ediyoruz.
* Metamask Private key'inizi;
 ![metamask](https://user-images.githubusercontent.com/111747226/214062437-69e144d9-528f-4a17-b46a-a747c1d5284c.png)
  
