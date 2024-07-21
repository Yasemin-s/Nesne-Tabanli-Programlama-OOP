👋 1 - Positional Record Nedir ? 

Nesne nedir?
İçinde veriler tutan bu veriler üzerinde işemler yapmamızı sağlayan fonksiyonlar barındıran bu verileri koruyabilmemizi sağlayan propertyler ile kapsülleme yapmamızı sağlayan yapılar barındıran canlı organizmadır.

Nesneler, kullandığımız özel belirli durumlara göre davranış sergileyen memberlar barındırıyordu(constructor, static constructor, deconstructor, destruct). Bunlar bizim bir nesnenin olağan dışındaki özel memberlarıdır ve belirli durumlara göre davranışlar sergiliyorlar. 

Nesne nasıl ki içinde özel memberlar barındırıyorsa aynı şekilde nesnenin birebir ta kendisi olan sadece davranışsal olarak datasını ön planda tutan record dediğimiz C# 9.0 ile gelen yapılanmlarında kendine has var olan özel memberları özel bir semantikle kullanmamızı sağlayan positional recordları inceleyeceğiz. 

✨  Posiitonal Record Nedir ? ✨

Positional record, C# 9.0 ile gelen ve nominal record'ların bir uzantısı olan bir özelliktir. 
Positional Record:
Positional record'lar, nominal record'ların özel bir formudur. Bu yapı, record tanımında parametreleri doğrudan belirterek daha kısa ve öz bir syntax kullanmanızı sağlar.
Nominal record: public record Person { public string FirstName { get; init; } public string LastName { get; init; } }
Positional record: public record Person(string FirstName, string LastName);

Record'lar, varsayılan olarak init-only özelliklere sahiptir. Bu, nesne oluşturulduktan sonra değiştirilemeyen, ama nesne oluşturulurken değer atanabilen özellikler anlamına gelir.

Positional record'lar, object initializer syntax'ını kullanarak ilk değerleri atamayı kolaylaştırır.
var person = new Person("John", "Doe") { Age = 30 }; şeklinde kullanılır.

Record'lar, değişmez (immutable) nesneler oluşturmak için tasarlanmıştır. Bu, bir kez oluşturulduktan sonra içeriğinin değiştirilememesi anlamına gelir.

👉 ! Classta ne yapabiliyorsak recordda da yapabiliyoruz. 

Positional recordlar esasında recordlar içerisinde tanımlama yapabildiğimiz constrcutor ve deconstructor kullanımlarını daha da özelleştirerek kullanılmasını sağlar. 

Positional record sana bir semantik kazandırıyor. Diyor ki ya kardeşim sen recordda çalışırken constrfutor ve deconstructor oluştururken uzun uzun eski yönteme dayalı oluşturma semnantiğinden ziyade positional record sayesinde gelen yeni bir semantiği kullanarak daha hızlı bir kod inşa et. 

![15-1](https://github.com/user-attachments/assets/c027e13b-ee77-4b70-8bc1-d57b50f87c6d)

Görselde arka planda name ve surname tanımlayacaktır. O imza hem constructor hem deconstructor oluyor. Recordın özelliğinden geliyor bu durum. Propertyler inittir. Property oluşturulurken init... kısmı şu anlama geliyor, sen b usınıftan nesne oluşturuken bu sınıfın nesnesinin oluşum sürecinde object initializerı kullanarak bu propertylere datalarını direkt atayabilirsin ama bu dataların değerlerini daha sonra değiştiremezsin. 

✨  Posiitonal Recordlarda Ayrıca Constructor Tanımlayabilir Miyiz ? ✨

Bir sınıfın içinde birden fazla overloading kuralları gereği constructor tanımlıyorsanız bu constructorlardan istediğiniz birini nesne oluşum sürecinde kullanabilrisiniz. Bu durum recordlarda da geçerlidir. Positional record tanımlanmışsa eğer nesne üretiminde tetiklenmesi/kullanılması zorunludur. 
Kendin manuel birden fazla farklı constructorlar oluştursan dahi o constructorlar tetiklendiği zaman yine positional recordı kullanmak zorundasın. Bunu da this keywordü ile, ilgili constructorı tetikleyerek gerçekleştirebilirsin. This keywordü ile constructor arasında geçiş yapabiliyorsan bunu recordlarda da yapabilirsin. Çünkü recordda bir sınıftır. 

👉 ! İleride structta da constructor olacak onda da this keywordü kullanabileceksin. 

![15-2](https://github.com/user-attachments/assets/f9aa19f3-9724-4896-879b-79793d4b8d1b)

Görselde positional recordun sana getirmiş olduğu constrcutorı tetikletmen gerekiyor.

✨  Posiitonal Record Kullanırken Property Oluşturma✨

![15-3](https://github.com/user-attachments/assets/26493855-450c-4c4b-98df-a65177d3c6d3)

