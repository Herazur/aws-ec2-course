## LAB 03: IAM Rolü ile EC2 Bulut Sunucusu izinleri verin

### adımlar

*   IAM Kontrol Paneli’ne gidin
*   Sol gezinme bölmesinde Kullanıcılar’a tıklayın
*   Bir kullanıcı ekleyin ve ona Programmatic access verin
*   İleri’ye tıklayın ve Attach existing policies directly’i seçin
*   AmazonS3FullAccess’i arayın ve ekleyin Bu politikaları aramak için arama kutusunu kullanın ve onay kutusuna tıklayın
*   Sonrasında etiketlere tıklayın ve Review’e tıklayın ve oluşturun.
*   Show’a tıklayın ve Access key ID ve Secret access key i bir yere kaydedin. Veya isterseniz CSV dosyasını da indirebilirsiniz.
*   Bir Amazon Linux EC2 Bulut Sunucusu Başlatın
*   SSH erişimi olmalı
*   Diyelim ki bu andan itibaren Amazon S3 ile çalışmak istiyorsunuz. Birkaç bucket yapın ve birkaç bucket listeleyin. AWS Komut Satırı arayüzünü kullanabilirsiniz bilgisayarınızda kullanmak isterseniz awscli ı yüklemeniz gerekmektedir.
*   AWS CLI’yi yapılandırın bunun için bilgisayarınızda awscli yüklü olması gerekir

aws configure

*   Daha önce oluşturup kaydettiğiniz kullanıcının acces key id’sini ve secret access key anahtarlarını girin.
*   Bölgenizin adını girin
*   AWS CLI’den rastgele bir adla bir S3 paketi oluşturun. Uygun izinleriniz varsa, hem s3 bucket oluşturabilir hem de listeleyebilirsiniz.

aws s3 mb s3://mybucketnameherazur

S3 paketlerinizi listeleyin.

aws s3 ls

*   EC2'den S3'e bağlanmak için Erişim anahtarlarını kullandınız.
*   Kimlik bilgisi dosyasını görüntüleyin. Sabit kodlanmış kimlik bilgileri, güvenlik açısından güvensizdir.

cat ~/.aws/credentials

*   Dosyayı silin. Bu, kimlik bilgilerini kaldıracak

rm ~/.aws/credentials

*   Şimdi kovaları listelemeye çalışın. Erişim anahtarlarını temizlediğimiz için yapamazsınız.

aws s3 ls us-east-1

### BÖLÜM 2: IAM Rolleri ile İzinler

*   IAM Dashboard’a gidin ve Roles’e tıklayın
*   Create Role’e tıklayın
*   Kullanım durumu (Use case) için EC2'yu seçin
*   Sonraki adım olarak AmazonS3FullAccess politikasını seçin ve bu role ekleyin. Ayrıca bu rol için AmazonEC2FullAccess politikasını da ekleyin. Bu rolü bir sonraki laboratuvarda yeniden kullanacağız.
*   Bir sonraki adım olarak rol için ad ve açıklama girin. Ekli S3 ve EC2 erişim ilkelerine sahip olduğunuzu doğrulayın ve Rolü oluşturun.
*   EC2 instance sayfasına gidin. EC2 bulut sunucusunu seçin, Actions > Security > Modify IAM Role tıklayın ve bir önceki adımda oluşturduğumuz rolü ekleyin.
*   Şimdi EC2 örneğinize girin .
*   s3 kovalarını listeleyelim. Yapabilmelisin
*   Rolü kaldırırsanız erişimin yine olmayacağını anlayacaksınız. (isteğe bağlı) Artık erişim anahtarlarını ve Rolü kullanarak S3 ve diğer AWS hizmetlerine nasıl erişim verileceğini görüyorsunuz. Geçici Kimlik Bilgileri kullandığından Roller’in daha güvenli olduğunu da biliyorsunuz.
*   Aynı örneği bir sonraki laboratuvar için tutalım. O zamana kadar örneğinizi (instace) ı durdurabilirsiniz.

### Roller nasıl çalışır?

Roller, her 30 dakikada bir dönen geçici kimlik bilgilerini kullanır ve sabit kodlama anahtarlarından çok daha güvenlidir.

*   EC2'ye eklenen rol için geçici kimlik bilgilerini görüntülemek için bu komutu EC2'nizin içine yazın.

curl 169.254.169.254/latest/meta-data/iam/security-credentials/{rol-adınız}