👋 1- Class Yapısına Dair Son Dokunuşlar

Class içinde tanımlanan class, sınıf elemanı mıdır?
Nested type dediğimiz iç içe tanımlanan classlarda içerdeki class, dışardaki classın elemanı olmuyor.
Bir classın elemanlarına classın nesnesi üzzerinden erişebiliyorum. Haliyle içerde tanımlanmış olan classa da erişebilmem gerekirdi ama erişemiyorum. Çünkü sınıfın elemanı değil.

👉 ! Sınıfın elemanlarına nesne üzerinden erişilir.

Foto1- Foto1 deki MyClass2 ye erişebilmem için MyClassın referansı ile gitmen gerek. Ben nasıl MyClass türünde bir nesne oluşturabilmem için MyClass türünü yazmam gerekiyorsa, MyClass2 türünde nesne oluşturabilmem için MyClass.MyClass2 demem gerekir. Çünkü MyClass2, MyClass içinde. 

👉 ! Foto2- MyClass.MyClass2...ahmet şeklinde olsaydı,, bunun türü ahmet olacaktı, en sonda neye gittiyse tür odur.

👋 1- Class Elemanlarına Açıklama Satırı Nasıl Eklenir?

Foto3- Şimdi bir sınıfın üstüne geldiğimiz zaman açıklasını altında görüyoruz, bizim oluşturduğumuz sınıfın üstüne gelirsek açıklama yok, bunu nasıl yapacağımızı öğreneceğiz.

Foto4- Aynı şekilde nesnenin memberlarına(sınıfın fieldlarına) açıklama ekleyeceğiz. Overloadlarını, aldıkları parametreleri görebileceğiz.

Açıklama ekleyeceğimiz yapının başına gelip /// koyarsan IDE bu yapılanmayı getirerek;
/// <summary>
/// Bu, Deneme1 classı için bir açıklamadır.
/// </summary>

Foto5-6 
Foto7- Parametreleri yakalıyor.
Foto8- Parametre açıklamasını da girdik.
Bu açıklama satırlarını ne amaçla kullanırız? Kendi yazdığımız kodlara daha sonra dönüp baktığımızda kolayca anlayabilmek için kullanırız.


















