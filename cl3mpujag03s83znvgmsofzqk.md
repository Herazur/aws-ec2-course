## Modül 1: Full-Stack Bir React Uygulaması Oluşturun

### Tanıtım

AWS Amplify, sunucusuz arka uçlara sahip tek sayfalı web uygulamaları veya statik siteler oluşturmak, dağıtmak ve barındırmak için Git tabanlı bir CI/CD iş akışı sağlar. Git deposuna bağlandıktan sonra Amplify, hem ön uç çerçevesi hem de Amplify CLI ile yapılandırılmış sunucusuz arka uç kaynakları için yapı ayarlarını belirler ve her kod taahhüdünde güncellemeleri otomatik olarak dağıtır.

### Ne öğreneceksin

*   Bir React uygulaması oluşturun
*   GitHub deposunu başlat
*   Uygulamanızı AWS Amplify ile dağıtın
*   Kod değişikliklerini uygulayın ve uygulamanızı yeniden dağıtın

#### Yeni bir React uygulaması oluşturun

*   Bir React uygulaması oluşturmanın en kolay yolu, create-react-app komutunu kullanmaktır. Komut İsteminizde veya Terminalinizde aşağıdaki komutu kullanarak bu paketi yükleyin:

npx create-react-app amplifyapp

cd amplifyapp

npm start

#### GitHub deposunu başlat

Bu adımda bir GitHub deposu oluşturacak ve kodunuzu depoya aktaracaksınız. Bu adımı tamamlamak için bir GitHub hesabına ihtiyacınız olacak — bir hesabınız yoksa [buradan kaydolun](https://github.com/) .

a. Uygulamanız için yeni bir GitHub deposu oluşturun ( [link](https://github.com/new) )

B. Git’i başlatın ve komut satırı arabiriminizde aşağıdaki komutları yürüterek uygulamayı yeni GitHub deposuna gönderin:

```
git init  
git remote add origin git@github.com:username/reponame.git  
git add .  
git commit -m “initial commit”  
git push origin master
```

#### AWS Management Console’da oturum açın

[AWS Management Console’u](https://console.aws.amazon.com/) açın. Ekran yüklendiğinde, başlamak için kullanıcı adınızı ve şifrenizi girin. Ardından arama çubuğuna “Amplify” yazın ve hizmet konsolunu açmak için AWS Amplify’ı seçin.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1653551448683/JeCwsPcur.png)

#### Uygulamanızı AWS Amplify ile dağıtın

Bu adımda, az önce oluşturduğunuz GitHub deposunu AWS Amplify hizmetine bağlayacaksınız. Bu, uygulamanızı AWS’de oluşturmanıza, dağıtmanıza ve barındırmanıza olanak tanır.

a. AWS Amplify hizmet konsolunda, Amplify Hosting altında “**Get started**”i seçin.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1653551450121/CMyybYtkN.png)

B. Depo hizmeti olarak GitHub’ı seçin ve **Continue**’ı seçin .

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1653551451480/CuGX47HFg.png)

C. GitHub ile kimlik doğrulaması yapın ve Amplify konsoluna dönün. Daha önce oluşturduğunuz depoyu ve ana dalı seçin, ardından **Next** öğesini seçin .

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1653551452857/HaQiyBwqx.png)

D. Varsayılan yapı ayarlarını kabul edin ve **Next**’i seçin .

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1653551454539/lXYAFjNqC.png)

e. Son ayrıntıları gözden geçirin ve **Save and deploy**’ı seçin .

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1653551455843/JWS1N8EQL.png)

F. AWS Amplify şimdi kaynak kodunuzu oluşturacak ve uygulamanızı [https://...amplifyapp.com](https://...amplifyapp.com) adresinde dağıtacaktır.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1653551457108/kbylyXyds.png)

G. Derleme tamamlandığında, web uygulamanızın canlı ve çalışır durumda olduğunu görmek için küçük resmi seçin.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1653551458396/rFMZY28F8.png)

#### Kod değişikliklerini otomatik olarak dağıt

Bu adımda, metin düzenleyicinizi kullanarak kodda bazı değişiklikler yapacak ve değişiklikleri uygulamanızın ana dalına göndereceksiniz.

a. Aşağıdaki kod ile src/App.js dosyasını düzenleyin ve kaydedin.

import React from 'react';  
import logo from './logo.svg';  
import './App.css';  
  
function App() {  
  return (  
    <div className="App">  
      <header className="App-header">  
        <img src={logo} className="App-logo" alt="logo" />  
        <h1>Hello from V2</h1>  
      </header>  
    </div>  
  );  
}  
  
export default App;

B. Yeni bir yapıyı otomatik olarak başlatmak için Komut İstemi’nde (Windows) veya Terminal’de (macOS) GitHub’daki değişiklikleri itin:

```
git add .  
git commit -m “changes for v2”  
git push origin master
```

C. Derleme tamamlandığında, güncellenmiş uygulamanızı görüntülemek için AWS Amplify konsolundaki küçük resmi seçin.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1653551459759/_gVkZoStx.png)

GitHub ile entegrasyon ve AWS Amplify kullanarak AWS Cloud’da bir React uygulaması dağıttınız. AWS Amplify ile uygulamanızı sürekli olarak bulutta dağıtabilir ve küresel olarak kullanılabilen bir CDN’de barındırabilirsiniz.