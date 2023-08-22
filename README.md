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
* Birinci adresimiz Admin adres olacak. (Bu adrese test tCVP ve Sepoila ETH istememiz gerekiyor.) [Sepoila ETH Faucet](https://sepoliafaucet.com/)
* İkinci adres Worker adresi olacak. Worker adresin Private key'ni alıyoruz ve bir yere not ediyoruz.
* Metamask Private key'inizi aşağıdaki resimdeki işlemleri yaparak bulabilirsiniz.
 ![metamask](https://user-images.githubusercontent.com/111747226/214062437-69e144d9-528f-4a17-b46a-a747c1d5284c.png)
  
* test tCVP için özel telegram grubundan talep edebilirsiniz.
* "" dahil silip privatekey ve kendi belirlediğimiz şifreyi yazıp çalıştırıyoruz.
  
```
node jsongen.js "workerprivatekey" "şifre"
```
* Bu adımları tamamladıktan sonra suncumuz için
![utc](https://github.com/CoinHuntersTR/PowerPool/assets/111747226/8943f87f-b54f-4a18-ae11-600bf865307c)
*Resimdeki gibi UTC ile başlayan dosyayı bilgisayarımıza indiriyoruz.
## Dappnode içine gerekli paketleri yüklüyoruz.
* [Prysm Sepolia DAppNode package](http://my.dappnode/#/installer/%2Fipfs%2FQmT2vSKsKVTs7oFxYnnzb8cpWiKnMDvPLy1qnaLWfEfVkD)
* Aşağıdaki gibi ayarları yapıp sonrasında, install diyoruz.
   ![Prysm](https://user-images.githubusercontent.com/111747226/262366920-8e1bda9a-6b97-4139-993d-b60c2457c0c6.png)
* [Geth Sepolia DAppNode package](http://my.dappnode/#/installer/%2Fipfs%2FQmNy6zTZM9LfHomWJpNYFWX6kJqz9Jgm5eragJagMwc4jk)
 ![Ekran görüntüsü 2023-08-21 150925](https://github.com/CoinHuntersTR/PowerPool/assets/111747226/65185640-7abd-4eec-b1d8-dd843a18d9ba)
* [PowerAgent DAppNode package](http://my.dappnode/#/installer/%2Fipfs%2FQmWfQRMJmp9JmdPknMLpKsSNn9AErmp6WJhZ4jme4njK5M)
![Ekran görüntüsü 2023-08-21 151013](https://github.com/CoinHuntersTR/PowerPool/assets/111747226/463f93ef-4149-48f4-9542-245ce7c7347d)
*PowerAgent Dappnode kurarken sizden worker adresi isteyecek onu ekliyoruz. 
* Biraz önce indirdiğimiz dosyayı yüklüyoruz.
* şifre worker private key yüklerken yazdığımız şifreyi ekliyoruz.
* web stock RPC adresine ws://sepolia-geth.dappnode:8546 bunu ekliyoruz.
* kayıt edip yüklenmesini bekliyoruz.
* Sepolia Geth senkronize olmasını bekliyoruz. Bu adımları tamamladıysak diğer bölüme geçelim.

[BURADAN](https://sepolia.etherscan.io/address/0xD5134EcD90EB63276aF2Fca897cC04D845AfD74f#writeContract) adresine ulaşıyoruz. 
* Admin olan Metamask cüzdanımızı bağlıyoruz ve "approve" fonksiyonunu açıyoruz.
* spender (address) bölümüne aşağıdaki adresi ekliyoruz.
```
0xc8E864f12c337Bdf6294a3DCeE0E565D2B1B4d90
```
* amount (uint256) bölümüne ise 1000 tCVP için yazıyoruz ve Write tuşuna basıyoruz. Cüzdana gelen bildirimleri onaylıyoruz.
```
1000000000000000000000
```
![kontrat açma](https://github.com/CoinHuntersTR/PowerPool/assets/111747226/3a4e2181-961e-498b-995a-3c0d686cbcf8)

## Stake işlemini yapıyoruz.
[BURADAN](https://sepolia.etherscan.io/address/0xc8E864f12c337Bdf6294a3DCeE0E565D2B1B4d90#writeContract) kontrat adresine ulaşıyoruz.
* Admin metamask cüzdanımızı bağlıyoruz. ve "registerAsKeeper" fonskiyonunu buluyoruz.
* worker_ (address) bölümüne worker adresini ekliyorsunuz.
* initialDepositAmount_ (uint256) bölümüne de yukarıdaki 10000 ile devem eden sayıları ekliyoruz.
* Write butonuna basıyoruz ve cüzdanımıza gelen bildirimleri kabul edip onaylıyoruz.
![keeper](https://github.com/CoinHuntersTR/PowerPool/assets/111747226/f50ec67d-15fb-407f-9b88-bbe4bf77e968)
## Notlar
* Sepolia Geth senkronizasyonu tamamlandıktan sonra Dappnode panelimizden Packages bölümüne geliyoruz ve PowerAgent'i restart yapyıoruz.
* [BURADAN](https://app.powerpool.finance/#/sepolia/ppv2/my-keepers) admin metamask cüzdanınızı bağlayarak kendi keeper ID'nizi öğrenebilirsiniz.
  
