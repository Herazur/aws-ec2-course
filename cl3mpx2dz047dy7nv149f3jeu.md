## NAS ve SAN arasındaki fark nedir?

NAS, (Network Attached Storage) ağa bağlı depolama anlamına gelir. Verileri, ağınızdaki tüm cihazlarınızdan erişilebilecek merkezi bir yerde depolamak istiyorsanız, bunu ağa bağlı bir depolama cihazı kullanarak yapabilirsiniz.

Evlerde ve küçük orta ölçekli işletmeler.

NAS, verileri depolamak için kullanılan bir depolama cihazıdır ve verileri depolamaktan başka hiçbir şey yapmaz. Yedeklilik için RAID yapılandırmasında birden fazla sabit sürücüye sahip olacak bir kutudur   
ve ayrıca doğrudan bir switch veya router’a bağlanacak bir ağ arayüz kartına sahip olacaktır, böylece verilere bir ağ üzerinden erişilebilir. NAS tipik evlerde kullanılan paylaşılan sürücü olarak erişilebilir ve ayrıca orta ölçekli işletmelerce kullanılmaktadır.

NAS’ın ana dezavantajlarından biri, tek bir arıza noktasına sahip olmasıdır. Örnek olarak, bir bileşenin, NAS’daki güç kaynağının arızalanması gibi bir arıza durumunda. O zaman diğer tüm cihazlar, verilerine erişemeyecek.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1653551570325/VsT9X7Tde.png)

SAN veya (Storage Area Network) depolama alanı ağı, büyük miktarlarda veriyi depolayan ve bunlara erişim sağlayan özel bir yüksek hızlı ağdır.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1653551572610/eq-UVuwtC.png)

Büyük miktarda veriyi depolayan ve bunlara erişim sağlayan özel, yüksek hızlı bir ağ.

Dolayısıyla, temelde veri depolama için kullanılan özel bir ağdır ve bu ağ, birden çok disk dizisinden(disk array), anahtarından(switch) ve sunucudan(server) oluşur.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1653551574263/vKSUSHhNL.png)

SAN hata toleranslıdır.   
Veriler birkaç disk dizisi arasında paylaşılır.

Ve bu cihazlardan birden fazlasına sahip olduğu için, bir SAN hataya dayanıklıdır. Ve veriler de birkaç disk dizisi arasında paylaşılır. Bu nedenle, bir anahtar veya disk dizisi veya bir sunucu çökerse, verilere yine de erişilebilir.

Ve bir sunucu eriştiğinde SAN üzerindeki veriler, sanki yerel bir sabit diskmiş gibi verilere erişir. Çünkü işletim sistemleri, bir SAN’ı NAS’ta olduğu gibi paylaşılan bir ağ sürücüsü yerine yerel bağlı bir sabit sürücü olarak tanır. Ve SAN’lar da son derece ölçeklenebilirdir çünkü ağda kesinti olmadan   
daha fazla depolama alanı eklemek kolaylıkla yapılabilir.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1653551576100/AwnFpHkCo.png)

Son derece ölçeklenebilir.

Bir SAN yüksek hızlı bir ağdır Ve bunun sebebi bir SAN’da tüm cihazların birbirine bağlı olması anlamına gelir. birbirlerine bağlıdırlar ve SAN’lar için bir standart olan fiber kanal kullanılarak birbirine bağlanırlar . Fiber kanal, fiber optiktir ve saniyede 2 gigabit arasında, saniyede 128 gigabayta kadar hıza sahiptir .

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1653551577705/_Vw2Ks431.png)

Fiber Kanal kullanılarak birbirine bağlı.  
2 Gbit/s — 128 Gbit/s arasındaki hızlar.

Bu nedenle **fiber kanal son derece hızlıdır** ve aynı zamanda çok pahalıdır ve günümüzde çoğu SAN fiber kanal kullanır. Ama aynı zamanda fiber kanala alternatif olarak bazı SAN’lar bunun yerine iSCSI kullanır. Bu fiber kanala göre daha ucuz bir alternatiftir, ancak fiber kanal kadar hızlı değildir.   
Şimdi SAN kullanmanın ana nedenlerinden biri, SAN’ların **ağ trafiğinden etkilenmemesi**dir. Yerel bir alan ağında meydana gelebilecek darboğazlar gibi Ve bunun nedeni, SAN’ların gerçekten bir yerel alan ağının parçası olmamasıdır . SAN’lar bölümlere ayrılmıştır. Temelde **tek başına bir ağ**dır ve daha önce bahsettiğim gibi SAN’ların diğer nedenleri **yüksek oranda ölçeklenebilir** ve ayrıca **çok yedekli**dirler. Ve ayrıca tahmin edebileceğiniz gibi SAN’lar **ucuz değil**dir. Çok yüksek bir maliyetle gelirler, bu nedenle esas olarak **büyük şirketler ve büyük kuruluşlar tarafından kullanılır**lar.