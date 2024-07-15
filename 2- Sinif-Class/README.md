👋 1- Class Kavramı
OOP'de temel esas yapılanma nesnesidir. Nesne fırat olarak bir classtır, yani classtan üretilebilir bir yapılanmadır.
foto1 - 

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
foto2
Classlarda, nesnelerdeki ortak alan tanımlamaları yapılır .Örnekteki field ve metot, bütün nesnelerde ortak olacaktır. Ama değerleri farklı olabilir. Hepsinin adı, niteliği/özelliği vardır ama bu özellik farklı değerlere sahiptir. Class tekildir, 1 tane tanımlarsın. Yani bir projede birden fazla class tanımlayabilirsin ama sadece bir modele ait classsı bir kere tanımlarsın. Yani 1 nesnenin modeli 1 classta olur. Nesne o classtan/o modelden çoğul olarak türer. Aralarında bire çok ilişki vardır. 
Sınıf elemanlarına şimdilik member diyelim. 

👋 5 - Sınıf Nasıl ve Nerede Oluşturulur? 
Class keywordü ile class oluşturabiliriz. foto2 - Ben bir classa yani nesne oluşturabilir bir yapılanma oluşturdum. Nesne rame yerleştirilirken türünü de belirtmem gerekiyor. Haliyle classın türü ne ise nesnenin türü de o olur. Nesneyi, onun türünden  bir referansla stackte işaretleyebiliyorum. 

👉 ! Yani nesnenin tüür ile onu işaretlediğim referansın türü aynı olamlıdır. 

👉 ! OOP' de oluşturulan class bizim için bir türdür, referans türüdür. 

👉 ! Namespace Nedir? 
İçinde birden fazla class, struct, interface gibi yapılanmaları barındıran, senin kütüphane mantığını oluşturmanı sağlayan, genel anlamda kurmuş olduğun sistemde sınıfların farklı namespaceler altında kategorize edip çağırma esnasında o kategorizeler üzerinden çağırmanı sağlayan yapılanmadır. 

Sınıf 3 farklı yerde oluşturulur:
 1- Namespace içinde - foto3
 2- Namespace dışında- foto4
 3- Namespaceden bağımsız class içinde(nested type - yani iç içe classlar) - foto5 
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

👉 ! Class içinde oluşturulan değişkenlere field denir. Normalde class içindeki elemanlara erişirken this keywordü kullanılır. foto6 

👋 7 - Sınıf Modelinden Referans Noktası Oluşturma
foto7
Ramde 2 bölge var dedik. Stack ve heap. Heapte nesneler tutuluyor. Stacke direk erişebiliyorum. Developer olarak heap e erişemiyorum. Dolayısıyla benim heapteki nesneyi kullanabilmem için yapmam gereken heape erişebilen bir aracı kullanmaktır. İşte bu araçlar da stackteki referanslardır. Referanslar stackte tutulan ve heapteki herhangi bir nesneyi işaretleyebilme özelliğine sahiptir. Biz bu türe(referanslara) referans türlü değişken diyoruz. 

👉 ! Bir class tanımlandığında o class adı bir türdür. Haliyle o türü kullanabilmek için direkt olarak o class adını kullanmak yeterlidir. 
foto8 - Burada OrnekModel bir classtır ve referans noktası oluşturmak için OrnekModel w; demen yeterlidir. Senin bunu değişken türü gibi kullanabilmenin altında bunun bir referans türlü değişken olması yatar. 
👉 ! Ramde foto9 - referans noktası alma vs, bir classın türünden bir değişken oluşturuyorum. Şuan da herhangi bir şeyi referans etmiyor. Herhangi bir nesneyi referans etmediği için w, null değere sahiptir. Bir değişkenin null değere sahip olması için onun nullable olması gereklidir ve referans türlü değişkenler özünde nullabledir. 





















👉 !
