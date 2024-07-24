👋 1- This Keywordü Nedir? İşlevleri Nelerdir?

Nesne modellerini oluşturmamızı sağlayan class yapıları içinde kullanılan this keywordünü inceleyeceğiz. 
This keywordü C# da üç farklı amaca hizmet eder.

 1- Sınıfın nesnesini temsil eder.
 2- Aynı isimde field ile metot parametrelerini ayırmak için kullanılır.
 3- Bir constructordann başka bir constructorı çağırmak için kullanılır.

 1- Sınıfın nesnesini temsil ettiği durumlar
This, her yerde çağırılmaz. Sadece memberların içinde çağırılır. Property, metot, indexer, constructor, deconstructor içinde çağırılabilir.

![5-1](https://github.com/user-attachments/assets/36e9d8ec-9f9b-445a-8e7c-1234e0ad20a8)

MyClasstan üreteceğin nesneyi this ile burada temsil edebiliyorsun. İlgili sınıftan birden fazla nesne üretebilir ve her bir nesne için this keywordünü kullanabiliriz. Bu this, oluşturulan herhangi bir nesneyi temsil etmez, oluşturduğun nesneyi temsil eder. This ilgili nesneleri temsil eder de diyebiliriz. 

![5-2](https://github.com/user-attachments/assets/cfef9012-50d2-4e05-8e9d-0e1701f60f4d)

X in içinde kullanılan this, m1 nesnesini temsil eder. Aynı zamanda this. diyerek ilgili nesnenin memberlarına da erişebilirim. 

👉 ! Sınıf içinde this keywordü gördüğünde, o classtan o anda üretilmiş olan nesne neyse o nesneyi temsil eder.

 2- Aynı isimde field ile metot parametrelerini ayırmak için kullanılan durumlar
Aslında bu 2. özellik, 1. özellikten gelmektedir.

![5-3](https://github.com/user-attachments/assets/b531d961-a1ea-452d-ac8b-ea0ffc9b993b)

This.a ile nesnenin a fieldına eriştik. Eğer this kullanmadan sadece a deseydim, metodun parametresindeki a ya erişmiş olacaktım. 

![5-4](https://github.com/user-attachments/assets/0ee5edd0-89c8-44e8-86c4-229cfe8415a3)

Burada this kullanmak zorunda değilsin. Compiler arka tarafta thisi kullanıyor zaten. Yani, field ve metot parametresi aynı ise this kullanman gerekir o ayrımı yapabilmen için, onun haricinde this kullanmana gerek yok.

 3- Bir constructordan başka bir constructorı çağırmak için kullanılan durumlar
Constructor yapılanmları bir nesnenin oluşum sürecinde ilk tetiklenen fonksiyondur. Bir constructordan başka bir constructorı çağırmak için kullanılır. Yani burada bir sınıfı inşa ederken farklı constructorları tek elden tetiklemeyi sağlayan mimarisel bir manevra getiriyor this keywordü.
