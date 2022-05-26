## LAB 01: Basit bir Linux EC2 örneğini yapılandırın ve başlatın

*   Üst Gezinme Çubuğundan/menüsünden Services’e tıklayın
*   EC2 hizmetini seçin
*   Launch instances’e tıklayın
*   Amazon Linux AMI’yi seçin
*   EC2 Bulut Sunucusu Türünü t2.micro seçin
*   Örnek Ayrıntılarını Yapılandır
*   Yapılandırabileceğimiz birçok parametre var ancak bu laboratuvar için onları varsayılan olarak bırakacağız.
*   Add Storage’a tıklayın ve varsayılan olarak bırakın
*   Add Tags’e tıklayın ve instance a tag verin
*   Configure Security Group, yeni bir güvenlik grubu oluşturun veya mevcut olanı seçin
*   Review and Launch Instance a basın
*   Key Pair oluşturun ve indirin
*   Oluşturduğunuz instanceın runnning durumuna geçmesini bekleyin
*   terminale geçip indirdiğiniz key pair dosyasının bulunduğu klasöre geçin ve chmod 400 keypairadi.pem diyin
*   ssh -i keypairadi.pem ec2-user@instancepublicip