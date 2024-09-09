# Savunma Güvenliğine Giriş

**Saldırgan güvenlik tek bir şeye odaklanır: sistemlere sızma. Sistemlere sızma, diğer şeylerin yanı sıra hatalardan yararlanarak, güvenli olmayan kurulumları kötüye kullanarak ve zorunlu olmayan erişim kontrolü politikalarından yararlanarak gerçekleştirilebilir.
Kırmızı ekipler ve penetrasyon test uzmanları saldırı güvenliği konusunda uzmanlaşmıştır. Savunma güvenliği, iki ana görevle ilgili olduğundan, saldırı güvenliğinin biraz tersidir:**

- İzinsiz girişlerin meydana gelmesini önleme
- İzinsiz girişleri ortaya çıktıklarında tespit etme ve uygun şekilde yanıt verme

## Mavi takımlar savunma güvenliği ortamının bir parçasıdır.  
### Savunma güvenliğiyle ilgili görevlerden bazıları şunlardır:

- **Kullanıcı siber güvenlik farkındalığı: Kullanıcıların siber güvenlik konusunda eğitilmesi, sistemlerini hedef alan çeşitli saldırılara karşı korunmaya yardımcı olur.**
- **Varlıkları belgelemek ve yönetmek: Doğru şekilde yönetmemiz ve korumamız gereken sistem ve cihaz türlerini bilmemiz gerekir.**
- **Sistemlerin güncellenmesi ve yama uygulanması: Bilgisayarların, sunucuların ve ağ cihazlarının doğru şekilde güncellenmesinin ve bilinen herhangi bir güvenlik açığına (zayıflık) karşı yama uygulanmasının sağlanması.**
- **Önleyici güvenlik cihazlarının kurulması: güvenlik duvarı ve izinsiz giriş önleme sistemleri (IPS), önleyici güvenliğin kritik bileşenleridir. Güvenlik duvarları hangi ağ trafiğinin içeri girebileceğini ve nelerin sistemden veya ağdan çıkabileceğini kontrol eder.IPS, mevcut kurallarla ve saldırı imzalarıyla eşleşen tüm ağ trafiğini engeller.**
- **Günlük kaydı ve izleme cihazlarının kurulması: Ağın uygun şekilde günlüğe kaydedilmesi ve izlenmesi olmadan, kötü amaçlı etkinliklerin ve izinsiz girişlerin tespit edilmesi mümkün olmayacaktır. Ağımızda yeni bir yetkisiz cihaz belirirse bunu bilmemiz gerekir.**

**Savunma güvenliğine ilişkin çok daha fazlası var ve yukarıdaki liste yalnızca birkaç genel konuyu kapsıyor. Bu yazıda şunları ele alıyoruz:**

1. Güvenlik Operasyon Merkezi (SOC)(Security Operations Center) 
2. Tehdit İstihbaratı
3. Dijital Adli Tıp ve Olay Müdahalesi (DFIR)(Digital Forensics and Incident Response)
4. Kötü Amaçlı Yazılım Analizi

### Bu görevde savunma güvenliğiyle ilgili iki ana konuyu ele alacağız:

- **Tehdit İstihbaratını ele aldığımız Güvenlik Operasyon Merkezi (SOC)**
- **Kötü Amaçlı Yazılım Analizini de kapsadığımız Dijital Adli Tıp ve Olay Müdahalesi (DFIR)**

![image](https://github.com/user-attachments/assets/5d069dcb-e032-4c02-9ee4-10939c8a091c)

## Güvenlik Operasyon Merkezi (SOC)

**Güvenlik Operasyon Merkezi (SOC), kötü niyetli siber güvenlik olaylarını tespit etmek için ağı ve sistemlerini izleyen siber güvenlik uzmanlarından oluşan bir ekiptir. 
Bir SOC'nin ana ilgi alanlarından bazıları şunlardır:**

- **Güvenlik açıkları: Bir sistem güvenlik açığı (zayıflığı) keşfedildiğinde, uygun bir güncelleme veya yama yüklenerek düzeltilmesi önemlidir.Bir düzeltme mevcut olmadığında, saldırganın bunu kötüye kullanmasını önlemek için gerekli önlemler alınmalıdır.Her ne kadar güvenlik açıklarının düzeltilmesi SOC için hayati öneme sahip olsa da bu görevin onlara atanması şart değildir.**
- **Politika ihlalleri: Güvenlik politikasını, ağın ve sistemlerin korunması için gerekli olan bir dizi kural olarak düşünebiliriz.Örneğin, kullanıcıların gizli şirket verilerini bir çevrimiçi depolama hizmetine yüklemeye başlaması bir politika ihlali olabilir.**
- **Yetkisiz etkinlik: Bir kullanıcının oturum açma adının ve parolasının çalındığı ve saldırganın bunları ağda oturum açmak için kullandığı durumu düşünün. Bir SOC'nin böyle bir olayı tespit etmesi ve daha fazla hasar meydana gelmeden mümkün olan en kısa sürede engellemesi gerekir.**
- **Ağa izinsiz girişler: Güvenliğiniz ne kadar iyi olursa olsun, izinsiz giriş ihtimali her zaman vardır.Bir kullanıcı kötü amaçlı bir bağlantıya tıkladığında veya bir saldırgan genel sunucudan yararlandığında izinsiz giriş meydana gelebilir. Her iki durumda da, bir izinsiz giriş meydana geldiğinde, daha fazla hasarı önlemek için bunu mümkün olan en kısa sürede tespit etmeliyiz.**

### Güvenlik operasyonları, korumayı sağlamaya yönelik çeşitli görevleri kapsar; Bu tür görevlerden biri tehdit istihbaratıdır.

## Tehdit İstihbaratı
**Bu bağlamda istihbarat, gerçek ve potansiyel düşmanlar hakkında topladığınız bilgileri ifade eder. Tehdit, bir sistemi bozabilecek veya olumsuz yönde etkileyebilecek herhangi bir eylemdir.
Tehdit istihbaratı, şirketin potansiyel düşmanlara karşı daha iyi hazırlanmasına yardımcı olacak bilgileri toplamayı amaçlamaktadır.Amaç, tehdit bilgisine sahip bir savunma elde etmek olacaktır. Farklı şirketlerin farklı rakipleri vardır.
Bazı saldırganlar bir mobil operatörden müşteri verilerini çalmaya çalışabilir; ancak diğer rakipler petrol rafinerisindeki üretimi durdurmakla ilgileniyor.Örnek düşmanlar arasında siyasi nedenlerle çalışan bir ulus devlet siber ordusu ve mali amaçlarla hareket eden bir fidye yazılımı grubu yer alıyor. Şirkete (hedefe) bağlı olarak düşmanlar bekleyebiliriz.**

**İstihbaratın verilere ihtiyacı var. Verilerin toplanması, işlenmesi ve analiz edilmesi gerekir. Veri toplama, ağ günlükleri gibi yerel kaynaklardan ve forumlar gibi genel kaynaklardan yapılır.
Verilerin işlenmesi, bunların analize uygun bir formatta düzenlenmesini amaçlamaktadır. Analiz aşaması, saldırganlar ve onların amaçları hakkında daha fazla bilgi bulmayı amaçlamaktadır; dahası, tavsiyelerin ve uygulanabilir adımların bir listesini oluşturmayı amaçlamaktadır.**

**Düşmanlarınız hakkında bilgi edinmek onların taktiklerini, tekniklerini ve prosedürlerini bilmenizi sağlar.ehdit istihbaratı sonucunda tehdit aktörünü (düşmanı) belirliyoruz, aktivitelerini tahmin ediyoruz ve bunun sonucunda saldırılarını azaltıp karşılık stratejisi hazırlıyoruz.**

##Dijital Adli Tıp ve Olay Müdahalesi (DFIR)

**Bu bölüm Dijital Adli Tıp ve Olay Müdahalesi (DFIR) ile ilgilidir ve şunları ele alacağız:**

- Dijital Adli Tıp
- Olay Müdahalesi
- Kötü Amaçlı Yazılım Analizi


### Dijital Adli Tıp
**Adli tıp, suçları araştırmak ve gerçekleri tespit etmek için bilimin uygulanmasıdır.Bilgisayarlar ve akıllı telefonlar gibi dijital sistemlerin kullanımı ve yaygınlaşmasıyla birlikte, ilgili suçları araştırmak için yeni bir adli tıp dalı doğdu: bilgisayar adli bilimi, daha sonra dijital adli bilime dönüştü.**

Savunma güvenliğinde, dijital adli bilimin odak noktası, bir saldırının kanıtlarını ve onun faillerini ve fikri mülkiyet hırsızlığı, siber casusluk ve yetkisiz içeriğe sahip olma gibi diğer alanları analiz etmeye kayar.

Sonuç olarak, dijital adli tıp aşağıdaki gibi farklı alanlara odaklanacaktır:

- **Dosya Sistemi: Bir sistemin depolama alanının dijital adli tıp görüntüsünün (düşük seviyeli kopya) analiz edilmesi, yüklü programlar, oluşturulan dosyalar, kısmen üzerine yazılan dosyalar ve silinmiş dosyalar gibi birçok bilgiyi ortaya çıkarır.**
- **Sistem belleği: Saldırgan, kötü amaçlı programını diske kaydetmeden bellekte çalıştırıyorsa, sistem belleğinin adli görüntüsünü (düşük seviyeli kopyası) almak, içeriğini analiz etmenin ve saldırı hakkında bilgi edinmenin en iyi yoludur.**
- **Sistem günlükleri: Her istemci ve sunucu bilgisayarı, olup bitenlerle ilgili farklı günlük dosyaları tutar. Günlük dosyaları, sistemde olup bitenler hakkında birçok bilgi sağlar. Saldırgan izlerini temizlemeye çalışsa bile bazı izler kalacaktır.**
- **Ağ günlükleri: Bir ağdan geçen ağ paketlerinin günlükleri, bir saldırının gerçekleşip gerçekleşmediği ve bunun neleri gerektirdiğiyle ilgili daha fazla soruyu yanıtlamaya yardımcı olur.**

  ### Olay Müdahalesi 

 **Bir olay genellikle bir veri ihlali veya siber saldırı anlamına gelir; ancak bazı durumlarda yanlış yapılandırma, izinsiz giriş girişimi veya politika ihlali gibi daha az kritik bir durum da olabilir.Siber saldırı örnekleri arasında, bir saldırganın ağımızı veya sistemlerimizi erişilemez hale getirmesi, genel web sitesini tahrif etmesi (değiştirmesi) ve veri ihlali (şirket verilerinin çalınması) yer alır.**

 Bir siber saldırıya nasıl tepki verirsiniz? Olay müdahalesi, böyle bir durumu ele almak için izlenmesi gereken metodolojiyi belirtir.Amaç hasarı azaltmak ve mümkün olan en kısa sürede iyileşmektir. İdeal olarak, olaya müdahaleye hazır bir plan geliştirirsiniz.

 **Olay müdahale sürecinin dört ana aşaması şunlardır:**

 - **Hazırlık:** Bu, eğitimli ve olayları ele almaya hazır bir ekip gerektirir. İdeal olarak, olayların yaşanmasını önlemek için çeşitli önlemler alınır.
 - **Tespit ve Analiz:** Ekip herhangi bir olayı tespit etmek için gerekli kaynaklara sahiptir; ayrıca, tespit edilen herhangi bir olayın ciddiyetini öğrenmek için daha fazla analiz edilmesi önemlidir.
 - **Sınırlama, Ortadan Kaldırma ve Kurtarma:** Bir olay tespit edildiğinde, olayın diğer sistemleri etkilemesinin durdurulması, ortadan kaldırılması ve etkilenen sistemlerin kurtarılması çok önemlidir.Örneğin, bir sisteme virüs bulaştığını fark ettiğimizde, virüsün diğer sistemlere yayılmasını durdurmak (kontrol altına almak), virüsü temizlemek (ortadan kaldırmak) ve sistemin uygun şekilde kurtarılmasını sağlamak isteriz.
 - **Olay Sonrası Faaliyet:** Başarılı bir iyileşmenin ardından bir rapor hazırlanır ve gelecekte benzer olayların önlenmesi için öğrenilen ders paylaşılır.

### Kötü Amaçlı Yazılım Analizi

**Kötü amaçlı yazılım, kötü amaçlı yazılım anlamına gelir. Yazılım, bir diske kaydedebileceğiniz veya ağ üzerinden gönderebileceğiniz programları, belgeleri ve dosyaları ifade eder. Kötü amaçlı yazılımlar aşağıdakiler gibi birçok türü içerir:**

- Virüs, kendisini bir programa ekleyen bir kod parçasıdır (bir programın parçası). Bir bilgisayardan diğerine yayılmak üzere tasarlanmıştır; dahası, bilgisayara bulaştığında dosyaları değiştirerek, üzerine yazarak ve silerek çalışır.Sonuç, bilgisayarın yavaşlamasından kullanılamaz hale gelmesine kadar değişir.
- Truva Atı, istenen bir işlevi gösteren ancak altında kötü amaçlı bir işlevi gizleyen bir programdır. Örneğin, bir kurban, şüpheli bir web sitesinden, saldırgana sistemi üzerinde tam kontrol sağlayan bir video oynatıcı indirebilir.
- Fidye yazılımı, kullanıcının dosyalarını şifreleyen kötü amaçlı bir programdır. Şifreleme, şifreleme parolasını bilmeden dosyaları okunamaz hale getirir. Saldırgan, kullanıcının bir "fidye" ödemeye razı olması durumunda kullanıcıya şifreleme şifresini sunar.

### Kötü amaçlı yazılım analizi, çeşitli yöntemler kullanarak bu tür kötü amaçlı programlar hakkında bilgi edinmeyi amaçlar:

1. Statik analiz, kötü amaçlı programı çalıştırmadan inceleyerek çalışır. Genellikle bu, montaj dili (işlemcinin komut seti, yani bilgisayarın temel talimatları) hakkında sağlam bilgi gerektirir.
2. Dinamik analiz, kötü amaçlı yazılımı kontrollü bir ortamda çalıştırarak ve faaliyetlerini izleyerek çalışır. Kötü amaçlı yazılımın çalışırken nasıl davrandığını gözlemlemenizi sağlar.

![image](https://github.com/user-attachments/assets/41a32792-c6ff-42b4-80a5-3c3f38d7114f)



## Bir güvenlik analisti olarak yapacağınız tipik bir görev ne olurdu?
**Bayrağı alana kadar devam etmek için “Siteyi Görüntüle”ye tıklayın. (İlk kez bayrak alıyorsanız, bayrak, bir görevi tamamladığınızda aldığınız bir metin dizisi olarak görülebilir. Örnek bayrak FLAG{WORDS_AND_MORE}'dur.)**

![image](https://github.com/user-attachments/assets/11a9b4c0-7f19-44f3-be50-6c8afa446abf)


Bir bankanın korunmasından sorumlu Güvenlik Operasyon Merkezinin (SOC) bir parçasısınız. Bu bankanın SOC'si Güvenlik Bilgileri ve Olay Yönetimi (SIEM) sistemini kullanıyor.SIEM, çeşitli kaynaklardan güvenlikle ilgili bilgi ve olayları toplar ve bunları tek bir sistem üzerinden sunar.

Örneğin, başarısız bir oturum açma denemesi veya beklenmedik bir coğrafi konumdan oturum açma girişimi olması durumunda size bilgi verilir.

Dahası, makine öğreniminin gelişmesiyle birlikte SIEM, bir kullanıcının genellikle yalnızca çalışma saatlerinde oturum açtığı halde sabah saat 3'te oturum açması gibi olağandışı davranışları tespit edebilir.

**Bu alıştırmada, ağımızdaki ve sistemlerimizdeki farklı olayları gerçek zamanlı olarak izlemek için bir SIEM ile etkileşime gireceğiz.Bazı olaylar tipik ve zararsızdır; diğerleri bizden daha fazla müdahale gerektirebilir.Kırmızı işaretli olayı bulun, not edin ve daha fazla inceleme için üzerine tıklayın.**

![image](https://github.com/user-attachments/assets/ca94e2bb-4e53-4d02-99bf-d01b07e8a7f1)


**Daha sonra şüpheli etkinlik veya olay hakkında daha fazla bilgi edinmek istiyoruz. Şüpheli olay, yerel kullanıcı, yerel bilgisayar veya uzak IP adresi gibi bir olay tarafından tetiklenmiş olabilir.Posta göndermek ve almak için fiziksel bir adrese ihtiyacınız vardır; benzer şekilde, İnternet üzerinden veri gönderip almak için de bir IP adresine ihtiyacınız vardır.Olayın gerçekten kötü niyetli olup olmadığını doğrulamak için tetikleyicinin nedenini inceliyoruz**

![image](https://github.com/user-attachments/assets/c81aac94-54ec-4e6a-bfbc-a183c8fb35a2)


**Kötü amaçlıysa, SOC'deki başka birine bildirimde bulunmak ve IP adresini engellemek gibi gerekli önlemleri almamız gerekir.**

![image](https://github.com/user-attachments/assets/e3547939-aad5-4875-b83d-b97a7a90711d)


![image](https://github.com/user-attachments/assets/95341fff-3632-46c2-a4a3-d47b92efef69)


![image](https://github.com/user-attachments/assets/a7bfd146-d3ce-4582-b655-653e31fd4ac4)







