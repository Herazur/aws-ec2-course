## Modül 2: Local Amplify Uygulamasını Başlatın

Bu modülde Amplify CLI’yi kuracak ve yapılandıracaksınız.

### Tanıtım

Artık hesabımızda yeni bir Amplify projesi başlattığımıza göre, geliştirmeye devam edebilmek ve yeni özellikler ekleyebilmek için onu yerel ortamımıza getirmek istiyoruz.

Bu modülde Amplify CLI’yi kuracak ve Amplify projesini CLI kullanarak başlatacaksınız.

### Ne öğreneceksin

*   Amplify CLI’yi kurun ve yapılandırın
*   Amplify uygulamasını başlatın

### Anahtar kavramlar

Amplify CLI — Amplify CLI, AWS hizmetlerini doğrudan terminalinizden oluşturmanıza, yönetmenize ve kaldırmanıza olanak tanır.

#### Amplify CLI’yi yükleyin

Amplify Command Line Interface (CLI), basit bir kılavuzlu iş akışını izleyerek uygulamanız için AWS bulut hizmetleri oluşturmaya yönelik birleşik bir araç zinciridir. Şimdi Komut İstemi’ni (Windows) veya Terminal’i (macOS) kullanarak Amplify CLI’yi yükleyelim. NOT: Bu komut, Komut İstemi/Terminalinizdeki herhangi bir dizinde çalıştırılabilir, çünkü “-g” ikili dosyanın sisteminize global olarak kurulacağını gösterir.

```
npm install -g @aws-amplify/cli
```

#### Amplify CLI’yi yapılandırın

Amazon IAM (Kimlik ve Erişim Yönetimi), AWS’de kullanıcıları ve kullanıcı izinlerini yönetmenize olanak tanır. CLI, hizmetleri sizin adınıza CLI aracılığıyla programlı olarak oluşturmak ve yönetmek için IAM’yi kullanır.

CLI’yi yapılandırmak için yapılandırma komutunu çalıştırın. CLI yapılandırma sürecinin bir videosunu izlemek için burayı [tıklayın](https://www.youtube.com/watch?v=fWbM5DLh25U) .

```
amplify configure
```
#### Amplify uygulamasını başlatın

Ardından, bir Backend dağıtacağız ve Backend ortamını yerel olarak başlatacağız.

a. Amplify konsolunda, [**Backend environments**](https://us-east-1.console.aws.amazon.com/amplify/home?region=us-east-1#)’a tıklayın ve **get started**’a tıklayın . Arka ucun dağıtılmasını bekleyin.

B. [**Backend environments**](https://us-east-1.console.aws.amazon.com/amplify/home?region=us-east-1#) sekmesinde, **Launch Studio**’a tıklayın

C. Amplify Console [**Backend environments**](https://us-east-1.console.aws.amazon.com/amplify/home?region=us-east-1#) sekmesine geri dönün ve Y**Local setup instructions** açın . Komutu panonuza kopyalayın ve bilgisayarınızdaki terminali açın.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1653551466988/T_NO_WxZz.png)

D. Komutu terminalinize yapıştırın ve kurulum talimatlarını izleyin.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1653551468404/NKPEsdcyE.png)

Amplify projesini başlattınız ve artık özellikler eklemeye hazırsınız! Bir sonraki modülde sadece birkaç satır kodla eksiksiz bir kullanıcı kimlik doğrulama akışı ekleyeceğiz.

Amplify projenizi istediğiniz zaman kontrol panelinde görüntülemek için şimdi aşağıdaki komutu çalıştırabilirsiniz:

```
amplify console
```