## LAB 06: Key pair yerine parola ile oturum açmak

### adımlar

1.  Bir SSH ile EC2 bulut sunucunuzda oturum açın. Çalışan bir EC2 Bulut Sunucunuz yoksa bir tane oluşturun.
2.  Kullanıcı için bir şifre belirleyin. Aşağıdaki örnek, kullanıcı olarak ec2 kullanıcısını kullanır:

```
sudo passwd ec2-user  
   Changing password for user ec2-user.  
   New password:  
   Retype new password:  
   Şifre yenileme başarılı ise şöyle görünür:  
   passwd: all authentication tokens updated successfully./ ya da / passwd: tüm kimlik doğrulama belirteçleri başarıyla güncellendi.
```

1.  /etc/ssh/sshd\_config dosyasındaki PasswordAuthentication parametresini bulup güncelleyin. Eğer görüntüleyemiyorsanız sudo su komutu ile yetki alıp deneyin:

```
PasswordAuthentication yes
```

1.  SSH hizmetini yeniden başlatın. Amazon Linux, RHEL 5 ve SUSE Linux için şu komutu kullanın:

```
sudo service sshd restart
```

1.  EC2 oturumundan çıkın ve ardından parola doğrulamasını test etmek için oturum açın.

```
ssh ec2-user@instance_publicadres
```

1.  Sizden bir şifre istenecektir. Parolayı girin ve ec2 kurulumunda başarıyla oturum açmış olmalısınız

### Bölüm 2: Parola kimlik doğrulamasını etkinleştirme ve EC2'de ilk oturum açma için parola belirleme adımları

İlk oturum açmanız için parola ssh’yi etkinleştirmek için başlatma sırasında bu komut dosyasını EC2 User data’ya yapıştırın. Komut dosyasında TODO altındaki satırları değiştirerek geçin.

```
#!/bin/bash  
sed 's/PasswordAuthentication no/PasswordAuthentication yes/' -i /etc/ssh/sshd_config  
systemctl restart sshd  
service sshd restart
```

```
#TODO: furkan'ı istediğiniz kullanıcı adıyla değiştirin  
useradd furkan
```

```
# TODO: password123'ü istediğiniz şifreyle değiştirin ve furkan'ı useradd'de seçilen kullanıcı adınızla değiştirin  
echo "password123" | passwd --stdin furkan
```

*   Komut dosyasında herhangi bir değişiklik yapmazsanız, bu komutu kullanarak birkaç dakika sonra EC2'de oturum açabilirsiniz. Parola parola123'tür. IP’yi EC2 IP’nizle değiştirin

```
ssh furkan@11.22.23.24
```