👋 1- Class Yapısına Dair Son Dokunuşlar

Class içinde tanımlanan class, sınıf elemanı mıdır?
Nested type dediğimiz iç içe tanımlanan classlarda içerdeki class, dışardaki classın elemanı olmuyor.
Bir classın elemanlarına classın nesnesi üzzerinden erişebiliyorum. Haliyle içerde tanımlanmış olan classa da erişebilmem gerekirdi ama erişemiyorum. Çünkü sınıfın elemanı değil.

👉 ! Sınıfın elemanlarına nesne üzerinden erişilir.

 ![4-1](https://github.com/user-attachments/assets/44c06077-737a-4e20-a7d5-af26f3b88311)

MyClass2 ye erişebilmem için MyClassın referansı ile gitmen gerek. Ben nasıl MyClass türünde bir nesne oluşturabilmem için MyClass türünü yazmam gerekiyorsa, MyClass2 türünde nesne oluşturabilmem için MyClass.MyClass2 demem gerekir. Çünkü MyClass2, MyClass içinde. 

👉 ! 

![4-2](https://github.com/user-attachments/assets/ffecf7df-5ce2-47fc-8922-b27998ede009)

MyClass.MyClass2...ahmet şeklinde olsaydı,, bunun türü ahmet olacaktı, en sonda neye gittiyse tür odur.

👋 2 - Class Elemanlarına Açıklama Satırı Nasıl Eklenir?

![4-3](https://github.com/user-attachments/assets/09857af5-c560-46f4-af78-a7632dc55728)

Şimdi bir sınıfın üstüne geldiğimiz zaman açıklasını altında görüyoruz, bizim oluşturduğumuz sınıfın üstüne gelirsek açıklama yok, bunu nasıl yapacağımızı öğreneceğiz.

![4-4-](https://github.com/user-attachments/assets/2a482b61-14bb-48fd-8467-1fe7e07d3618)

Aynı şekilde nesnenin memberlarına(sınıfın fieldlarına) açıklama ekleyeceğiz. Overloadlarını, aldıkları parametreleri görebileceğiz.

Açıklama ekleyeceğimiz yapının başına gelip /// koyarsan IDE bu yapılanmayı getirerek;
/// <summary>
/// Bu, Deneme1 classı için bir açıklamadır.
/// </summary>

![4-5](https://github.com/user-attachments/assets/181573f4-ba94-45c0-9821-a61025480b9e)
![4-6](https://github.com/user-attachments/assets/b95fc578-8364-47ca-a289-137c32d22c4b)

![4-7](https://github.com/user-attachments/assets/46e6049b-c999-46ae-b9ea-fe87072f4803)

Parametreleri yakalıyor.

![4-8](https://github.com/user-attachments/assets/2c09fc13-258c-4932-a9f5-b1a9bcd73685)

Parametre açıklamasını da girdik.
Bu açıklama satırlarını ne amaçla kullanırız? Kendi yazdığımız kodlara daha sonra dönüp baktığımızda kolayca anlayabilmek için kullanırız.
