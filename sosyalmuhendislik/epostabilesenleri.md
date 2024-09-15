### İşte bir e-postanın iki bölümü:
1- **e-posta başlığı** (e-postayı aktaran e-posta sunucuları gibi e-postayla ilgili bilgiler)

2- **e-posta gövdesi** (metin ve/veya HTML biçimli metin)

![image](https://github.com/user-attachments/assets/a1b6858b-e15f-4d3d-9d04-016d95227698)


### Potansiyel olarak kötü amaçlı bir e-postayı analiz ederken nelere dikkat edersiniz?

**Aşağıdaki e-posta başlığı alanlarıyla başlayalım:**

1- **From-Kimden** gönderenin e-posta adresi

2- **Subject-Konu** e-postanın konu satırı

3- **Date-Tarih** e-postanın gönderildiği tarih

4- **To-Alıcı** alıcının e-posta adresi

 Bu genellikle herhangi bir e-posta istemcisinde açıkça görülebilir. Aşağıdaki resimde bu alanların bir örneğine bakalım.

 ### Uyarı: Bu gerçek bir e-postadan bir kesittir. Aşağıdaki resimdeki e-posta bir honeypot Yahoo e-posta adresinden gelmektedir. Bu odada açıklanan e-posta adresleri veya IP adresleriyle etkileşime girmeyin/etkileşime girmeyin.

![image](https://github.com/user-attachments/assets/7a611f2e-8e47-4336-8575-73ba5223810d)

**Not:** Yukarıdaki resimdeki sayılar, yukarıdaki e-posta başlığı alanları madde işareti listesine karşılık gelir. Aynı e-posta başlığı bilgilerini ve daha fazlasını elde etmenin başka bir yöntemi de 'ham' e-posta ayrıntılarını görüntülemektir.
Aşağıdaki görselde bu bilgilerin Yahoo içerisinde nasıl görüntüleneceğini görebilirsiniz.

![image](https://github.com/user-attachments/assets/29d3a32f-72e5-4fbc-8f83-6167f6fccf67)

### Aşağıda e-posta örneği için ham mesajın bir pasajı bulunmaktadır.

![image](https://github.com/user-attachments/assets/40a7cb3e-28b1-4288-a54a-76065cf77f97)

Yukarıdaki resimde başka ilgi çekici e-posta başlığı alanları da bulunmaktadır.

* **X-Originating-IP** - E-postanın gönderildiği IP adresi (bu, X başlığı olarak bilinir)
* **Smtp.mailfrom/header.from** - E-postanın gönderildiği alan adı (bu başlıklar Kimlik Doğrulama Sonuçları'nın içindedir)
* **Reply to-Yanıtla** - Bu, Gönderen e-posta adresi yerine yanıt e-postasının gönderileceği e-posta adresidir

Açıklığa kavuşturmak gerekirse, yukarıdaki örnekte yer alan e-postada Gönderen, newsletters@ant.anki-tech.com'dur, ancak bir alıcı e-postayı yanıtlarsa yanıt answer@ant.anki-tech.com adresine gidecektir. Yanıtla ve newsletters@ant.anki-tech.com adresine DEĞİL.

Aşağıda, e-posta başlıklarının nasıl analiz edileceğine ilişkin Medya Şablonu'ndan ek bir kaynak bulunmaktadır:

https://web.archive.org/web/20221219232959/https://mediatemple.net/community/products/all/204643950/understanding-an-email-header




