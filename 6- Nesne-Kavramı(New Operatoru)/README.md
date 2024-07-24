👋 1 -  Nesne Kavramı Nedir? Nesne Nasıl Oluşturulur? New Operatörü

Nesne tabanlı programalamada çoğu kayynak encapsulation, abstraction, polimorfizm, kalıtımdan bahseder ve bu kavramlar nesnenin etrafında dönüyor.
Nesne nedir?,
Neden nesne kullanıyoruz?,
Sınıftan nesne nasıl olıuşturuyoruz?,
Bir sınıftan nesne oluşturup onu ram e nasıl alıyoruz? bunları konuşacağız.
Heape konulmuş nesnenin daha sonra stackteki herhangi bir referansla nesnenin nasıl işaretlendiği ve referansla arasında ilişkinin nasıl olduğu anlatılacaktır.

 ✨ Nesne Nedir? Ne Amaçla Kullanılır? ✨
 
Nesne dediğimiz yapılanma canlı bir organizmadır. İçinde birden fazla anlamlı birbiriyle ilişkisel veriler tutan ve sadece bunları tutmakla yetinmeyen bu veriler üstüde işlemler yapıp sonuçlar üretebilen fonksiyonellikler barındıran bir yapılanma/bir organizmadır.
Nesne dediğimiz yapılanma, ben yase olarak nesneyim. Adım soyadım göz rengim vs bunlar nesnenin/yase nin bir parçasıdır. Beni ben yapan değerlerdir. Beni ben yapan bütün değerler bir araya geldiğinde nesne ortaya çıkar. Haliyle o nesne o olguya dair verileri tutan ve o veriler üzerinde işlem yapılmasını sağlayan bir organizmadır. 
Prosedürel programlamada bir olguya dair verileri temsil edebilmek için kullandığımız değişkenler diziler vs bu olgular bir yerden sonra çoğaldığında oradaki kodun yönetimi ne kadar zorlaşıyorsa biz bu olguların bir tanesini classla modelliyoruz. Bu classlar neticesinde o olguya dair bütün alanları field dediğimiz yapıları, bundan üretilen nesnenin fieldlarına gerekli değerleri koyuyorz ve bu fieldlar üzerinde işlemler yapmamızı sağlayan metotlar, propertyler, indexerlar kullanıyoruz. 

👉 ! Nesne dediğimiz yapılanma class yapılanmalarından üretilen verilerdir. Yani nesne de bir veridir. Ben yase olarak, adım soyadım uzunluğum vs bunlar birer veridir. Ama ben yase olarak bir nesneyim. Yani nesnelerde bir veridir daha üstün daha kompleks bir veridir.

👉 ! Nesneler kompleks veri olarak geçer. Ne string ne int ne chardır. Bunların hepsini barındırabilen bir yapıdır. Nesne, bir olgunun karşılığıdır.

👉 ! Nesneler kompleks değerlerdir haliyle nesneleri ifade etmemizi sağlayan classlarda kompleks typelardır. 

✨ Nesne Neden Kullanılır? ✨

Kodu daha hızlı geliştirebilmek, daha sistematik yönetilebilr hale getirmek için nesne kullanılır.

👉 ! Nesne oluşturmak için, classtan başka seçenek yoktur. İnterfaceden abstractan nesne oluşmaz. Struct yyapısından nesne oluşturduğunu zannedersin ama nesne oluşmaz. Recard dediğimiz yapılardan nesne oluşur ama davranışı değişir.

👉 ! Recard da aslında class yapılanmasıdır. 

👉 ! Nesne = Class yapılanmasıdır.

 ✨ Bir sınıftan nesne nasıl oluşturulur/üretilir? ✨

![6-1](https://github.com/user-attachments/assets/ed98c6b1-7df0-4baf-9d2c-5cf3e8171af0)
 
Sınıftan, ram in heap bölgesinde tutulacak nesne nasıl oluşturulur. 

👉 ! Semantik açıdan new operatorü ile nesne oluşturuyorsun. 

new Type(); type kısmı hangi sınıftan hangi türdense onu belirttiğin yerdir. Sonuç olarak sınıfta bir türdür. Burada () kullanımı da bir metottur, ilerde buna constructor diyeceğiz.

![6-2](https://github.com/user-attachments/assets/6ce0b41b-fa75-441d-a7ec-57fbb04dce93)

![6-3](https://github.com/user-attachments/assets/95254c5b-32e0-4cdf-9429-4836623ace27)

(oluşturulan nesneler heapte tutulur.)

Heapte olan nesneye direkt erişemiyoruz. Bunun için referansa ihtiyacım var. Görselde de görüldüğü heapte tutulan nesne type türünde olduğu için referansın türü de type olmalıdır. Oluşturduğum nesne ahmet türündeyse referans da ahmet türünde olmalıdır. 

![6-5](https://github.com/user-attachments/assets/020e7739-ccf5-4820-a5ad-02b67e2499b2)

Burada x, oluşturduğum referanstır. Bu işlem sonucunda, stackte type türünde bir x oluşturuldu ve heapteki nesneyi referans etti.

Normalde int a = 5 deki = oepratorü, atama/assign operatorüdür. Ama Type x = new Type() daki = operatorü artık atama değil, işaretleme/referans etme operatorü olarak adlandırılır. Yani = operatorü değer türlü değişkenlerde atama/assign görevi referans türlü değişkenlerde referans etme/işaretleme görevi görür.

✨ Referanssız Nesnelere Ne Oluyor? Ne İşe Yarıyor? ✨

Oluşturulan nesne illa bir referansla işaretlenmek zorunda değil. 
C# 9.0 da target typed new expressions özelliği, nesne oluşum sürecinde, oluşturulacak olan nesne eğer ki direkt bir referansa atılıyorsa eğer burada hangi nesnenin oluşturukluğu referans sayesinde bilinmektedir. Dolayısıyla ilgili nesnenin oluşturulması için,
Type x = new Type() semantiğinden ziyade,
Type x = new() kullanımı ile oluşturulabilir. Bu kullanımda new ile nesne oluşturulurken oluşacak nesnenin türü referansın türünden alınmaktadır.

👉 ! C# 9.0 özelliğini kullanabilmek için kullandığın çalışma en az .Net 5.0 versiyonu olmalıdır. Yoksa hata verir.









