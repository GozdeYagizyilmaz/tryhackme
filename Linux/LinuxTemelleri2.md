## Shell Operatörlerine Giriş

**Dikkate değer birkaç önemli operatör var. Temelleri ele alacağız ve bunları uygun şekilde küçük parçalara ayıracağız.Genel bakışta aşağıdaki operatörleri göstereceğim:**

![image](https://github.com/user-attachments/assets/8eac4a83-41da-453d-ba5c-555eaa0aff80)

### Operatör "&"
Bu operatör arka planda komutları çalıştırmamızı sağlar. Örneğin büyük bir dosyayı kopyalamak istediğimizi varsayalım.Bu oldukça uzun zaman alacak ve dosya başarılı bir şekilde kopyalanana kadar başka hiçbir şey yapamayacak durumda olacağız.
"&" kabuk operatörü, bir komutu yürütmemize ve onu arka planda çalıştırmamıza izin vererek başka şeyler yapmamıza olanak tanır!

### Operatör "&&"
Bu kabuk operatörü, ortağı "&"nın ne kadar tanıdık olduğu anlamında biraz yanıltıcıdır. "&" operatörünün aksine, çalıştırılacak komutların bir listesini yapmak için "&&" kullanabiliriz, örneğin komut1 && komut2.
Ancak, komut2'nin yalnızca komut1 başarılı olduğunda çalışacağını belirtmekte fayda var.

### Operatör ">"
Bu operatör, çıkış yeniden yönlendiricisi olarak bilinir. Bunun esas anlamı, çalıştırdığımız bir komutun çıktısını alıp bu çıktıyı başka bir yere göndermemizdir.Diyelim ki "hey" mesajını içeren "hoş geldiniz" adında bir dosya oluşturmak istedik. "Hey" içeriğiyle dosyanın oluşturulmasını istediğimiz yerde echo hey > hoş geldiniz komutunu çalıştırabiliriz:

![image](https://github.com/user-attachments/assets/2ab6a9ed-31e6-4339-874c-ab2e62dc62ee)

## Not: "Hoş geldiniz" dosyası zaten mevcutsa içeriğin üzerine yazılacaktır!

### Operatör ">>"
Bu operatör daha önce tartıştığımız operatör (>) gibi bir çıkış yönlendiricisidir.Ancak bu operatörü farklı kılan şey, örneğin bir dosya içindeki herhangi bir içeriğin üzerine yazmak yerine, çıktıyı yalnızca sona koymasıdır.
>> operatörü, içeriği şu şekilde değiştirmek yerine, çıktının dosyanın altına eklenmesine olanak tanır:

![image](https://github.com/user-attachments/assets/fb1220b1-b01a-4082-8ce3-1e8fff260272)


## Linux Temelleri Serisinin ilk bölümü için aşağıdaki linke tıklayın :

[LinuxTemelleri](https://github.com/GozdeYagizyilmaz/tryhackme/blob/main/LinuxTemelleri.md)


