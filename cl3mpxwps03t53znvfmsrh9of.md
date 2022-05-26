## Yeni Başlayanlar İçin Blockchain #2

### Öğreneceklerimiz

*   Kriptografik hash fonksiyonları (Cryptographic Hash Functions)
*   Private Keys
*   Public Keys
*   İşlemler (Transactions)
*   Dijital imza (Signatures)
*   Bloklar (Blocks)

### Cryptographic Has Functions Nedir?

*Hash, rastgele uzunluktaki bir girdiyi sabit uzunluktaki şifreli bir çıktıya dönüştüren matematiksel bir fonksiyondur. Bu nedenle, ilgili orijinal veri miktarına veya dosya boyutuna bakılmaksızın, benzersiz karma değeri her zaman aynı boyutta olacaktır. Girdinin herhangi bir kısmı değişirse çıktı da ona göre değişecek, random bir sayı alacaktır. Aşağıdaki görsel örnekte olduğu gibi*

*İki farklı girdi aynı çıktı ile sonuçlanmamalıdır. Amacımız hash fonksiyonlarını çarpışmasız(collision) hale getirmek.*

*Hash fonksiyonun bir başka özelliği ise girdi ile çıktı benzer olmamasıdır.*

*Daha iyi anlamak için bu sitede* [*https://guggero.github.io/blockchain-demo/#!/hash*](https://guggero.github.io/blockchain-demo/#!/hash) *denemeler yapabilirsiniz.*

### Private Keys

*Etherium hesabımız için ana şifre olarak düşünebiliriz. Hesaba erişimi ve para göndermemizi sağlar. Bu da demektir ki kimseyle paylaşılmamalıdır. Private Keyler aslında düz bir metindir fakat encryption şifreleme yöntemi ile insanlar ve diğer bilgisayarlar tarafından okunmasını engellemek için şifreli bir hale dönüştürülür.*

### Public Keys

*Private keylerden yaratılır, dolayısıyla public key’e erişmek için private keylere ihtiyacımız vardır. Public Keylerinizi başkalarıyla paylaşmanızda hiçbir sakınca yoktur.*

### Transactions

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1653551615565/BV97SNaMW.png)

*Bu işlemle ilgili tek sorun, bu işlemi yapan kişinin parayı gönderen doğru adres olduğuna güvenmek zorunda olmamız. Bu sorunu da dijital imzalar(signatures) ile çözüyoruz.*

### Digital Signatures

*Özel bir anahtar kullanarak bir mesajı veya belgeyi imzalama işlemidir. Mesaj veya belge önce özel anahtar kullanılarak şifrelenir ve ardından şifrelenen mesaj veya belge alıcıya gönderilir. Alıcı daha sonra göndericinin açık anahtarını kullanarak mesajın veya belgenin şifresini çözer.*

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1653551617130/OXuT6lesZ.png)

*Alice Bob’a 1 BTC göndermek istiyorsa, private keyini kullanarak 1 BTC giriş harcayan bir işlemi imzalamalı ve ağdaki düğümlere göndermelidir. İmzalama için kullanılan private anahtara imza anahtarı, public anahtara ise doğrulama anahtarı adı verilir.*

### Blockchain Nedir ve Önemi?

*Tüm işlemlerin kaydını tutacağı için blockchain i banka işlem kayıtları olarak düşünebiliriz. Blockchain’in en önemli özelliklerinden biri merkezi olmamasıdır. Bu bir banka tarafından kontrol edilmediği, tek bir kişi tarafından kontrol edilmediği anlamına gelir. İnternetteki rastgele kişiler tarafından özel olarak sahip olunan bir bilgisayar ağı tarafından kontrol edilir. Bunun önemli olmasının sebebi; bir kişi veya bir kuruluş veya bir varlık tarafından merkezi olarak sahip olunduğu anda bu kişilerin onunla yozlaşmış veya kötü niyetli bir şey yapma ve gücüne sahip olmalarıdır. Örneğin banka hesabınız varsa bunun olma olasılığı düşüktür ancak teorik olarak hükümet bankayı tüm fonlarınızı devretmeye zorlayabilir. Belki vergi falan ödemen gerekir. Fikir ne olursa olsun bunu kontrol eden organizasyon var. Ve böylece herhangi bir zamanda bu merkezi otorite içeri girebilir ve defterdekileri, hesap bakiyesini değiştirebilir. Ama bir blockchainden bahsettiğimizde bu mümkün olamaz. Çünkü bu bir kişiye veya kuruluşa ait değil. Ağa katkıda bulunan dünyadaki tüm bilgisayarlar tarafından kullanılıyor ve kontrol ediliyor.*

### Mining Blocks

*Her işlem gönderdiğinizde, genellikle çok küçük miktarda bir ücret ödemeniz gerekir(fees) ve bu ücret, bir bloğu güvenceye almaya ve doğrulamaya çalışan madencilere verilecektir. Dünyanın her yerinde bulunan bilgisayarlar yani dünyanın her yerinde etherium blok zincirine bağlı bu adamlardan bir grup var. Artık her yeni blok oluşturulduğunda ve tüm işlemler eklendiğinde, her madenciye gönderiliyor. Yani tüm bu madenciler ağdaki bir tür düğümdür(node). İşlemlerin mevcut bloğa eklenmesini bekliyorlar. Bu olduğunda madencilerin yaptığı şey bloğu kazmaya çalışmaktır. Blok madenciliği bazı hesaplamalar yapmaktan özellikle çok zaman alıcı olan ve bir dakika içinde ulaşacağımız bir bloğun karmasını yapan bir sayıyı tahmin etmeye çalışan bazı çok zor hesaplamalardan oluşur. Şimdi bunu bu madenciler için yapmanın amacı, eğer belirli bir sayıyı tahmin edebilirlerse bloğu başarıyla kazarlar ve onlara ödül verilir. Bu ödül iki şeyden oluşur; Block Reward ve Fees.*