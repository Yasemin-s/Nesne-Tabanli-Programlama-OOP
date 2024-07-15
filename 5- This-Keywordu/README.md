👋 1- This Keywordü Nedir? İşlevleri Nelerdir?

Nesne modellerini oluşturmamızı sağlayan class yapıları içinde kullanılan this keywordünü inceleyeceğiz. 
This keywordü C# da üç farklı amaca hizmet eder.
 1- Sınıfın nesnesini temsil eder.
 2- Aynı isimde field ile metot parametrelerini ayırmak için kullanılır.
 3- Bir constructordann başka bir constructorı çağırmak için kullanılır.

 1- Sınıfın nesnesini temsil ettiği durumlar
This, her yerde çağırılmaz. Sadece memberların içinde çağırılır. Property, metot, indexer, constructor, deconstructor içinde çağırılabilir.
Foto1- MyClasstan üreteceğin nesneyi this ile burada temsil edebiliyorsun. İlgili sınıftan birden fazla nesne üretebilir ve her bir nesne için this keywordünü kullanabiliriz. Bu this,, oluşturulan herhangi bir nesneyi temsil etmez, oluşturduğun nesneyi temsil eder. This ilgili nesneleri temsil eder de diyebiliriz. 
foto2- X in içinde kullanılan this, m1 nesnesini temsil eder. Aynı zamanda this. diyerek ilgili nesnenin memberlarına da erişebilirim. 

👉 ! Sınıf içinde this keywordü gördüğünde, o classtan o anda üretilmiş olan nesne neyse o nesneyi temsil eder.

 2- Aynı isimde field ile metot parametrelerini ayırmak için kullanılan durumlar
Aslında bu 2. özellik, 1. özellikten gelmektedir.
Foto3- This.a ile nesnenin a fieldına eriştik. Eğer this kullanmadan sadece a deseydim, metodun parametresindeki a ya erişmiş olacaktım. 
Foto4- Burada this kullanmak zorunda değilsin. Compiler arka taraffta thisi kullanıyor zaten. Yani, field ve metot parametresi aynı ise this kullanman gerekir o ayrımı yapabilmen için, onun haricinde this kullanmana gerek yok.

 3- Bir constructordan başka bir constructorı çağırmak için kullanılan durumlar
Constructor yapılanmları bir nesnenin oluşum sürecinde ilk tetiklenen fonksiyondur. Bir connstructordan başka bir constructorı çağırmak için kullanılır. yani burada bir sınıfı inşa ederken farklı constructorları tek elden tetiklemeyi sağlayan mimarisel bir manevra getiriyor this keyordü.







