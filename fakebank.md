## Bu görevi masaüstünde ilk açtığınızda, ekranınız otomatik olarak görevin sanal makinesini başlatacak ve bölünmüş ekranda görüntüleyecektir. 
**Bunu FakeBank adlı sahte bir banka uygulamasını hacklemek için kullanacaksınız.Ayrıca bir mobil cihazdan dağıtmak için Makineyi Başlat düğmesine de tıklayabilirsiniz. 
Ekranınız bölünmüyorsa bu sayfanın sol üst kısmındaki mavi Bölünmüş Görünümü Göster düğmesini kullanın.**
![image](https://github.com/user-attachments/assets/cbeaf080-96e8-497e-b73f-5e5348647bcc)

**Gizli dizinleri ve sayfaları bulmak amacıyla FakeBank'ın web sitesine kaba kuvvet uygulamak için "GoBuster" adlı bir komut satırı uygulamasını kullanacağız.
GoBuster potansiyel sayfa veya dizin adlarının bir listesini alacak ve bunların her biriyle bir web sitesine erişmeyi deneyecektir; sayfa varsa size söyler.**
### Adım 1) Bir terminal açın
**Komut satırı olarak da bilinen terminal, grafiksel kullanıcı arayüzü kullanmadan bilgisayarla etkileşim kurmamıza olanak tanır. 
Makinede Terminal simgesini kullanarak terminali açın:**: ![image](https://github.com/user-attachments/assets/69aa6417-79d6-40d8-b590-361994294028)
### Adım 2) Gizli web sitesi sayfalarını bulun
**Çoğu şirket, çalışanlarına günlük operasyonlar için temel yönetici kontrollerine erişim sağlayan bir yönetici portalı sayfasına sahip olacaktır.
Bir bankada, bir çalışanın müşteri hesaplarına ve müşteri hesaplarından para transferi yapması gerekebilir.Çoğu zaman bu sayfalar özel hale getirilmez ve 
saldırganların yönetici kontrollerini veya hassas verileri gösteren veya bunlara erişim sağlayan gizli sayfaları bulmasına olanak tanır.
GoBuster'ı (bir komut satırı güvenlik uygulaması) kullanarak FakeBank'ın web sitesinde potansiyel olarak gizli sayfaları bulmak için terminale aşağıdaki komutu yazın.**

![image](https://github.com/user-attachments/assets/10c8f45f-8932-4905-8b23-f31f823acf7c)

**Komut çalışacak ve size buna benzer bir çıktı gösterecektir:**
![image](https://github.com/user-attachments/assets/6794bda0-447f-4015-8d69-954e874b36bb)

**Yukarıdaki komutta, -u taradığımız web sitesini belirtmek için kullanılır, -w gizli sayfaları bulmak için yinelenecek kelimelerin listesini alır.
GoBuster'ın listedeki her kelimeyle web sitesini taradığını ve sitede bulunan sayfaları bulduğunu göreceksiniz. 
GoBuster, sayfa/dizin adları listesinde (Durum: 200 ile gösterilir) bulduğu sayfaları size bildirecektir.**

![image](https://github.com/user-attachments/assets/cf65d13d-72b6-4a71-a4f8-2ea4b7194c53)

### Adım 3) Bankayı Hackleyin
**Bankadaki hesaplar arasında para transferi yapmanızı sağlayan (/bank-transfer) gizli bir banka havalesi sayfası bulmuş olmalısınız. 
Gizli sayfayı makinedeki FakeBank web sitesine yazın.**

![image](https://github.com/user-attachments/assets/3aa69214-7645-48f2-a590-fa2b203bff82)

**Bu sayfa, bir saldırganın herhangi bir banka hesabından para çalmasına olanak tanır ve bu, banka için kritik bir risktir.
Etik bir bilgisayar korsanı olarak, (izin alarak) uygulamalarındaki güvenlik açıklarını bulursunuz 
ve bunları, bir bilgisayar korsanı bunları kullanmadan önce düzeltilmesi için bankaya bildirirsiniz.**

**2276 numaralı banka hesabından kendi hesabınıza (8881 numaralı hesap) 2000$ aktarın.**

![image](https://github.com/user-attachments/assets/0c839ea8-a943-4638-b3ee-705a1b0d3253)

**Transferiniz başarılı olduysa artık yeni bakiyenizin hesap sayfanıza yansıdığını görebilmeniz gerekir.
Şimdi oraya gidin ve parayı aldığınızı onaylayın! (Değişikliklerin görünmesi için Yenile'ye basmanız gerekebilir)**

![image](https://github.com/user-attachments/assets/96ac85d1-2ff5-43ce-9d81-09416855b21c)

**Artık hesap bakiyenizin üstünde bu sorunun cevabını belirten bir mesaj görmelisiniz. İhtiyacınız olan cevabı bulabilir misiniz?
Buradaki sorunun doğru cevabı banka sayfanızı yeniledikten sonra ortaya çıkan tebrik mesajı olacaktır.**
![image](https://github.com/user-attachments/assets/af0e2d3a-4af9-4b74-91f5-2cd911265b2a)


![image](https://github.com/user-attachments/assets/2b092cbb-7531-4f03-975a-da124d3578d0)

**Son aşama olarak sayfanın üst kısmındaki kırmızı "Sonlandır" düğmesini tıklayarak makineyi sonlandırın.**

# TEBRİKLER









