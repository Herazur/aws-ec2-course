## Firewall Nedir? Firewall türleri nelerdir ve ne işe yarar?

Firewall(Güvenlik Duvarı), internetten gelen bilgileri filtreleyerek yetkisiz erişimin özel bir ağa girmesini önlemek için tasarlanmış bir sistemdir. Firewall istenmeyen trafiği engeller ve istenen trafiğe izin verir. Dolayısıyla bir firewall’ın amacı, özel bir ağ ile genel internet arasında bir güvenlik duvarı bariyeri oluşturmaktır. Çünkü internette, zarar vermek için özel bir ağa girmeye çalışan bilgisayar korsanları ve kötü niyeli trafik her zaman olacaktır.

Özel bir ağ ile genel internet arasında bir güvenlik bariyeri oluşturur.

Firewall, bunu önlemek için ağdaki ana bileşendir ve firewall içeride çok sayıda bilgisayar ve sunucu bulunan büyük bir kuruluş için özellikle önemlidir. Çünkü bir bilgisayar korsanının girip bu organizasyonu tamamen bozabileceği tüm bu cihazların internetteki herkes tarafından erişilebilir olmasını istemiyoruz.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1653551598686/iDf2iIApi.png)

Güvenlik duvarı özellikle büyük kuruluşlar için önemlidir.

Bilgisayar ağlarında kullanılan firewall, bir bina yapısında bir firewall’ın nasıl çalıştığına çok benzer.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1653551600272/wSDVqpK1p.png)

Bina Yapısı Firewall

Aslında firewall kelimesi buradan geldi. Bir bina yapısındaki firewall, bir bariyer sağlar, böylece gerçek bir yangın durumunda, bir binanın her iki tarafında, yangını kontrol altında tutmak ve diğer tarafa yayılmasını önlemek için firewall orada bulunur. Yani yangının tüm binayı yok etmesini önlemek için firewall var. Ama firewall burada olmasaydı, yangın diğer tarafa sıçrayacak ve tüm bina yıkılacaktı. Firwall diğer tarafına yayılmadan ve özel bir ağa zarar vermeden önce zararlı etkinliği durdurur.

### Firewall Kuralları

Firewal, gelen ağ trafiğini filtreleyerek çalışır ve kurallarına göre bir ağa girmesine izin verilip verilmediğini belirler, bu kurallar access control list olarak da bilinir. Bu kurallar özelleştirilebilir ve ağ yöneticisi tarafından belirlenir. Yönetici yalnızca nelerin ağa girebileceğine değil, aynı zamanda nelerin ağdan ayrılabileceğine de karar verir.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1653551602173/G_T8mLNXz.png)

Bu kurallar izin verir veya vermez. Örnek olarak, burada bir güvenlik duvarının erişim kontrol listesinde bazı kurallarımız var. Bu firewall tarafından izin verilen veya reddedilen IP adreslerinin bir listesini gösterir.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1653551603831/wiUd4CODa.png)

Ve görebileceğiniz gibi, bazı IP adreslerinden gelen trafiğin bu ağa girmesine izin veriliyor.. ancak bir IP daresinden gelen trafik reddedildi. Dolayısıyla, bu IP adresinden gelen trafik bu ağa girmeye çalışırsa, firewall ayarlanan kurallar nedeniyle firewall bunu reddetecektir. Ancak kurallar izin verdiği için diğer IP adreslerine erişim verilir. Firewall yalnızca IP adreslerine dayalı kurallar oluşturmaz, aynı zamanda alan adlarına, protokollere, programlara, bağlantu noktalarına ve anahtar sözcüklere dayalı kurallar da oluşturabilir. Diyelim ki bu örnekte, firewall kuralları, bağlantı noktası numarlarına göre erişimi kontrol ediyor ve diyelim ki kurallar 80, 25 ve 110 numaralı bağlantı noktalarını kullanan gelen verilere izin verdi ve bu bağlantı noktalarını kullanan verilere bu ağa erişim izni verildi.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1653551605321/kHzES_pPM.png)

Böylece, bu bağlantı noktalarını kullanan herhangi bir gelen veri firewall’dan geçebilir. Ancak bu firewall da kurallar, 23 ve 3389 numaralı bağlantı noktalarını kullanan herhangi bir veriyi reddetti. Bu nedenle, bu bağlantı noktası numarlarını kullanan herhangi bir gelen veri, firewall erişimi reddedecek ve firewall’ı geçemeyecektir. Yani kısaca güvenlik duvarları temelde bu şekilde çalışır.

### **Firewall Tipleri**

#### 1\. Host-based firewall

Bu bir yazılım güvenlik duvarıdır ve yalnızca o bilgisayarı korur. Birçok virüsten koruma programı, ana bilgisayar tabanlı bir güvenlik duvarı (host-based firewall) ile birlikte gelir.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1653551606744/L9ILq4sg5.png)

#### 2\. Network-based firewall

Ağ tabanlı bir güvenlik duvarı, donanım ve yazılımın birleşimidir ve ağ katmanında çalışır. Özel bir ağ ile genel internet arasında yerleştirilir. Ancak, yalnızca o bilgisayarı koruduğu host-based firewall’ın aksine, network-based firewall tüm ağı korur ve bunu tüm ağa uygulanan yönetim kuralları aracılığıyla yapar böylece herhangi bir zararlı faaliyet bilgisayarlara ulaşmadan durdurulabilir.

Ağ tabanlı güvenlik duvarları, çoğunlukla büyük kuruluşlar tarafından kullanılan bağımsız bir ürün olabilir. Ayrıca, bir yönlendiricinin bir bileşeni olarak yerleşik olarak da yerleştirilebilirler. Bu, birçok küçük kuruluşun güvendiği şeydir. Veya bir hizmet sağlayıcının bulut altyapısında da konuşlandırılabilirler. Artık birçok kuruluş hem ağ tabanlı hem de ana bilgisayar tabanlı güvenlik duvarlarını kullanacak.. Tüm ağı bir bütün olarak korumak için ağ tabanlı bir güvenlik duvarı kullanacaklar… ve ayrıca bireysel olarak ana bilgisayar tabanlı güvenlik duvarlarını kullanacaklar. Bilgisayarları ve sunucuları için koruma. Bunu yaparak, maksimum koruma sağlayacaktır. Çünkü eğer zararlı veriler ağ güvenlik duvarından geçerse.. her bilgisayardaki ana bilgisayar tabanlı güvenlik duvarları onu durdurmak için orada olacaktır.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1653551608432/1zGZgdgJ0.png)