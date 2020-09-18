![png](https://miro.medium.com/max/3840/1*MAfGVIXrgJVKpKg_ZwMDow.png)
# shell-cheatsheet
shell komutlarının türkçe açıklamalarını içerir

# Temel Komutlar

```whoami:``` Bulunan oturumun sahibi olan kullanıcıyı yazdırır.

```su:``` Başka bir kullanıcının yetkileri ile komut çalıştırmak için yeni bir shell ayağa kaldırır. (“Örnek: su root”)

```pwd:``` Neredeyiz? Şu an bulunduğunuz dizini yazdırır. (“print working directory”)

```ls:``` Bulunduğumuz dizinin içindeki dosyaları ve dizinleri listeler. (“listing”)

```cd dizin_adı: ``` Bulunduğunuz dizini değiştirmenize yarar. (“change directory”)
```man:``` Argüman olarak verdiğiniz komutun manuelini, kılavuzunu açar. (Örnek: man touch)

```touch dosya_yolu:```  Belirttiğiniz yoldaki dosyanın son değiştirilme tarihini günceller. Böyle bir dosya yoksa bu dosyayı oluşturur.

```cd .. :```  Hiyerarşik olarak bulunduğunuz dizinden üst dizine çıkmanıza yarar. (Örnek: Çalışma dizininiz /home/ali iken çalışma dizininizi /home yapar)

```~ :``` Oturumun sahibi kullanıcı için home dizinini belirtir. (Tilde sembolü)

```cd ~/../.:```  Çalışma dizininizi "home"'un üst dizinine ayarlar. Sondaki nokta bulunulan en son klasörün kendisini belirtir.

```cp klasör/dosya.csv backup/dosya.bck:```  "klasör" dizinindeki "dosya.csv" dosyasını, "backup" dizinine "dosya.bck" dosya ismiyle kopyalar.
```cp dosya1.txt dosya2.txt backup:```  Belirtilen iki dosyayı ("dosya1.txt" ve "dosya2.txt") aynı isimle "backup" dizinine kopyalar.

```dd:```  Dosya kopyalama ve dönüştürme yapar.Örneğin dd if=/dev/sda of=./disk.img ile /dev/sda diskinin tamamının imajını .img dosyası olarak alabilirsiniz.

```mv:```  Dosyaları taşımak ya da yeniden adlandırmak için kullanılan komut (move)

```mv dosya_adi.txt yeni_dosya_adi.txt:```  dosya_adi.txt'yi yeni_dosya_adi.txt olarak taşıdık. Böylece adını değiştirmiş olduk.

```rm:```  Dosyaları silmek için kullanılan komut. ("remove")

```rm dosya.txt backup/dosya-2.txt:```  Belirtilen iki dosyayı da siler.

```mkdir dizin_ismi:```  dizin_ismi adında yeni bir dizin oluşturur.
```mkdir -p gecersiz_dizin/hedef_dizin:```  gecersiz_dizin'in varolmaması durumunda hedef_dizin ile birlikte onu da açar.

```rm -rf dizin_ismi:```  dizin_ismi adlı dizini içindeki dosyaları ve altdizinleri de dahil ederek siler.

```pbcopy:```  Argüman olarak verilen değeri panoya kopyalar.
```cat dosya_ismi:```  Dosyanın içeriğini ekrana yazdırır.

```df:```  Dosya sisteminizdeki disk alanı hakkında bilgi edinmenizi sağlar.

```du:```  Disk kullanımını görmek ve hangi uygulamanın yada dosya alt sisteminin ne kadar yer kapladığını görmek için kullanılır.

```ps :```  Sisteminizde hangi işlemlerin çalıştığını görmenizi sağlar.

```groups :```  Verilen kullanıcının gruplarını listeler. Örneğin groups root

```wget :```  HTTP, HTTPS veya FTP protokollerini kullanan bir adresteki dosyayı terminal üzerinden doğruca kendi makinemize indirmek için kullanılan komut.

```grep :```  Dosyaların içinde düzenli ifadelerle (RegEx) arama yapmanızı sağlayan komut. Log incelerken vazgeçilmezimiz.

```watch :```  Belirli aralıklarla bir komutun çıktısını çalıştırarak ekrana yazdırır.(watch -n1 ls -la )

# Veri Manipülasyonu

```less:``` Büyük dosyalara bakmak için kullanılan bir komut. Dosyanın tamamını ekrana yazdırmaz, daha okunabilir ilerlenebilir hale getirir.

less’e birden fazla dosya ismi verirsek :n’le bir sonraki dosyaya, :p’yla bir önceki dosyaya gideriz, :q’la çıkarız.

```more:``` less' in eskisi. Sadece aşağıya kaydırmaya izin verir.

```head:``` Dosyanın ilk parçasını (standart 10 satır) yazdırır.

```tail:``` Head komutunun tam tersi olarak dosyanın son parçasını yazdırır. '-f' parametresi ile kullanıldığı zaman dosyaya anlık olarak yazılan içeriği ekrana basar.

# Komut Satırı Bayrakları

```head -n 3 directory/dosya_ismi.csv:``` Dosyadaki ilk üç satırı getiriyor (“number of lines”)

```ls -R:``` Bütün klasörleri ve içindekileri gösterir

```man:``` Yanına yazılan komut hakkında yardım eder (manual)

```cut:``` csv dosyalarında sütunları seçer

cut -f 2-5,8 -d , dosya.csv: 2. ve 5. sütun arasındakileri seç. (flag'ler: -f (fields, sütunları belirtir), -d (delimiter, ayırıcı))

```sed:``` Akış editörü. Dosyalar üzerinde bir çok işlem yapmaya yarar. Örneğin sed -i 's/aaaa/bbbb/g' test.txt ile text.txt içerisinde ki her aaaa dizisi bbbb haline getirilebilir.

```awk:``` Metin dosyalarını işlemek için kullanılır. Örneğin awk -F';' '{print$1}' test.txt ile test.txt içerisindeki satırları ';' ayracına göre sütunlara ayırır ve ilk sütunları ekrana yazdırır

```find:``` Dizin araması yapar. find / -name "temp*" ile / dizininde ismi temp ile başlayan tüm dosyalar aranabilir.

```grep:``` dosyada arama yapar

grep kelime directory/dosya.csv: "kelime"yi içeren satırları getirir

grep -Hirn kelime directory: belirtilen dizin altında "kelime"yi içeren satırları getirir.

        -c: kelimenin bulunduğu satır sayısı döndürür
        -h: birden fazla dosyada arama yapıyorsa dosya isimlerini döndürmez
        -i: büyük/küçük harf farkını yok sayar ("kelime" ve "Kelime"yi arar)
        -l: eşleşme bulunan dosya isimlerini getirir, eşleşmeleri getirmez
        -n: eşleşen satırların satır sıralarını döndürür
        -v: eşleşme bulunmayan satırları döndürür
```paste:``` iki tabloyu tek tablo yapar

# Komutların çıktılarını nasıl saklıyoruz?

örnek: ```head -n 5 directory/dosya.csv > dosya2.csv:``` çıktı dosya2.csv’ye gider.

çıkardığımız dosyanın içeriklerine ```cat dosya2.csv```’yle bakabiliriz.

örnek:``` head -n 5 directory/dosya.csv >> dosya2.csv :``` çıktı dosya2.csv'ye gider.

fakat buradaki farklılık, > yerine >> kullanmamız. eğer >> kullanırsak, yazdığımız veriler dosyaya eklenir, dosyada halihazırda bulunan veriler silinmez.

yine aynı şekilde çıkardığımız dosyanın içeriklerine cat dosya2.csv’yle bakabiliriz.

örnek:``` head -n 5 directory/dosya.csv 2> dosya2.csv :``` oluşan hata dosya2.csv'ye gider.

buradaki farklılık ise > yerine 2> kullanmamız. eğer 2> kullanırsak, kullandığımız komutta oluşan hata çıktılarını dosyaya yazmış oluruz.

örnek:``` head -n 5 directory/dosya.csv > dosya2.csv 2> err.txt```

buradaki komutta hata oluşmazsa çıktı dosya2.csv'ye, hata oluşursa oluşan hata çıktısı err.txt'ye yazılır.

# pipe | operatörü:
pipe soldaki komutun çıktısını alıp sağa gönderiyor.

örnek: ```head -n 5 directory/dosya.csv | tail -n 3:``` beşinci satıra kadar aldı, sonra sondan üçüncüyü aldı (tail dosyanın sonundan alması gerektiğini belirtir)

örnek: ```cut -d , -f 2 directory/dosyacsv | grep -v anahtar_kelime:``` cut’la dosya.csv’deki 2. kolonu seçti, pipe'la sağ tarafa grep’le "anahtar_kelime" kelimesinin geçmediği durumların aramasını yaptı

örnek: ```cut -d , -f 1 directory/dosya.csv | grep -v Tarih | head -n 10:``` dosya.csv verisinin ilk kolonunu seçtik, “Tarih” yazan header line’ı sildik ve ardından ilk on satırı aldık (head en baştaki satırları alması gerektiğini belirtir)

```wc:``` kaç tane karakter, kelime, ya da satır varsa döndürür (“word count”)

# Jokerler

Komutlarda birden fazla dosya ismi verirsek birden fazla dosya üstüne çalışır. Bütün dosyaların hepsini tek tek yazmaktansa * operatörünü kullanırız.
```cut -d , -f 1 directory/*.csv
cut -d , -f 1 directory/ka*.csv:``` Klasörde kalem.csv ve kagit.csv isimli iki tane csv dosyası olsun, ikisini de seçmek için

```?``` tek bir karakteri eşliyor, mesela 201?.txt 2017.txt ve 2018.txt’yi eşliyor, ama 2017-01.txt’yi eşlemiyor.

```[…]:``` köşeli parantezin içindeki bir karakteri eşler, mesela 201[78].txt 2017.txt ya da 2018.txt’yi eşler.

```{…}:``` {*.txt, *.csv} .txt ya da .csv’yle biten dosyaları eşler.






