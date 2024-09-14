![image](https://github.com/user-attachments/assets/df3a58d9-7ccc-4385-92e4-e1dcbc9e0e2a)


### "Linux'un Temelleri" serisinin ilk bölümüne hoş geldiniz. Büyük olasılıkla bir Windows veya Mac makinesi kullanıyorsunuz; her ikisinin de görsel tasarımı ve çalışma şekli farklıdır.Tıpkı Windows, iOS ve MacOS gibi Linux da akıllı arabalara, android cihazlara, süper bilgisayarlara, ev aletlerine, kurumsal sunuculara ve daha fazlasına güç veren, dünyadaki en popüler işletim sistemlerinden biridir.
**Linux'un arkasındaki tarihin bir kısmını ele alacağız ve sonunda bir Linux sihirbazı olma yolculuğunuza başlayacağız! Bu yazıda şunlar olacak:**

* **İlk komutlarınızı etkileşimli bir Linux makinesinde tarayıcınızda çalıştırma**
* **Dosya sistemiyle etkileşimde bulunmak için kullanılan bazı temel komutları size öğretmek**
* **Dosyaları nasıl arayabileceğinizi ve kabuk operatörlerini nasıl tanıtabileceğinizi göstermek**

## Linux Nerelerde Kullanılır?
**Linux'un Windows gibi İşletim Sistemlerine (OS'ler) göre yaklaşmanın çok daha korkutucu olduğunu söylemek doğru olur. Her iki varyantın da kendine göre avantaj ve dezavantajları bulunmaktadır.
"Linux" adı aslında UNIX'i (başka bir işletim sistemi) temel alan birden fazla işletim sistemi için kullanılan bir şemsiye terimdir.Linux'un açık kaynaklı olması sayesinde, Linux'un çeşitleri her şekil ve boyutta mevcuttur; 
sistemin kullanım amacına en uygun olanıdır.Örneğin Ubuntu ve Debian, Linux'un daha yaygın dağıtımlarından bazılarıdır çünkü çok genişletilebilirdir.Yani Ubuntu'yu bir sunucu (web siteleri ve web uygulamaları gibi) veya tam teşekküllü bir masaüstü olarak çalıştırabilirsiniz. Bu seri için Ubuntu kullanacağız. Ubuntu Sunucusu yalnızca 512 MB RAM'e sahip sistemlerde çalışabilirLinux aşağıdaki gibi şeylere güç verir:**

* **Ziyaret ettiğiniz web siteleri**
* **Araç eğlencesi/kontrol panelleri**
* **Mağazalardaki kasalar ve kasalar gibi Satış Noktası (PoS) sistemleri**
* **Trafik ışığı kontrolörleri veya endüstriyel sensörler gibi kritik altyapılar**
**Windows'un farklı sürümlerine (7, 8 ve 10) sahip olduğunuza benzer şekilde, Linux'un da birçok farklı sürümü/dağıtımı vardır.**
  
### İlk Linux Makinenizle Etkileşim Kurma (Tarayıcı İçi)
**Bu odada, bu odanın materyallerini takip ederken tarayıcınız aracılığıyla etkileşimde bulunabileceğiniz bir Ubuntu Linux makinesi bulunmaktadır.Konuşlandırıldıktan sonra odanın üst kısmında bir kart görünecektir:**

![image](https://github.com/user-attachments/assets/7045993a-af5e-42e0-aa26-70fa068acda6)


**Bu, makineyi yönetmeye yönelik düğmelerle birlikte, IP adresi ve süre sonu zamanlayıcısı da dahil olmak üzere, odada dağıtılan makineye ilişkin tüm bilgileri içerir.
Şimdilik, bu odayı takip ederken tarayıcınızda kendi Linux makinenizle etkileşime girebileceğiniz "Makineyi Başlat" düğmesine basın:**

![image](https://github.com/user-attachments/assets/eb9aa85d-62fe-452a-af3e-71f36fef8bed)

### İlk Birkaç Komutunuzu Çalıştırma
**"Terminal" tamamen metin tabanlıdır ve ilk başta korkutucudur.Ancak bazı komutları ayrıntılı olarak ele alırsak, bir süre sonra terminali kullanmaya hızla alışırsınız.**

![image](https://github.com/user-attachments/assets/8aee23c9-936b-4c45-914d-d28feac947ee)


**Dosyalara gitmek, içeriklerinin çıktısını almak ve dosya oluşturmak gibi temel işlevleri yapabilmemiz gerekiyor! Bunu yapmak için gereken komutlar açıklayıcıdır (tabii ki ne olduklarını öğrendikten sonra...)**
**Aşağıdaki tabloda listelediğim ilk komutlardan ikisiyle başlayalım:**

![image](https://github.com/user-attachments/assets/d8b9ecf8-8dae-45d2-9e3a-cfd004b7827f)

* **echo :** Sağladığımız herhangi bir metnin çıktısını alın.

![image](https://github.com/user-attachments/assets/47cee3e3-d6a0-49e0-a373-33c46b6a9af4)

* **whoami:** Şu anda hangi kullanıcı olarak oturum açtığımızı öğrenin!

  ![image](https://github.com/user-attachments/assets/d5f5d5ea-99b6-4fbb-b5fd-2474e42991b6)

**Şu ana kadar sadece "echo" ve "whoami" komutlarını ele aldık. Dosya sisteminde gezinmek, okumak ve yazmak da dahil olmak üzere yapmamız gereken şeyleri düşündüğünüzde pek de kullanışlı değil.**
**Bu görevde, bunu yapabilmemiz için komutları öğreneceğiz. Tıpkı bir önceki görevde olduğu gibi, bir sonraki başlıkta da tabloda yer alan komutları göstereceğim ve bu komutların kullanılan örneklerini göstereceğim.**

### Dosya Sistemiyle Etkileşim
**Daha önce de belirttiğim gibi, oturum açtığınız makinede masaüstü ortamına bağlı kalmadan gezinebilmek oldukça önemli. Sonuçta, hiçbir yere gidemeyeceksek giriş yapmanın ne anlamı var?**

![image](https://github.com/user-attachments/assets/39f6d1b0-398f-4889-a785-c75c4830b34c)

**Mevcut Dizinimizdeki Dosyaları Listeleme (ls)**
Herhangi bir dosya veya klasörün içeriğini bulmak gibi bir şey yapmadan önce, ilk etapta neyin var olduğunu bilmemiz gerekir. Bu "ls" komutu kullanılarak yapılabilir (listelemenin kısaltması)


![image](https://github.com/user-attachments/assets/1bf09c29-3663-4801-97e0-c764b07c2cd9)

## Bir dizinin içeriğini, ls'yi ve dizinin adını kullanarak, o dizine gitmek zorunda kalmadan listeleyebilirsiniz. Yani ls Folder1 gibi..

**Mevcut Rehberimizi Değiştirmek (cd)**
Artık hangi klasörlerin mevcut olduğunu bildiğimize göre, o dizine geçmek için "cd" komutunu (dizin değiştirmenin kısaltması) kullanmamız gerekiyor.
Diyelim ki "Folder1" dizinini açmak isteseydim "cd Folder1"i açardım.
Yine bu "Folder1" dizininin içeriğini bulmak istediğimizde, tekrar "ls" kullanırız:

**Bir Dosyanın İçeriğinin Çıktısını Alma (cat)**
Dosyaların varlığını bilmek harika olsa da, bunların içeriğini görüntüleyemediğimiz sürece o kadar da yararlı değildir."Cat"dosyaların (sadece metin dosyalarının değil!) içeriklerinin çıktısını almamızın harika bir yoludur.
Aşağıdaki ekran görüntüsünde, "Belgeler" adlı bir dizindeki dosyaları listelemek için "ls" kullanımını nasıl birleştirdiğimi görebilirsiniz:

![image](https://github.com/user-attachments/assets/398e6785-d79f-41a2-95e0-ca804b52ffba)

Aşağıdakileri yapmak için bu görevin önceki bölümlerinde edindiğimiz bazı bilgileri uyguladık:

* **Bu makinenin "Belgeler" klasöründe hangi dosyaların bulunduğunu bize bildirmek için "ls" kullanıldı. Bu durumda buna "todo.txt" adı verilir.**
* **Daha sonra bu "todo.txt" dosyasının içeriğini birleştirmek/çıkışlamak için cat todo.txt dosyasını kullandık; burada içerik "İşte benim için daha sonra yapmam gereken önemli bir şey!"**

## cat'i ve dizinin adını kullanarak dosyaya gitmek zorunda kalmadan, dizinler içindeki bir dosyanın içeriğini çıkarmak için cat'i kullanabilirsiniz. Yani cat /home/ubuntu/Documents/todo.txt

**Mevcut Çalışma Dizinimizin Tam Yolunun Bulunması (pwd)**
Linux makinenizde gezinirken, şu anda üzerinde çalışmakta olduğunuz dizinin adının terminalinizde listeleneceğini fark edeceksiniz.Dosya sisteminin tam olarak neresinde olduğumuzun izini kaybetmek kolaydır, bu yüzden "pwd"yi tanıtmak istiyorum. Bu, yazdırma çalışma dizini anlamına gelir.
Önceki örnek makineyi kullanarak şu anda "Belgeler" klasöründeyiz - ancak bu, Linux makinesinin dosya sisteminde tam olarak nerede? Bunu aşağıdaki ekran görüntüsündeki gibi "pwd" komutunu kullanarak bulabiliriz:

![image](https://github.com/user-attachments/assets/bfab1f15-4a2c-4c88-8b65-723ff5a45a1a)

* **Terminalimiz sayesinde "Belgeler"de olduğumuzu zaten biliyoruz, ancak bu noktada gelecekte kolayca geri dönebilmemiz için "Belgeler"in nerede saklandığına dair hiçbir fikrimiz yok.**
* **Bu "Belgeler" klasörünün tam dosya yolunu bulmak için "pwd" (çalışma dizinini yazdır) komutunu kullandım.**
* **Linux bize bu "Belgeler" dizininin makinedeki "/home/ubuntu/Documents" konumunda saklandığını söyledi**
* **Artık gelecekte kendimizi farklı bir konumda bulursak, çalışma dizinimizi bu "Belgeler" dizinine değiştirmek için cd /home/ubuntu/Documents komutunu kullanabiliriz.**

**Dosyaları Arama**
Neyin nerede olduğunu öğrenmek için sürekli olarak **cd ve ls** kullanmanıza gerek yoktur. Bunun yerine, bunun gibi şeyleri bizim için otomatikleştirmek için **Find** gibi komutları kullanabiliriz!
Find komutu, tam olarak ne yapmak istediğinize bağlı olarak hem çok basit hem de daha karmaşık bir şekilde kullanılabilmesi açısından harikadır. Ancak önce temellere sadık kalalım.

### Basit bir başlangıç ​​yapalım ve aradığımız dosyanın adını zaten bildiğimizi ancak tam olarak nerede olduğunu hatırlayamadığımızı varsayalım! Bu durumda "passwords.txt" dosyasını arıyoruz

![image](https://github.com/user-attachments/assets/525172a3-9c38-4dda-8300-a58b0fed8b8e)

"Bul" dosyayı bulmayı başardı - klasör1/passwords.txt dosyasında olduğu ortaya çıktı,Ancak diyelim ki dosyanın adını bilmiyoruz veya ".txt" gibi uzantısı olan her dosyayı aramak istiyoruz.
Sonunda .txt bulunan herhangi bir şeyi aramak için joker karakter **(*)** olarak bilinen şeyi kullanabiliriz.Bizim durumumuzda geçerli dizinimizde bulunan her .txt dosyasını bulmak istiyoruz. find -name *.txt gibi bir komut oluşturacağız.

![image](https://github.com/user-attachments/assets/aacfa595-6dcb-4224-bc69-231bf754aede)

**Grep'i kullanma**
Grep komutu, aradığımız belirli değerler için dosyaların içeriğinde arama yapmamızı sağlar.Örneğin bir web sunucusunun erişim günlüğünü ele alalım. Bu durumda, bir web sunucusunun erişim günlüğünde 244 giriş bulunur.

![image](https://github.com/user-attachments/assets/945420e4-f2ce-4ed3-baec-25ae170f78ee)

Belirli bir değeri bulmak istediğimizi düşünürsek, 244 girişi incelemek o kadar da verimli değil. Grep'i, bu dosyanın tüm içeriğinde, belirtilen değerin herhangi bir girişini aramak için kullanabiliriz.
Bir web sunucusunun erişim günlüğü örneğine göre, "81.143.211.90" IP adresinin ziyaret ettiği her şeyi görmek istiyoruz (bunun kurgusal olduğunu unutmayın)

![image](https://github.com/user-attachments/assets/91c926a9-952e-4e3c-b135-358e6a688e5b)


"Grep" bu dosyada arama yaptı ve bize IP için sağladığımız ve bu günlük dosyasında yer alan girişleri gösterdi.





















