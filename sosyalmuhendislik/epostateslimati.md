# Kimlik Avı Analizinin Temelleri(Sosyal Mühendislik)
Spam ve Kimlik Avı yaygın sosyal mühendislik saldırılarıdır. Sosyal mühendislikte kimlik avı saldırısı vektörleri bir telefon görüşmesi, kısa mesaj veya e-posta olabilir. Tahmin edebileceğiniz gibi, saldırı vektörü olarak odak noktamız e-postadır.

Spam olarak sınıflandırılan ilk e-postanın tarihi 1978 yılına dayanıyor ve bugün hâlâ varlığını sürdürüyor.

Kimlik avı, bir savunmacı olarak sizin de savunmanız gereken ciddi bir saldırı vektörüdür.

Pek çok ürün spam ve kimlik avı ile mücadeleye yardımcı olur, ancak gerçekçi olmak gerekirse bu e-postalar yine de iletilebilir. Bunu yaptıklarında, bir Güvenlik Analisti olarak bu e-postaların kötü amaçlı mı yoksa iyi niyetli mi olduğunu belirlemek için nasıl analiz edeceğinizi bilmeniz gerekir.

Ayrıca, kötü amaçlı e-postaların kullanıcının gelen kutusuna geri dönmesini önlemek amacıyla güvenlik ürünlerinizi güncellemek için e-posta hakkında bilgi toplamanız gerekecektir.

### E-Posta Hakkında

E-postanın icadı ARPANET için 1970'li yıllara dayanmaktadır.letişim şeklimize katkı sağlayan kişi Ray Tomlinson'du.

Peki bir e-posta adresini neler oluşturur?

* **Kullanıcı Adı (Username)**
* **@**
* **Domain**

 **Giden ve gelen e-posta mesajlarını kolaylaştırmak için 3 özel protokol vardır ve bunlar aşağıda kısaca listelenmiştir.**

 * **SMTP-(Simple Mail Transfer Protocol) (Basit Posta Aktarım Protokolü)** E-postaların gönderilmesini yönetmek için kullanılır.
 * **POP3- (Post Office Protocol) (Postane Protokolü)** Bir istemci ile posta sunucusu arasında e-postanın aktarılmasından sorumludur.
 * **IMAP-(Internet Message Access Protocol) (İnternet Mesaj Erişim Protokolü)** Bir istemci ile posta sunucusu arasında e-postanın aktarılmasından sorumludur.

Hem POP3'ün hem de IMAP'nin aynı tanıma sahip olduğunu fark etmiş olmalısınız. Fakat ikisi arasında farklar var.

### POP3

* **E-postalar tek bir cihaza indirilir ve saklanır.**
* **Gönderilen mesajlar, e-postanın gönderildiği tek cihazda saklanır.**
* **E-postalara yalnızca e-postaların indirildiği tek cihazdan erişilebilir.**
* **Mesajları sunucuda tutmak istiyorsanız "E-postayı sunucuda tut" ayarının etkinleştirildiğinden emin olun veya tek cihazın uygulamasına veya yazılımına indirildikten sonra tüm mesajlar sunucudan silinir.**

### IMAP

* **E-postalar sunucuda saklanır ve birden fazla cihaza indirilebilir**
* **Gönderilen mesajlar sunucuda saklanır.**
* **Mesajlar birden fazla cihazda senkronize edilebilir ve erişilebilir.**

Şimdi e-postanın göndericiden alıcıya nasıl ulaştığından bahsedelim. Bunu en iyi şekilde açıklamak için aşağıdaki aşırı basitleştirilmiş resme bakın:

![image](https://github.com/user-attachments/assets/dbd9d047-66f9-40da-9e07-8e00924d3d09)

Aşağıda yukarıdaki diyagramdaki her numaralandırılmış noktanın açıklaması bulunmaktadır:

* **Alexa, en sevdiği e-posta istemcisinde Billy'ye (billy@johndoe.com) bir e-posta yazıyor. İşi bittikten sonra gönder tuşuna basıyor.**
* **SMTP sunucusunun Alexa'nın e-postasını nereye göndereceğini belirlemesi gerekiyor. Johndoe.com ile ilişkili bilgiler için DNS'yi sorgular.**
* **DNS sunucusu johndoe.com bilgisini alır ve bu bilgiyi SMTP sunucusuna gönderir.**
* **SMTP sunucusu Alexa'nın e-postasını İnternet üzerinden Billy'nin johndoe.com adresindeki posta kutusuna gönderir.**
* **Bu aşamada Alexa'nın e-postası çeşitli SMTP sunucularından geçer ve sonunda hedef SMTP sunucusuna iletilir.**
* **Alexa'nın e-postası sonunda hedef SMTP sunucusuna ulaştı.**
* **Alexa'nın e-postası iletildi ve şu anda yerel POP3/IMAP sunucusunda Billy'yi bekliyor.**
* **Billy, posta kutusundaki yeni e-postalar için yerel POP3/IMAP sunucusunu sorgulayan e-posta istemcisinde oturum açar.**
* **Alexa'nın e-postası Billy'nin e-posta istemcisine kopyalanır (IMAP) veya indirilir (POP3).**




