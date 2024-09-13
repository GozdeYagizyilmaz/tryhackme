# Web Uygulama Güvenliği

### Bir web uygulaması, modern standart bir web tarayıcımız olduğu sürece kurulum yapmadan kullanabileceğimiz bir “program” gibidir,Firefox, Safari veya Chrome gibi. Dolayısıyla ihtiyacınız olan her programı yüklemek yerine sadece ilgili sayfayı gezmeniz yeterli. Aşağıda web uygulamalarına bazı örnekler verilmiştir:

* Tutanota, Protonmail, Outlook ve Gmail gibi web postası
* Microsoft Office 365 (Word, Excel ve PowerPoint), Google Drive (Dokümanlar, E-Tablolar ve Slaytlar) ve Zoho Office (Writer, Sheet ve Show) gibi çevrimiçi ofis paketleri
* Amazon.com, AliExpress ve Etsy gibi çevrimiçi alışverişler

### Binlerce örnek daha sayısız hizmet sağlıyor. Diğer örnekler arasında çevrimiçi bankacılık, para transferi, hava durumu tahmini ve sosyal medya yer alır.

### Bir web uygulamasının fikri, uzak bir sunucuda çalışan bir program olmasıdır.Sunucu, istemcilere “hizmet vermek” için sürekli çalışan bir bilgisayar sistemini ifade eder. Bu durumda sunucu, web tarayıcıları tarafından erişilebilen belirli bir program türünü çalıştıracaktır.

Çevrimiçi bir alışveriş uygulamasını düşünün.Web uygulaması, ürünlerle ilgili verileri ve bunların ayrıntılarını bir veritabanı sunucusundan okuyacaktır.Veritabanı, bilgileri düzenli bir şekilde depolamak için kullanılır. Örnekler arasında ürünler, müşteriler ve faturalarla ilgili bilgiler yer alır.

Bir veritabanı sunucusu, veritabanına okuma, arama ve yazma dahil olmak üzere birçok işlevden sorumludur.Çevrimiçi alışveriş web uygulamasının birden fazla veritabanına erişmesi gerekebilir, örneğin:

*  **Ürün veritabanı: Bu veritabanı, ürünlerle ilgili ad, görsel, teknik özellikler ve fiyat gibi ayrıntıları içerir.**
*  **Müşteri veritabanı: Müşterilerle ilgili isim, adres, e-posta ve telefon numarası gibi tüm ayrıntıları içerir.**
*  **Satış veritabanı: Her müşterinin ne satın aldığını ve nasıl ödeme yaptığını bu veritabanında görmeyi bekliyoruz.**

  Herhangi bir çevrimiçi alışveriş sisteminde depolanan bilgi miktarını zaten görebiliyoruz.Bir saldırganın web uygulamasından yararlanmayı (hacklemeyi) ve müşterilerin veritabanını çalmayı başardığını varsayalım. Bu durumda firma ve müşterileri açısından ciddi bir kayıp yaşanacaktır.

  Aşağıdaki resimde bir çevrimiçi alışveriş sitesinde bir ürünün aranması gösterilmektedir. En basit versiyonda arama dört adımdan oluşacaktır:

  ![image](https://github.com/user-attachments/assets/f3db6cab-1853-4c93-9e77-7a387d88f5ff)

Birçok şirket hata ödül programları sunmaktadır. Bir hata ödül programı, şirketin sistemlerinde bir güvenlik açığı (zayıflık) keşfeden herkese bir ödül sunmasına olanak tanır.

  Ana koşul, bulunan güvenlik açığının bug bounty kapsamı ve kuralları dahilinde olmasıdır. Diğerlerinin yanı sıra Google, Microsoft ve Facebook'un hata ödül programları var.

  Bir hatayı keşfetmeniz, güvenlik açığının ciddiyetine, yani keşfettiğiniz zayıflığa bağlı olarak size birkaç yüz ABD Dolarından onbinlerce ABD Dolarına kadar kazanç sağlayabilir.

  ### Diyelim ki bir online mağazadan ürün satın almak istiyorsunuz. Bu web uygulamasında yapmayı bekleyebileceğiniz belirli işlevler vardır. En basit haliyle çevrimiçi sipariş şu şekilde olabilir:

  ![image](https://github.com/user-attachments/assets/ac51b320-254c-4198-b9b2-f5dc8b557658)

 ### Web uygulamalarına yönelik yaygın saldırıların birkaç ana kategorisi vardır:

* **Web sitesine giriş yapın: Saldırgan birçok kelimeyi deneyerek şifreyi keşfetmeye çalışabilir. Saldırgan, otomatik bir araçla uzun bir şifre listesi kullanarak bunları giriş sayfasında test eder.**
* **Ürünü arayın: Saldırgan, arama terimine belirli karakterler ve kodlar ekleyerek sistemi ihlal etmeye çalışabilir.Saldırganın amacı, hedef sistemin vermemesi gereken verileri döndürmesi veya vermemesi gereken bir programı çalıştırmasıdır.**
* **Ödeme ayrıntılarını sağlayın: Saldırgan, ödeme ayrıntılarının açık metin olarak mı yoksa zayıf şifreleme kullanılarak mı gönderildiğini kontrol eder.**

  ## Tanımlama ve Kimlik Doğrulama Hatası
  **Kimlik belirleme, bir kullanıcıyı benzersiz şekilde tanımlama yeteneğini ifade eder.Bunun aksine, kimlik doğrulama, kullanıcının iddia ettiği kişi olduğunu kanıtlama yeteneğini ifade eder.Çevrimiçi mağazanın, kullanıcının kimliğini onaylaması ve sistemi kullanmadan önce kimlik doğrulaması yapması gerekir.
  Ancak bu adım farklı türde zayıflıklara açıktır. Örnek zayıflıklar şunları içerir:**
* **Saldırganın kaba kuvvet kullanmasına izin vermek, yani geçerli oturum açma kimlik bilgilerini bulmak için genellikle otomatik araçları kullanarak birçok şifreyi denemek.**
* **Kullanıcının zayıf bir şifre seçmesine izin vermek. Zayıf bir şifrenin tahmin edilmesi genellikle kolaydır.**
* **Kullanıcıların şifrelerinin düz metin olarak saklanması. Saldırgan şifreleri içeren dosyayı okumayı başarırsa saklanan şifreyi öğrenmesini istemeyiz.**
  
![image](https://github.com/user-attachments/assets/6421c0d4-2f59-4159-8221-c8c4a1fcc96a)

## Bozuk Erişim Kontrolü
**Erişim kontrolü, her kullanıcının yalnızca rolü veya işiyle ilgili dosyalara (belgeler, resimler vb.) erişebilmesini sağlar.Örneğin, pazarlama departmanındaki birinin finans departmanının belgelerine erişmesini (okumasını) istemezsiniz. Erişim kontrolüyle ilgili örnek güvenlik açıkları şunları içerir:**

* **En az ayrıcalık ilkesinin uygulanmaması ve kullanıcılara ihtiyaç duyduklarından daha fazla erişim izni verilmesi.Örneğin, çevrimiçi bir müşteri, ürünlerin fiyatlarını görebilmeli ancak değiştirememelidir.**
* **Benzersiz tanımlayıcıyı kullanarak başka birinin hesabını görüntüleyebilme veya değiştirebilme.Örneğin bir banka müşterisinin başka bir müşterinin işlemlerini görebilmesini istemezsiniz.**
* **Kimliği doğrulanmamış bir kullanıcı olarak kimlik doğrulaması gerektiren (oturum açma) sayfalara göz atabilme. Örneğin, oturum açmadan önce kimsenin web postasını görüntülemesine izin veremeyiz.**

## Enjeksiyon Saldırısı
Enjeksiyon saldırısı, web uygulamasındaki kullanıcının girişinin bir parçası olarak kötü amaçlı kod ekleyebileceği bir güvenlik açığını ifade eder.Bu güvenlik açığının bir nedeni, kullanıcının girişinin uygun şekilde doğrulanmaması ve sterilize edilmemesidir.

## Şifreleme Hataları
**Bu kategori kriptografiyle ilgili hataları ifade eder. Kriptografi, verilerin şifrelenmesi ve şifresinin çözülmesi süreçlerine odaklanır.Şifreleme, açık metni şifreli metne dönüştürür; bu, şifresini çözecek gizli anahtara sahip olmayan herkes için anlamsız olacaktır.
Başka bir deyişle şifreleme, gizli anahtarı bilmeden hiç kimsenin verileri okuyamamasını sağlar. Şifre çözme, gizli anahtarı kullanarak şifreli metni orijinal açık metne geri dönüştürür. Şifreleme hatalarına örnekler şunları içerir:**

* **Hassas verileri açık metin olarak göndermek (örneğin, HTTPS yerine HTTP kullanmak). HTTP, web'e erişmek için kullanılan protokoldür, HTTPS ise HTTP'nin güvenli sürümüdür. Diğerleri HTTP üzerinden gönderdiğiniz her şeyi okuyabilir ancak HTTPS'yi okuyamaz.**
* **Zayıf bir şifreleme algoritmasına güvenmek. Eski bir şifreleme algoritması, her harfi birer birer kaydırmaktır. Örneğin, "TRY HACK ME", "USZ IBDL NF" olur. Bu şifreleme algoritmasının kırılması önemsizdir.**
* **Şifreleme işlevleri için varsayılan veya zayıf anahtarların kullanılması. 1234'ü gizli anahtar olarak kullanan şifrelemeyi kırmak zor olmayacak**

  







  
  
  
