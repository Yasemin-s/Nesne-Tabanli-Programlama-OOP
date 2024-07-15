👋 1- Class Kavramı
OOP'de temel esas yapılanma nesnesidir. Nesne fırat olarak bir classtır, yani classtan üretilebilir bir yapılanmadır.

![2-1](https://github.com/user-attachments/assets/e8e9c931-314b-4f16-b5da-0e7e71494815)


👋 2 - Sınıf Nedir? Neden Sınıf Yapısı Kullanılır? 
Obje/nesne oluşturabilmem için önce yapmam gereken bu nesneyi modellemektir. Modelleme, bir nesnenin önceden tanımlanmış arayüzü demektir.
OOP'de bir object oluşturmak için o objectin modellenmesi/tanımlanması gerekmektedir. Bir objenin/nesnenin tanımının oluşturabilmesi için class yapısı kullanılır.

👋 3 - Neden Class/Sınıf Yapısı Kullanılır? 
Class yapısı kendi içinde field, property, indexer, metotlar olarak ayrılır. 

field: İlgili nesnenin içinde hangi değerlerin tutulacağına dair alan tanımlamamızı sağlayan yapılardır. 

property: Encapsulation yapılanmlarını sağlayabiliyor. Kontrollü erişim için kullanılır.

indexer: Dizilerde veya koleksiyonlarda indexer operatörü ile işlem yapabilmemizi sağlayan belirli/efektif syntax kazandırır. 

metotlar: Operasyonel olark bir objenin içinde fieldlar yada dışarıdan gelen değerleri hangi işlemlere tabi tutacağımızı ayarlarız.

Yani sınıf bizim kodu inşa ettiğimiz yerdir. Artık bu kodu çalıştırmam lazım bu kod işlevselliğini göstersin dediğimde de obje oluşturup bunu objede çalıştırıyoruz. Haliyle class dediğimiz yapılanma, nesne tabanlı programlamanın temelidir. 

👋 4 - Sınıf İle Nesne Arasındaki İlişki Nedir? 
Sen bir class oluşturuyorsun, bu classtan nesne üretilebiliyor. Sınıf, bir nesne mdoelidir. Bu sınıf üzerinden üretilen nesnelerle operasyonel işlemler gerçekleştirebilir. Haliyle sınıf ne nesne arasındaki ilişki bu davranış üzerinden kurulur. 
👉 ! Sınıftan birden fazla nesne oluşturulabilir. Nesneleri, belleği doldurana kadar oluşturabilirsin. 

![2-2](https://github.com/user-attachments/assets/2675ca05-a560-47b5-93e6-432decb6eca5)


Classlarda, nesnelerdeki ortak alan tanımlamaları yapılır .Örnekteki field ve metot, bütün nesnelerde ortak olacaktır. Ama değerleri farklı olabilir. Hepsinin adı, niteliği/özelliği vardır ama bu özellik farklı değerlere sahiptir. Class tekildir, 1 tane tanımlarsın. Yani bir projede birden fazla class tanımlayabilirsin ama sadece bir modele ait classsı bir kere tanımlarsın. Yani 1 nesnenin modeli 1 classta olur. Nesne o classtan/o modelden çoğul olarak türer. Aralarında bire çok ilişki vardır. 
Sınıf elemanlarına şimdilik member diyelim. 

👋 5 - Sınıf Nasıl ve Nerede Oluşturulur? 
Class keywordü ile class oluşturabiliriz. 

![2-2](https://github.com/user-attachments/assets/58cb3c1f-58b8-45bc-9d90-215b5cd00092)

Ben bir classa yani nesne oluşturabilir bir yapılanma oluşturdum. Nesne rame yerleştirilirken türünü de belirtmem gerekiyor. Haliyle classın türü ne ise nesnenin türü de o olur. Nesneyi, onun türünden  bir referansla stackte işaretleyebiliyorum. 

👉 ! Yani nesnenin tüür ile onu işaretlediğim referansın türü aynı olamlıdır. 

👉 ! OOP' de oluşturulan class bizim için bir türdür, referans türüdür. 

👉 ! Namespace Nedir? 
İçinde birden fazla class, struct, interface gibi yapılanmaları barındıran, senin kütüphane mantığını oluşturmanı sağlayan, genel anlamda kurmuş olduğun sistemde sınıfların farklı namespaceler altında kategorize edip çağırma esnasında o kategorizeler üzerinden çağırmanı sağlayan yapılanmadır. 

Sınıf 3 farklı yerde oluşturulur:
 1- Namespace içinde - ![2-3](https://github.com/user-attachments/assets/58fb13a5-2304-4682-88b3-7e3ab61af4c0)

 2- Namespace dışında- ![2-4](https://github.com/user-attachments/assets/405b1c32-0110-4443-93b9-77dc1c09767c)

 3- Namespaceden bağımsız class içinde(nested type - yani iç içe classlar) - ![2-5](https://github.com/user-attachments/assets/30199a03-4459-4716-92dd-52dff7984b32)

👉 ! Dıştaki sınıfa "enclosing class/outer class", içteki classa "nested class/inner class" denir.

Aynı namespace altındaki classlar birbirlerine direk class isimleri ile erişebilirler. Farklı namespace altındaki classlar namespace ismi üzerinden birbirlerine erişebiliyorlar. Ev gibi düşünün, aynı evdeysem sana isminle erişebiliyorum ama farklı evlerdeysek x evinin yasesi diyerek erişiyorum. 

👉 ! Önemli olan kısım, namespace üstünde class tanımlanırsa bu classlara herkes erişebilir ama namespace altında tanımlanan classlara x evinin yasesi şeklinde erişim oluyor. 

👉 ! Bir class tanımlanmasında, tanımlanan yerde(namespace içi/dışı, class içi) aynı isimde birden fazla class tanımlanamaz. 

👋 6 - Sınıf İle Nesne Modeli Nasıl Tasarlanır?
Buradaki soru sınıf ile nasıl nesne modeli oluşturabilirm değil sınıfla nasıl bir nesne modeli tasarlarım? Autocadde evi nasıl tasrlarım kısmını ele alıyoruz ama henüz ev yapmıyoruz. Aynı şekilde burda da nesne oluşturmayacağız nesne modeli tasarlayacağız. 
 
Şimdi nesne modeli tasarlayabilmek için nelere ihtiyacın olabilir?
 1- Bu nesnenin içinde değerler tutmak için fieldlara ihtiyacın olabilir.
 2- Nesnenin içinde operasyonel işlemler gerçekleştirebilmek için fonksiyonlara ihtiyacın olabilir.
Yani iki yapılanma oluşturman gerekecek. 

👉 ! Class içinde oluşturulan değişkenlere field denir. Normalde class içindeki elemanlara erişirken this keywordü kullanılır. ![2-6](https://github.com/user-attachments/assets/47a84109-cb1d-42db-92ae-daec0b016be4)


👋 7 - Sınıf Modelinden Referans Noktası Oluşturma

![2-7](https://github.com/user-attachments/assets/5a9f4a1a-569b-4081-82a4-bcbb68c20aa7)

Ramde 2 bölge var dedik. Stack ve heap. Heapte nesneler tutuluyor. Stacke direk erişebiliyorum. Developer olarak heap e erişemiyorum. Dolayısıyla benim heapteki nesneyi kullanabilmem için yapmam gereken heape erişebilen bir aracı kullanmaktır. İşte bu araçlar da stackteki referanslardır. Referanslar stackte tutulan ve heapteki herhangi bir nesneyi işaretleyebilme özelliğine sahiptir. Biz bu türe(referanslara) referans türlü değişken diyoruz. 

👉 ! Bir class tanımlandığında o class adı bir türdür. Haliyle o türü kullanabilmek için direkt olarak o class adını kullanmak yeterlidir. 

![2-8](https://github.com/user-attachments/assets/69ebfce4-2a83-490a-ac2a-6c3cef8f2245)

Burada OrnekModel bir classtır ve referans noktası oluşturmak için OrnekModel w; demen yeterlidir. Senin bunu değişken türü gibi kullanabilmenin altında bunun bir referans türlü değişken olması yatar. 
👉 ! Ramde 

![2-9](https://github.com/user-attachments/assets/0868c8f8-fd35-4a7f-a6b0-2a30c01fda79)

Referans noktası alma vs, bir classın türünden bir değişken oluşturuyorum. Şuan da herhangi bir şeyi referans etmiyor. Herhangi bir nesneyi referans etmediği için w, null değere sahiptir. Bir değişkenin null değere sahip olması için onun nullable olması gereklidir ve referans türlü değişkenler özünde nullabledir. 





















👉 !
