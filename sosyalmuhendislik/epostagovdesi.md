### E-posta gövdesi, e-postanın, gönderenin görüntülemenizi istediği metni (düz veya HTML biçimli) içeren kısmıdır.  Aşağıda salt metinden oluşan bir e-posta örneği verilmiştir.

![image](https://github.com/user-attachments/assets/4c60e505-dedf-484a-9f1b-c0a15763280c)

### Aşağıda HTML biçimli e-postanın bir örneği verilmiştir.

![image](https://github.com/user-attachments/assets/c262d5a0-d590-4819-a29b-9b0a86c51485)

Bir e-postanın HTML kodunu görüntülemek için aşağıda gösterilen yaklaşımla aynıdır ancak web posta istemcisine bağlı olarak değişiklik gösterebilir.  Aşağıdaki örnekte ekran görüntüsü Protonmail'den alınmıştır.

![image](https://github.com/user-attachments/assets/8f6f88d9-debc-4953-afc6-64c9e9cb8ea7)

HTML kodunun bir pasajı aşağıda gösterilmektedir.

![image](https://github.com/user-attachments/assets/16895548-b9b2-4b45-a19f-2c8b22d9315a)

Bu özel e-posta web istemcisi Protonmail'de, HTML'ye geri dönme seçeneğine "Oluşturulan HTML'yi görüntüle" adı verilir.

![image](https://github.com/user-attachments/assets/e91188da-3f65-4992-9c73-5ccbf026e05e)

Yine diğer web posta istemcileri için durum farklı olacaktır. Son olarak, e-postalar ekler içerebilir. Aynı öncül geçerlidir; bir e-postanın ekini bir e-postanın HTML biçiminden veya kaynak kodunu görüntüleyerek görüntüleyebilirsiniz.
Aşağıda birkaç örneğe bakalım. Aşağıdaki örnek, "Netflix"ten gelen ve ek içeren HTML biçimli bir e-postadır. Web istemcisi Yahoo!

![image](https://github.com/user-attachments/assets/1ffd8ccc-ba32-4558-8c89-b964cadfbe9b)

1-E-posta gövdesinde bir resim bulunur. 

2-E-posta eki bir PDF belgesidir.

Şimdi bu eki kaynak kodunda görüntüleyelim.

![image](https://github.com/user-attachments/assets/33586289-3cb0-4301-b9a6-2495f3162cfb)

Yukarıdaki örnekte bu ekle ilişkili başlıkları görebiliriz:

* **İçerik Türü(Content-type)** **uygulama/pdf**'tir.
* **Content-Disposition** bunun bir ek olduğunu belirtir.
* **Content-Transfer-Encoding** bize bunun base64 ile kodlandığını söyler.

Base64 kodlu verilerle kodunu çözebilir ve makinenize kaydedebilirsiniz. 

### Uyarı: Eklerle etkileşimde bulunurken dikkatli olun ve e-postanın ekine kazara çift tıklamadığınızdan emin olun.


  







