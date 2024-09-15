### E-postalarla ilgili genel kavramları ve göndericiden alıcıya nasıl ulaştığını anlattığımıza göre artık bu iletişim yönteminin nasıl kötü amaçlarla kullanıldığına geçebiliriz.

**Farklı türdeki kötü amaçlı e-postalar aşağıdakilerden biri olarak sınıflandırılabilir:**

* **Spam** - çok sayıda alıcıya toplu olarak gönderilen istenmeyen önemsiz e-postalardır. Spam'in daha kötü niyetli çeşidi MalSpam olarak bilinir.
* **Kimlik avı(pishing)** - bireyleri hassas bilgiler vermeye teşvik etmek amacıyla güvenilir bir kuruluştan geliyormuş gibi görünen hedeflere gönderilen e-postalar.
* **Hedef odaklı kimlik avı(spear pishing)** - hassas bilgiler arayan belirli bireyleri veya kuruluşları hedefleyerek kimlik avını bir adım daha ileri götürür.
* **Balina avcılığı(Whaling)** - hedef odaklı kimlik avına benzer, ancak özellikle C Düzeyi üst düzey bireyleri (CEO, CFO vb.) hedef alır ve amaç aynıdır.
* **Smishing(sms oltalama)** - mobil kullanıcıları özel hazırlanmış metin mesajlarıyla hedefleyerek kimlik avını mobil cihazlara taşır.
* **Vishing(Sesli oltalama)** - smishing'e benzer, ancak sosyal mühendislik saldırısı için kısa mesaj kullanmak yerine saldırılar sesli aramalara dayalıdır.

### Kimlik avı e-postalarının ortak özellikleri aşağıda verilmiştir:

* **Gönderenin e-posta adı/adresi** güvenilir bir varlıkmış gibi görünecektir **(e-posta sahteciliği)**
* E-postanın konu satırı ve/veya metni (metin) **aciliyet duygusuyla** yazılmıştır veya **Fatura, Askıya Alındı** ​​vb. gibi belirli anahtar kelimeleri kullanır.
* E-posta gövdesi (HTML), güvenen bir varlıkla (Amazon gibi) eşleşecek şekilde tasarlanmıştır
* E-posta gövdesi (HTML) kötü biçimlendirilmiş veya yazılmış (önceki noktanın aksine)
* E-posta gövdesi Sayın Bay/Bayan gibi **genel içerik** kullanır.
* Köprüler (gerçek kaynağını gizlemek için çoğu zaman URL kısaltma hizmetlerini kullanır)
* **Meşru** bir belge gibi görünen kötü amaçlı bir ek

**Hatırlatma: Köprüler ve eklerle uğraşırken, yanlışlıkla köprüye veya eke tıklamamaya dikkat etmeniz gerekir.**

### Köprüler ve IP adresleri 'kaldırılmış' olmalıdır. Defanging, ciddi bir güvenlik ihlaline yol açabilecek kazara tıklamaları önlemek için URL'yi/alanı veya e-posta adresini tıklanamaz hale getirmenin bir yoludur.
E-postadaki "@" veya "." gibi özel karakterlerin yerine geçer. URL'de farklı karakterlerle.Örneğin, oldukça şüpheli bir alan adı olan http://www.suspiciousdomain.com, tespit için SOC ekibine iletilmeden önce hxxp[://]www[.]suspiciousdomain[.]com olarak değiştirilecektir.
