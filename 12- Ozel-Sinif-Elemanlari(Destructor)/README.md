👋 1 - Destructor Metot Nedir?

Destructor/finalizer functions : Bir classtan üretilmiş olan nesne imha edilirken otomatik çağırılan metottur. Constructor yapıcı, destructor yıkıcıdır. New operatörü ile compilerdan o neneyi talep ediyorsan/oluşturuyorsan bu anda constructor devreye giriyor. Constructor nesne oluşturulurken temel konfigurasyonları nesneyle ilgili temel işlemleri yapan ilk tetiklenen fonksiyondur. Nesneyle ilgili artık işlem yapmaya gerek yok/nesneye ihtiyacım yoksa nesneyi yok edicez. Çünkü bellekte bize lazım olmayan bir değere/nesneyle işimiz olmayacak. Destructor nesne imha edilirken kullanılan bir fonksiyondur. Yani final bir fonksiyon, nesnedeki garanti bir şekilde en son tetiklenecek olan fonksiyondur. 

👉 ! C# programlama dilinde destructor sadece class yapılanmasında kullanılabilir ve bir class sadece bir destructor içerir. Constructorda overload işlemleri yapabiliyoruz ama destructorda overload yapamıyoruz. Destructor, parametre alamaz.

👋 2 - Destructor Davranış Modeli 

Nesne imha edilirken/yıkılırken/yok edilirken/silinirken, destructor yıkıcı fonksiyon devreye girer. 

Peki bir nesne hangi şartlarda, kim tarafından imha edilir?

- Bir nesnenin imha edilmesi için ilgili nesne ehrhangi bir referans tarafından işaretlenmemelidir.
- Nesnenin oluşturulduğu ve kullanıldığı scope sona ermiş olamlıdır. Oluşturduğun nesnenin kullanıldığı scope sona erdi ve sen bu nesneyi scope dışına taşımadıysan/vermediysen/dışarıdan bir şekilde ulaşılabilir kılmadıysan artık o nesneye de ihtiyaç olmayacağından nesne de imha olacaktır.
  
Herhangi bir diziye/koleksiyona verdiysen eğer dizinin yada koleksiyonun o anki indexi yine ilgili nesne için bir referanstır. Bu durumda imha edilemez. Ama bir nesne salt bir şekilde referans edilmemişse imha edilir. 

👉 ! Yani anlaşılan ilgili nesne bir daha erişilemez hale gelirse, mimari tarafından/garbage collector ile nesne imha edilir. 

✨ Garbage Collector(GC) ✨

Ramde bir daha kullanılmamak üzere erişilmemek üzere duran nesneler/referanssız nesneler/scopeu bitmiş ilgili görevi bitmiş alanlarda tanımlanmış olan nesneler/dışarıdan bir daha erişilmeyen nesneler çöp diye nitelendirilir. Haliyle bu nesneleri/değerleri toplayan yapılanmalara garbage collector denir. Uygulamada gereksiz olan nesneleri toplamak için Garbage Collector isimli bir mekanizma devreye girer. GC kafasına göre çalışır.
Esasında gc C# da bellek optimizasyonunu üstlenen bir yapılanmadır. C# da gc'ın ne zaman iş göreceği tahmin edilemez, kafasına göre takılır. Dolayısıyla bir geliştiricinin bu mekanizmaya müdahele etmesi pek önerilmez. 

👉 ! Gc ilgili nesneyi imha ederken tam o sırada destructor fonksiyonu devreye girer.

![12-1](https://github.com/user-attachments/assets/82e7e19c-ef28-476c-aaeb-12e1021b0d43)

Parametre alamaz ve tek imzası budur. Overload vs. olamaz. 

![12-2](https://github.com/user-attachments/assets/8c566d58-e779-4e87-9a51-39d4a99154f7)

![12-3](https://github.com/user-attachments/assets/f2be9ce3-e363-498c-843f-57d308c1a890)

Nesne burada(~) imha edilmiş olsaydı bu metot çalışmazdı artık imha edilmeden çnceki son yerdir.

✨ Garbage Collector(GC) Çalışıp Destructor Devreye Girmesi Durum Senaryoları ✨

- Statik yapılanmaların içinde sadece static yapılanmalar çağırılır.
- Gc'ye erişebilmek için GC.Collect() demek yeterlidir. GC, system sınıfının altındadır. GC.Collect(), ilgili dataları topluyor ama destructor tetiklenene kadar bunu yazdırmıyor. Bunu yazdırabilmesi için Console.Readline() demeliyiz.

![12-4](https://github.com/user-attachments/assets/cdc414c2-a20b-4ba6-9302-d13f6de15b35)

Aslında bu şekilde dışarıdan müdahele etmek tavsiye edilmez ama bazen görmek için böyle yapıyoruz.














