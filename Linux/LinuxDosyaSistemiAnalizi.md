### Canlı adli dosya sistemi analizi gerçekleştirmek, genellikle olay müdahalesinin erken bir aşamasıdır ve potansiyel güvenlik ihlallerini değerlendirme ve belirlemede kritik öneme sahiptir.Bu süreç, yetkisiz erişim, kötü amaçlı faaliyetler veya veri ihlaline dair kanıtları ortaya çıkarmak için dijital eserleri, sistem günlüklerini, kullanıcıları ve dosya yapılarını incelemeyi içerir.

### Olay müdahalesinin bu aşamasında yalnızca tehlikeye ilişkin eserleri analiz edip belirlediğimizden, tehlikeye atılmış canlı sistemi daha sonraki kullanımlar için düzeltmenin genellikle güvenli olmadığını vurgulamak önemlidir.Bunun yerine, yedeklerden güvenli bir şekilde geri yükleme yapmak ve güvenlik açığı yönetimi iyileştirme faaliyetlerini gerçekleştirmek (ki bu, bu odanın kapsamı dışındadır) kurtarma ve etkiyi en aza indirmek için önemlidir.


## Dayanak Noktasını Belirleme
Dosya yükleme özelliğinin istismar edildiğine dair ipuçlarını tespit etmek için aramamızı web dizinlerine odaklamalı ve sunucuya yüklenen dosyaları incelemeliyiz.Öncelikle /var/www/html/ dizinindeki web dizinine gidin ve web dosyalarını ve dizinlerini listelemek için ls -al komutunu çalıştırın:

![image](https://github.com/user-attachments/assets/7d2e66fb-b0c2-4ac3-a37c-fcce527e1dae)


Dizin yapısından, /uploads dizininin aradığımız şeyi içereceği anlaşılıyor. Uploads dizinindeki dosyaları listeleyelim:

![image](https://github.com/user-attachments/assets/a58ab4b8-5367-4505-9524-440fb48e913a)

/uploads dizini incelendiğinde, JPEG görüntüleri de dahil olmak üzere, görünüşte rastgele isimlere sahip çok sayıda dosyanın mevcut olduğu görülmektedir.Ek olarak, bu dosyaların hepsinin www-data kullanıcısına ait olduğunu unutmayın. Olası görüntü olmayan dosyalara odaklanmak için, JPEG dosyalarını filtrelemek için grep komutunu kullanabiliriz:

![image](https://github.com/user-attachments/assets/97b9c874-8fdb-42d7-ba47-19ed0f6e18ea)

Grep komutundaki -v seçeneği, ".jpeg" uzantısına sahip olmayan dosyaları görüntüleyerek deseni geçersiz kılar.Bu, PHP gibi farklı uzantılara sahip olup daha fazla araştırma gerektirebilecek dosyaları belirlememize ve öncelik sırasına koymamıza olanak tanır.
.phtml dosyasının içeriğini görüntülemek, kötü amaçlı bir web kabuğunun (sistem komutlarının yürütülmesine izin veren bir web sunucusundaki dosya) varlığına dair kanıt sağlıyor ve varsayımlarımızı doğruluyor:

![image](https://github.com/user-attachments/assets/bc4a03bd-99ab-407d-9326-d550a0762fc4)

Yukarıdaki analizden, saldırganın sunucuda PHP kodu çalıştırmak için bir .phtml belgesi yüklediği anlaşılıyor.PHP kodundaki güvenli olmayan system() çağrısı nedeniyle, bu dosya sistemde uzaktan keyfi komutların çalıştırılmasına izin verir.
Saldırgan muhtemelen web sunucusundan kendi sistemlerine daha kararlı bir bağlantı kurmak için bunu istismar etti.

Saldırıya yol açan yüklenen dosyayı belirledikten sonra, isteği ilişkilendirmek ve saldırı hakkında daha fazla bilgi edinmek için web sunucusu günlüklerine bakmak iyi bir fikirdir.Apache veya Nginx günlükleri gibi web sunucusu günlükleri, saldırganın faaliyetleri, istek kalıpları ve kökeni hakkında değerli bilgiler sağlayabilir

## Sahiplik ve İzinler
Dosya sahipliği ve izinler sistem güvenliğinin kritik yönleridir.Saldırganlar genellikle kötü amaçlı dosyaları yüklemek için yazma izinlerine sahip dizinleri hedefler. Yaygın yazılabilir dizinler şunlardır:

* **/tmp:** Geçici dizin tüm kullanıcılar tarafından yazılabilir olduğundan yaygın bir tercihtir.
* **/var/tmp:** Genellikle tüm dünyaya yazma izinlerine sahip geçici bir dizindir.
* **/dev/shm:** Paylaşımlı bellek dosya sistemidir ve normalde tüm kullanıcılar tarafından yazılabilir.

Bu dizinlerdeki dosyaları listelemek ve şüpheli dosyaları veya değişiklikleri araştırmak için ls -al komutunu çalıştırmak iyi bir fikirdir. Ayrıca, kriterlerimize uyan dosyaları hızlı bir şekilde belirlemek için find komutunu da kullanabiliriz. Örneğin:

![image](https://github.com/user-attachments/assets/3b97b31e-9dd5-4751-abb0-1db2b84a2219)

Yukarıdaki komut www-data kullanıcısının sahip olduğu tüm dosyaları kök dizinden başlayarak listeler ve döndürür.Ayrıca komutun çıktısını less komutuna yönlendiriyoruz, bu da çıktıyı kaydırmamızı ve sayfalandırmamızı sağlıyor, çünkü muhtemelen çok sayıda giriş olacak.
Less komutundan çıkmak için Q tuşuna basın.
Komutun çıktısında birkaç iyi huylu girdi görüyoruz. Ancak, göze çarpanlardan biri /var/www/html/assets/ dizininde listelenen reverse.elf.Dosyayı daha ayrıntılı olarak listelediğimizde (ls -l /var/www/html/assets/reverse.elf), dosya izinlerinin bu dosyanın x biti ile tanımlanan tüm kullanıcılar tarafından çalıştırılabilir olduğunu gösterdiğini görebiliriz:

![image](https://github.com/user-attachments/assets/a1f40d71-a5e1-4b24-9db7-13cc27bd61a5)

reverse.elf dosyasını daha fazla incelemeden önce, bir inceleme sırasında belirli dosyaları çekmek için kullanılabilecek birkaç yararlı find komutu daha vardır:

![image](https://github.com/user-attachments/assets/25fbfc85-eade-4347-966a-812202bf1724)

* Belirli bir gruba ait dosya ve dizinlerin listesini alın.
* Tüm dünya tarafından yazılabilir dosyaların ve dizinlerin listesini alın.
* Son beş dakika içerisinde oluşturulan veya değiştirilen dosyaların listesini alın.

### Not : Her komutun ardından, izinlerden kaynaklanabilecek herhangi bir hata mesajını bastırarak çıktıyı temizlemek için 2>/dev/null komutunun geldiğine dikkat edin.

## Metadata
Meta veri, dosyaları tanımlayan gömülü bilgileri ifade eder ve bir dosyanın özellikleri, kökenleri ve nitelikleri hakkında bilgi sağlar.Dosya oluşturma tarihleri, yazar bilgileri, kompozisyon ve dosya türleri gibi çeşitli bilgi türlerini içerebilir.
Bir sistemde canlı analiz gerçekleştirirken meta veriler, belirli dosyaların köken ve değişiklik zaman damgalarını ve bazı durumlarda yazar ayrıntılarını belirlemede oldukça yararlı olabilir.

Exiftool, dosya başlıklarını ve gömülü meta veri yapılarını ayrıştırarak dosyalardan meta verileri çıkarmak ve değiştirmek için kapsamlı yeteneklere sahip Perl tabanlı bir komut satırı yardımcı programıdır.
Örneğin, şüpheli reverse.elf dosyasının meta verilerini aşağıdaki komutu çalıştırarak analiz edebiliriz:

![image](https://github.com/user-attachments/assets/c1e391ec-863e-4a7b-b67a-6dd6ebc138a5)

Yukarıdaki çıktıda görüldüğü gibi, ExifTool bize bu dosya hakkında türü, boyutu, izinleri, mimarisi ve hatta değişiklik ve erişim zaman damgaları gibi daha fazla ayrıntı verir.

## Kontrol Toplamlarını Analiz Etme
Kontrol toplamları, kriptografik karma işlevleri (MD5 veya SHA-256 gibi) kullanılarak verilerden üretilen benzersiz değerlerdir.Bu fonksiyonlar, verileri temsil eden sabit boyutlu karakter dizileri üretir; böylece verilerdeki küçük bir değişiklik bile önemli ölçüde farklı bir sağlama toplamına yol açar

Kontrol toplamları genellikle veri bütünlüğünü doğrulamak için kullanılır ve verilerin değiştirilmediğinden veya bozulmadığından emin olunur.Olay müdahale ekipleri için, bilinen imzalara dayanarak kötü amaçlı dosyaları ve yürütülebilir dosyaları tanımlamak amacıyla da kullanılabilirler.

Daha önce tanımladığımız reverse.elf dosyasının karma değerlerini incelemek için iki yararlı checksum yardımcı programından yararlanabiliriz. Dosyada hem md5sum hem de sha256sum çalıştırarak karma değerini çıktı olarak alabiliriz:

![image](https://github.com/user-attachments/assets/e2a9c923-ec42-4df1-9922-69f366d262ec)

Karma değerlerini elde ettiğimizde, bunları daha detaylı analiz için VirusTotal gibi bir kötü amaçlı yazılım tespit servisine gönderebiliriz.Bunu yaptığımızda, çeşitli satıcıların bu dosyayı bir Meterpreter ters kabuk yükü olarak işaretlediğine dair kanıt bulacağız.
Bu hızlı analiz, saldırganın web sunucusuna etkileşimli bir ters kabuk bağlantısı elde etmek için ilk RCE'sini kullanarak reverse.elf dosyasını yerleştirdiğini ve çalıştırdığını gösteriyor.

## Zaman damgaları
Zaman damgaları, belirli bir eylemin ne zaman gerçekleştiğini gösteren dosyalarla veya olaylarla ilişkili ek meta veri parçalarıdır.
Zaman damgaları, olay müdahalesi ve adli bilişim faaliyetlerinde dosya ve dizinlerin oluşturulma, değiştirilme ve erişim sürelerinin izlenmesi için en önemli unsurlardan biridir.Bu zaman damgaları, adli soruşturmalarda paha biçilmezdir, çünkü olayların sırası ve bir sistemde gerçekleştirilen eylemler hakkında temel ipuçları sağlar ve bir zaman çizelgesi oluşturmaya yardımcı olur.

Unix tabanlı sistemlerde genellikle üç ana zaman damgası kaydedilir:

* **Zaman Damgasını Değiştir (mtime):** Bu zaman damgası, bir dosyanın içeriğinin son olarak ne zaman değiştirildiğini veya düzenlendiğini yansıtır. Bir dosyaya her yazıldığında veya dosya değiştirildiğinde, mtime'ı güncellenir.
* **Zaman Damgasını Değiştir (ctime):** Bu zaman damgası, bir dosyanın meta verilerinin son olarak ne zaman değiştirildiğini gösterir.Meta veriler, izinler, sahiplik veya dosya adının kendisi gibi öznitelikleri içerir. Bir dosyayla ilişkili herhangi bir meta veri değiştiğinde, ctime'ı güncellenir.
* **Erişim Zaman Damgası (atime):** Bu zaman damgası, bir dosyaya en son ne zaman erişildiğini veya okunduğunu gösterir. Bir dosya her açıldığında, atime'ı güncellenir.

Aşağıdaki komutu çalıştırarak bir dosyanın Değiştirme Zaman Damgasını (mtime) kolayca görüntüleyebiliriz:

![image](https://github.com/user-attachments/assets/9a156d39-99e1-4e5e-8642-cca92145ac32)

Aynı dosyanın Değişiklik Zaman Damgasını (ctime) görüntülemek için şunu çalıştırabiliriz:

![image](https://github.com/user-attachments/assets/4ae4b93e-f2e3-4da7-9600-4a887afc6fde)

Son olarak dosyanın Erişim Zaman Damgasını (atime) görüntülemek için şunu çalıştırabiliriz:

![image](https://github.com/user-attachments/assets/36159893-fe1f-4099-b667-37ba512cf298)

Belirtildiği üzere, bir dosyanın Erişim Zaman Damgası (atime), soruşturma eylemleri gerçekleştirdiğimiz sırada kolayca ve istemeden güncellenebilir.Meta verileri ExifTool kullanarak görüntülediğimizde veya md5sum veya sha256sum ile sağlama toplamlarını analiz ettiğimizde, reverse.elf üzerinde okuma eylemleri gerçekleştirdik, böylece erişim zamanını değiştirdik.

Bu, canlı adli analizde dikkate alınması gereken önemli bir kavramdır, bu nedenle etkilenen sistemin adli açıdan sağlam yedeklerini ve kopyalarını önceden elde etmek hayati önem taşır.Bu nedenle zaman bizim için güvenilir bir ölçüt olmayacaktır.

Yukarıdaki üç komutu hatırlamak faydalı olsa da, üç zaman damgasını aynı anda hızlıca görmek için stat komutunu da kullanabiliriz:

![image](https://github.com/user-attachments/assets/90e8125f-e296-47d9-ae79-069b4f479243)











