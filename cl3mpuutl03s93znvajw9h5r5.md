## Rust’a Başlarken

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1653551476085/AY3N3ZQMn.png)

#### Hello, World!

İlk Rust programınızı yazalım. Yeni bir dil öğrenirken `Hello, world!`ekrana yazdıran küçük bir program yazmak gelenekseldir, bu yüzden burada da aynısını yapacağız!

Dosya adı: hello.rs

```
fn main() {  
    println!("Hello, World!");  
}
```

`println!`konsola metin yazdıran bir *makrodur .*

Terminal ile dosyanın bulunduğu dizine geçip aşağıdaki kodları çalıştıralım.

```
$ rustc hello.rs  
$ ./hello  
Hello, world!
```

#### Hello, Cargo!

Cargo, Rust’ın yapı sistemi ve paket yöneticisidir. Çoğu Rustacean, Rust projelerini yönetmek için bu aracı kullanır çünkü Cargo, kodunuzu oluşturmak, kodunuzun bağlı olduğu kitaplıkları indirmek ve bu kitaplıkları oluşturmak gibi birçok görevi sizin yerinize gerçekleştirir. *(Kodunuzun bağımlılıklara* ihtiyaç duyduğu kitaplıkları çağırıyoruz .)

#### Cargo ile Proje Oluşturma

Gelin Cargo’yu kullanarak yeni bir proje oluşturalım ve orijinal “Hello, World!” ile ne kadar farklı olduğuna bakalım. *Proje* dizininize (veya kodunuzu saklamaya karar verdiğiniz yere) gidin . Ardından, aşağıdakileri çalıştırın:

```
$ cargo new hello\_cargo   
$ cd hello\_cargo
```

*Hello\_cargo* dizinine gidin ve dosyaları listeleyin. Cargo’nun bizim için iki dosya ve bir dizin oluşturduğunu göreceksiniz: bir *Cargo.toml* dosyası ve içinde *main.rs dosyası bulunan bir src* dizini .

Ayrıca bir *.gitignore* dosyasıyla birlikte yeni bir Git deposu başlattı.

Seçtiğiniz metin düzenleyicide *Cargo.toml’yi* açın . Aşağıdaki koda benzer görünmelidir.

Dosya adı: Cargo.toml

```
[package]  
name = "hello_cargo"  
version = "0.1.0"  
edition = "2021"


[dependencies]
```

Bu dosya, Cargo’nun konfigürasyon formatı olan [*TOML*](https://toml.io/) ( *Tom’s Obvious, Minimal Language* ) formatındadır.

İlk satır, `[package]`, aşağıdaki ifadelerin bir paketi yapılandırdığını gösteren bir bölüm başlığıdır. Bu dosyaya daha fazla bilgi ekledikçe, diğer bölümleri de ekleyeceğiz.

Sonraki üç satır, Cargo’nun programınızı derlemesi için ihtiyaç duyduğu yapılandırma bilgilerini belirler: kullanılacak Rust’ın adı, sürümü.

Son satır, `[dependencies]`projenizin bağımlılıklarından herhangi birini listelemeniz için bir bölümün başlangıcıdır. Rust'ta kod paketlerine *sandıklar* denir . Bu proje için başka kasalara ihtiyacımız olmayacak, ancak Bölüm 2'deki ilk projede olacak, bu yüzden bu bağımlılıklar bölümünü kullanacağız.

Şimdi *src/main.rs dosyasını* açın ve bir göz atın:

Dosya adı: src/main.rs

```
fn main() {  
    println!("Hello, world!");  
}
```

Önceki projemiz ile Cargo’nun oluşturduğu proje arasındaki fark, Cargo’nun kodu *src* dizinine yerleştirmesi ve üst dizinde bir *Cargo.toml* yapılandırma dosyamızın olması.

#### Kargo Projesi Oluşturma ve Yürütme

Şimdi “Hello, World!”u kurup çalıştırdığımızda nelerin farklı olduğuna bakalım. Hello\_cargo dizininizden aşağıdaki komutu girerek projenizi oluşturun :

```
$ cargo build  
 Compiling hello\_cargo v0.1.0 (/home/herazur/rust/hello\_cargo)  
 Finished dev \[unoptimized + debuginfo\] target(s) in 0.37s
```

`cargo build`İlk kez çalıştırmak , Cargo'nun en üst düzeyde yeni bir dosya oluşturmasına da neden olur: *Cargo.lock* . Bu dosya, projenizdeki bağımlılıkların tam sürümlerini takip eder. Bu projenin bağımlılıkları yok. Bu dosyayı asla manuel olarak değiştirmeniz gerekmeyecek; Cargo sizin için içeriğini yönetir.

Az önce `cargo build` ile bir proje oluşturduk ve onunla çalıştırdık , ancak kodu derlemek ve ardından ortaya çıkan yürütülebilir dosyayı tek bir komutta çalıştırmak için:

```
$ cargo run  
 Finished dev \[unoptimized + debuginfo\] target(s) in 0.00s  
 Running \`target/debug/hello\_cargo\`  
Hello, world!
```

Bu sefer Cargo’nun derleniyor olduğunu gösteren bir çıktı görmediğimize dikkat edin `hello_cargo`. Cargo, dosyaların değişmediğini anladı, bu yüzden sadece ikili dosyayı çalıştırdı.

Kargo ayrıca adlı bir komut sağlar `cargo check`. Bu komut, derlendiğinden ancak yürütülebilir bir dosya üretmediğinden emin olmak için kodunuzu hızla kontrol eder:

```
$ cargo check  
    Checking hello\_cargo v0.1.0 (/home/herazur/rust/hello\_cargo)  
    Finished dev \[unoptimized + debuginfo\] target(s) in 0.11s
```

Neden yürütülebilir bir dosya istemiyorsun? Çoğu zaman, `cargo check`çok daha hızlıdır `cargo build`’den çünkü yürütülebilir dosya üretme adımını atlar. Kodu yazarken çalışmanızı sürekli kontrol ediyorsanız, `cargo check`kullanmak süreci hızlandıracaktır!

Kargo hakkında şimdiye kadar öğrendiklerimizi tekrarlayalım:

*   `cargo build`kullanarak bir proje oluşturabiliriz .
*   `cargo run`kullanarak tek adımda bir proje oluşturup çalıştırabiliriz.
*   `cargo check`kullanarak hataları kontrol etmek için bir ikili oluşturmadan bir proje oluşturabiliriz.