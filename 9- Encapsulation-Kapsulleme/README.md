👋 1 - Encapsulation - Kapsülleme Nedir ?                                                                        
 Bir veriyi neden kapsülleriz?
Encapsulation, kapsülleme nesnelerimizdeki fieldların kontrollü bir şekilde dışarıya açılmasıdır. Bir başka deyişle, nesnelerimizi başkalarının yanlışç kullanımından korumak için kontrolsüz erişime kapatmaktır. 

Bir nesnenin field değerinin 3 olduğunu düşünün. Dışarıdan biri bu değere ulaşıp bunun da değerini 15 olarak tekrara verirse bu istenmeyen bir durumdur ve bu durumda encapsulation kullanırız. 

Encapsulation her defasında dışarıya çıkan ve dışarıdan gelen değeri her durumda kontrol eder. Böyle bir durumda prop dediğimiz propertyi kullanıyoruz. foto1

  ✨ Encapsulation Nasıl Uygulanır ? ✨

Metot ve property olarak iki şekilde encapsulation uygulanmaktadır. Classın fieldını erişim belirleyicisinden private i kullanarak encapsulation yapabiliriz. (Çocuk para istiyor. Benim cüzdanımı getir sadece ben sana verecem diyorum, ben erişebiliyorum.) Private olarak işaretlemesem bile default olarak privatedır. Burada dış dünyaya açacağım metot türü field türü ile aynı olmalıdır. Değerin okunması için get fonksiyonu oluşturulur. Değer atamak için ise set metodu kullanılır. Foto2, Foto2 deki gibi zahmetli olmasın diye property ile kullanım sağlanmıştır. 

  ✨ Property İle Encapsulation Gerçekleştirmek ✨

Prop, normalde elimizdeki herhangi bir fieldın değerine müdahele edilmeyecekse kendi fieldını oluşturan ve direkt kısa bir property tanımlaması yapan property türüydü. Ama var olan bir fiedlın üzerinde encapsulationı property üzerinden yapacaksan fullproperty dediğimiz propfull tab tab yaparak kullanabilirsin ve artık kendi oluşturduğun fieldı burada kullanabilirsin. Oluşturulan property de temel ahlak, temsil ettikleri fieldların adının büyük harfle başlayarak propertyler oluşturulur. Foto3  

👉 ! This, o anki nesneyi temsil ediyordu. Typescriptte this keywordünü kullanmak zorunludur ama C# ta zorunlu değildir.  








