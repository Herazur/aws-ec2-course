## Yeni Başlayanlar İçin Blockchain #3

### Dış ödemeyi al fonksiyonu

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1653551537882/A6jLr6rPH.png)

### Bu sözleşmeye para göndermek için

Bakarsanız miktarın düştüğünü, biraz gas ücreti çektiğini görebilirsiniz

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1653551539049/qvjaX40VS.png)

### Sözleşmenin bakiyesini fonksiyon ile öğrenme

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1653551540344/sk3okgQYU.png)

Yeni Solidty versiyonda adresi manuel olarak eklemeniz gerekebilir.

Deploy edip getBalance diyelim ve 0 bakiye olduğunu görelim.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1653551541672/TKwgcLwHtv.png)

Sonrasında Value miktar ekleyip (ben 5 yazdım) Recieve e basalım yine getBalance dediğimizde bakiye olduğunu görelim.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1653551542998/OIDxKWNYN.png)

### Ether gönderen son kişinin adresini takip etmek

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1653551544445/j_MlJ8ymq.png)

1 ether recieve edelim ve lastSender a basıp ether gönderen son adresi görelim

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1653551545717/lNvOG5pQV.png)

Ether gönderdiğiniz ACCOUNT adresini değiştirip tekrar denediğinizde adresin değiştiğini gözlemleyebilirsiniz.

### Etheriumu sözleşmeden farklı bir etherium hesabına ether göndermek

Şimdi yapacağımız bir ether hesabından 1 ether alıp (recieve) aldığımız 1 ether i de başka etherium adresine göndereceğiz. Yeterli bakiyemiz yoksa bize hata döndürecek.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1653551547011/Sgf_QcH29.png)

Öncelikle etherium alacağımız etherium hesabına geçip value 1 yapalım ve 1 etherium recieve edelim.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1653551548318/Els9nttTOz.png)

Sonrasında göndereceğimiz etherium hesabına geçiş yapıp adresini kopyalayalım.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1653551549461/YLsv__nvV.png)

Adresi Pay kısmına yapıştıralım ve Pay a basalım

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1653551550697/bHngngRZg.png)

Gas ücreti ödediğimiz için tam bir rakam vermeyecektir fakat işlem başarılı.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1653551551886/A4F5Rk6rY.png)