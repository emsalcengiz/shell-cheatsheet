# shell-cheatsheet
shell komutlarının türkçe açıklamalarını içerir

# Temel Komutlar

**whoami:** Bulunan oturumun sahibi olan kullanıcıyı yazdırır.

**su:** Başka bir kullanıcının yetkileri ile komut çalıştırmak için yeni bir shell ayağa kaldırır. (“Örnek: su root”)

**pwd:** Neredeyiz? Şu an bulunduğunuz dizini yazdırır. (“print working directory”)

**ls:** Bulunduğumuz dizinin içindeki dosyaları ve dizinleri listeler. (“listing”)

**cd dizin_adı**: Bulunduğunuz dizini değiştirmenize yarar. (“change directory”)

**man:** Argüman olarak verdiğiniz komutun manuelini, kılavuzunu açar. (Örnek: man touch)

**touch dosya_yolu**: Belirttiğiniz yoldaki dosyanın son değiştirilme tarihini günceller. Böyle bir dosya yoksa bu dosyayı oluşturur.

**cd .. **: Hiyerarşik olarak bulunduğunuz dizinden üst dizine çıkmanıza yarar. (Örnek: Çalışma dizininiz /home/ali iken çalışma dizininizi /home yapar)

**~ **: Oturumun sahibi kullanıcı için home dizinini belirtir. (Tilde sembolü)

**cd ~/../.**: Çalışma dizininizi "home"'un üst dizinine ayarlar. Sondaki nokta bulunulan en son klasörün kendisini belirtir.

**cp klasör/dosya.csv backup/dosya.bck**: "klasör" dizinindeki "dosya.csv" dosyasını, "backup" dizinine "dosya.bck" dosya ismiyle kopyalar.

**cp dosya1.txt dosya2.txt backup**: Belirtilen iki dosyayı ("dosya1.txt" ve "dosya2.txt") aynı isimle "backup" dizinine kopyalar.

**dd**: Dosya kopyalama ve dönüştürme yapar.Örneğin dd if=/dev/sda of=./disk.img ile /dev/sda diskinin tamamının imajını .img dosyası olarak alabilirsiniz.

**mv**: Dosyaları taşımak ya da yeniden adlandırmak için kullanılan komut (move)

**mv dosya_adi.txt yeni_dosya_adi.txt**: dosya_adi.txt'yi yeni_dosya_adi.txt olarak taşıdık. Böylece adını değiştirmiş olduk.

**rm**: Dosyaları silmek için kullanılan komut. ("remove")

**rm dosya.txt backup/dosya-2.txt**: Belirtilen iki dosyayı da siler.

**mkdir dizin_ismi**: dizin_ismi adında yeni bir dizin oluşturur.

**mkdir -p gecersiz_dizin/hedef_dizin**: gecersiz_dizin'in varolmaması durumunda hedef_dizin ile birlikte onu da açar.

**rm -rf dizin_ismi**: dizin_ismi adlı dizini içindeki dosyaları ve altdizinleri de dahil ederek siler.

**pbcopy**: Argüman olarak verilen değeri panoya kopyalar.

**cat dosya_ismi**: Dosyanın içeriğini ekrana yazdırır.

**df**: Dosya sisteminizdeki disk alanı hakkında bilgi edinmenizi sağlar.

**du**: Disk kullanımını görmek ve hangi uygulamanın yada dosya alt sisteminin ne kadar yer kapladığını görmek için kullanılır.

**ps**: Sisteminizde hangi işlemlerin çalıştığını görmenizi sağlar.

**groups**: Verilen kullanıcının gruplarını listeler. Örneğin groups root

**wget**: HTTP, HTTPS veya FTP protokollerini kullanan bir adresteki dosyayı terminal üzerinden doğruca kendi makinemize indirmek için kullanılan komut.

**grep**: Dosyaların içinde düzenli ifadelerle (RegEx) arama yapmanızı sağlayan komut. Log incelerken vazgeçilmezimiz.

**watch**: Belirli aralıklarla bir komutun çıktısını çalıştırarak ekrana yazdırır.(watch -n1 ls -la )
