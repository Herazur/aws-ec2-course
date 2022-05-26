## DHCP Nedir ve Nasıl çalışır?

Her bilgisayar veya cihaz, iletişim amacıyla bir ıp adresine sahip olmalıdır. IP adresi, ağdaki bir bilgisayar veya aygıt için bir tanımlayıcıdır. Ve bir bilgisayara bir IP adresi atamanın iki yolu vardır. Statik IP veya Dinamik IP kullanılarak yapılabilir.

Statik bir IP, bir kullanıcının bir IP adresini manuel olarak atadığı yerdir. Şimdi bu, ağ oluşturmanın başlangıcında yapılan orjinal yöntemdi. Dolayısıyla, bir ağdaki her bilgisayar için bilgisayarın ağ yapılandırma sayfasını açmanız ve manuel olarak bir IP adresi girmeniz gerekiyordu.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1653551507875/GpeD5IqOG.png)

Statik bir IP, bir kullanıcının bir IP atadığı yerdir. manuel olarak adresleyin.

Ancak bir IP adresine ek olarak, bir alt ağ maskesi (subnet mask) varsayılan ağ geçidi (default gateway) ve bir DNS sunucusu da yazmanız gerekir. Ve ağa başka bir bilgisayar veya cihaz eklemek istediğinizde, aynı şeyi yapmanız gerekiyordu. Tahmin edebileceğiniz gibi, özellikle çok sayıda bilgisayara sahip büyük bir ağla uğraşıyorsanız, bu çok fazla iş olabilir. Ayrıca, tüm IP adreslerinin benzersiz olduğundan emin olmalısınız çünkü aynı IP adresini iki kez atarsanız, bir IP çakışmasına neden olur ve bu bilgisayarların ağa erişememesine neden olur.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1653551509289/P2c5CPXlf.png)

I.P. adresleri benzersiz olmalıdır.

Ancak bunun daha iyi ve daha kolay bir yolu vardır. Dinamik IP, bilgisayarın bir DHCP sunucusundan otomatik olarak IP adresi aldığı yerdir. DHCP sunucusu, bir bilgisayara otomatik olarak IP adresi atar. Ve bir IP adresine ek olarak, bir alt ağ maskesi, varsayılan ağ geçici ve bir DNS sunucusu da atayabilir.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1653551510632/O6-hq6DTFX.png)

Dinamik IP, bir bilgisayarın IP aldığı yerdir DHCP sunucusundan.

Bu nedenle, burada bir örnek olarak , bir Microsoft Windows bilgisayarındaki ağ arabirim kartı için açık bir ağ bağlantı özellikleri penceremiz var . Ve burada görebileceğiniz gibi, bu bilgisayar otomatik olarak bir IP adresi alacak şekilde ayarlanmıştır.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1653551512034/vDrYmBmQV.png)

Otomatik olarak bir IP Adresi Alma

Bu seçeneği seçtiğinizde, bilgisayar ağ üzerinde bir IP adresi için bir istek yayınlayacak ve ardından DHCP sunucusu kendi havuzundan bir IP adresi atayacak ve bunu bilgisayara teslim edecektir.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1653551513422/fO2ZKHoei.png)

Ve sonra bu yapıldığında, DHCP sunucusunun bilgisayarınıza verdiği tüm farklı ayarları doğrulayabilirsiniz. Bunu, bir Windows bilgisayarında bir komut istemi açarak ve ardından

> ipconfig / all

yazıp “enter” tuşuna basarak yapabilirsiniz.

Burada görebileceğiniz gibi , bu bilgisayarda DHCP etkindir, bu da onun IP adresini bir DHCP sunucusundan aldığı anlamına gelir ve burada alt ağ maskesi, varsayılan ağ geçidi ve DNS sunucusuyla birlikte IP adresini görebilirsiniz.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1653551514819/Yzhegatk0c.png)

Yani tüm bu ayarlar DHCP sunucusu tarafından verildi. Dinamik IP adreslemenin en iyi seçim olduğunu söyleyebileceğiniz gibi, otomatiktir ve bir ağı yönetmeyi çok daha kolay hale getirir.