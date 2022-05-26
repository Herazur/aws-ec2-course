## LAB 02: EC2 örneğinde Apache web sunucusunu kurun ve ondan golden image oluşturun

*   Lab 1'de yaptığımız gibi bir Amazon Linux EC2 Bulut Sunucusuna SSH ile bağlanın.
*   Apache web sunucusunu kurun

```
sudo yum -y install httpd
```
*   HTTPD hizmetini başlatın.

```
sudo service httpd start
```
*   Başlangıçta HTTPD sunucusunu etkinleştir

```
sudo chkconfig httpd on
```
*   EC2 Dashboard’a gidin ve instance ı seçin.
*   İnstance açıklaması altında ve Güvenlik Grubunun adına tıklayın.
*   İnbound Rules ekleyin ve Port range 80 ve Source IP’si 0.0.0.0/0 olan bir gelen kuralı ekleyin
*   İnstance’ın Public IP adresini bir Web tarayıcısına yapıştırarak Web Sunucusunun çalışıp çalışmadığını test edin. Public IP, İnstance Details sekmesi altında bulunur.
*   Apache Web Sunucusu Test Page Web Sayfasını görmelisiniz
*   Kök kullanıcı olun

```
sudo su
```
*   Basit bir özel index.html sayfası oluşturun ve /var/www/html üzerine koyun. Bu dizin, Apache web sunucusunun index.html dosyasını arayacağı varsayılan dizindir.

```
echo "Merhaba. Bu sayfa benim AWS EC2 Linux Bulut Sunucumda barındırılıyor.">/var/www/html/index.html
```
*   index.html dosyasına genel erişim vermek için html klasörünün iznini değiştirin

```
chmod -R 755 /var/www/html
```
*   Şimdi bir web sunucusundaki instance IP’sine tekrar göz atın. Bu mesajınızı görmelisiniz. ‘Merhaba. Bu sayfa benim AWS EC2 Linux Bulut Sunucumda barındırılıyor’

*   İnstance’ı seçin ve ardından Actions, Image and Templates, Create Image. öğesini seçin .
*   Create Image iletişim kutusunda, aşağıdaki bilgileri belirtin ve ardından Create Image öğesini seçin .
*   Image name — Görüntü için benzersiz bir ad.
*   Image description — Görüntünün isteğe bağlı açıklaması
*   No reboot — Bu seçenek varsayılan olarak seçili değildir. Amazon EC2 bulut sunucusunu kapatır, bağlı birimlerin anlık görüntülerini alır, AMI’yi oluşturup kaydeder ve ardından bulut sunucusunu yeniden başlatır. Bulut sunucunuzun kapanmasını önlemek için Yeniden başlatma yok’u seçin . AMI’nizin oluşturulurken durumunu görüntülemek için gezinme bölmesinde AMI’ler öğesini seçin . Başlangıçta, durum ancak birkaç dakika sonra pending değişmelidir .available
*   Yeni AMI’nizden bir örnek başlatın. Lab 1'i takip edin ve AMI sayfasında AMI’yi seçerken My AMI’yi seçin ve oluşturduğunuz AMI’yi seçin.
*   Yeni örneğin IP adresine göz atın. Daha önce olduğu gibi aynı mesajı görmelisiniz.

Artık daha fazla instance başlatmak için kullanabileceğimiz altın bir görüntü oluşturduk. Altın bir görüntü, basit bir ifadeyle, seçtiğiniz veri/yapılandırma ile beğeninize göre özelleştirdiğiniz bir görüntüdür. Örnekleri başlatabileceğiniz kişisel bir AMI olarak kaydedilir.