👋 1 - Record Nedir? OOP deki Yeri Neresidir?

Recordı anlayabilmek için ön hazırlık - İnit Only Properties : 

 ✨ İnit Only Properties ✨

C# 9.0 da, herhangi bir nesnenin propertylerine ilk değerlerinin verilmesi ve sonraki süreçte bu değerlerin değiştirilmemesini garanti altına almamızı sağlayan init only properties özelliği gelmiştir. Yani herhangi bir propertyi read only haline getirir. Bu özellik sayesinde nesnenin sadece ilk yaratılış anında propertylerine değer atanmakta ve böylece iş kuralları gereği runtime da değeri değişmemesi gereken nesneler için ideal bir önlem alınmaktadır. 

👉 ! Nesnenin ilk yaratılış anına object initializer denir. Object initializer anında read only bir propertye değer atayamazsın. Atayabilmek istiyorsan init only property kullanmak gerekir. İnit only properties, object initializer dediğimiz nesnenin ilk yaratılış anında değer atamayı ve sadece okunur yapmayı sağlar. 

![10-1](https://github.com/user-attachments/assets/0a44c47a-11ad-4043-b604-4414eaa05cee)

Propertyin get set kısımlarından seti kaldırırsan sadece okunur hale getirirsin ve sadece okunur hale getirdiğin için ilk değeri atayamazsın. İşte bu sıkıntıdan doalyı set kalkmış olsa bile ilk değerini = 3 şeklinde verebiliyorsun. 

👉 ! İnit only properties, developer açısından süreç esnasında değiştirilmemesi gereken property değerlerinin - yanlışlıkla - değiştirilmesinin önüne geçmekte ve böylece olası hata ve buglardan yazılım arındırmaktadır. 

👋 2 - İnit Only Properties ve Getter Only Properties Arasında Nasıl Bir Fark Var ? 

Readonly bir propertye değer atamaya çalıştığımızda hata verir. 

![10-2](https://github.com/user-attachments/assets/60ab16d1-3326-4779-8ad0-76fa2ca51bbe)

Init only properties ise readonly bir propertye değer vermeyi sağlar. 

👋 3 - Init Only Propertis Nasıl Tanımlanır ? 

 ![10-3](https://github.com/user-attachments/assets/dfa24886-7c47-4993-af95-6c1246048a95)

Init only properties özelliğini kullanabilmek için init keywordünü kullanmak yeterlidir. İnit ile, property sadece okunabilir ve object initializer olduğunda değer ataması gerçekleştirilebilir. Ayrıca init, get keywordü olmadan kullanılmaz ve gereği yapısı bu semantikte set bloğu kullanılmaz. 

public string Name { get; init; } = "yase"; bu şekilde direkt değer atamanın adı, auto propert initializerdır ve get init konseptinde ilk değerini constructordan da alabilir. 

![10-4](https://github.com/user-attachments/assets/33ffcd42-3742-4353-861a-3090845a64a7)

Readonly fieldlarda init only property kullanımı kritik: Init bir yandan set görevi görür. Readonly property de değer atamak istiyorsak init kullanabiliriz. 

👋 4 - Record Nedir ? 

Record bir nesne hatta class, classın kendisidir. 
C# 9.0 ile gelen init only properties özelliği, nesne üretim esnası dışında değişmez değerler oluşturulması için constructor ve auto property initializer yapısının yanında object initializer yapısının kullanılabilir olmasını sağlıyordu.  

![10-5](https://github.com/user-attachments/assets/b8cd7c90-c78f-4c33-b76c-ebd4996940d2)

Eğer ki bir propertyde sabitlik/değişmemezlik/salt okunurluk/readonly/sadece okunabilirlik amaç ediniliyorsa init-only properties özelliği kullanılabilir. Ama eğer ki object bütünsel olarak değişmez olsun istiyorsan bu durumda init yetersiz kalacaktır. İhtiyacımız olan intten fazlasıdır. İşte bu ihtiyaçtan dolayı record türü geliştirilmiştir. 

👉 ! Record, bir propertyin değişmezliğinden ziyade nesnenin genel olarak değerinin değişmemesine odaklanır. Record, bir objenin sabit/değişmez olarak kalmasını sağlamakta ve bu durumu güvence altına almaktadır. Böylece bu obje, artık değeri değişmeyeceğinden dolayı esasında objectten ziyade değer gözüyle bakılan bir yapıya dönüşecektir. 

👉 ! Nesne ön planda ise bu class, nesnenin değerleri ön plandaysa bu recorddır. Buradan yola çıkarak recordları, içerisinde data barındıran  lightweight(hafif) classlar olarak değerlendirebiliriz. Nesneden çok değerler ön planda olduğu için. 

👉 ! Recordlar, classlara istinaden objectten farklı olarak içerisinde bulunan dataları sabitleyerek, nesneden ziyade verileri/dataları ön plana çıkarır. 

![10-6](https://github.com/user-attachments/assets/2b08a35f-c8aa-4f8e-afa7-52a11a1a903a)

👉 ! Recordlar bir classtır. Sadece nesnelerinden ziyade değerleri ön plana çıkmış classtır.

👋 5 - Record Tanımlama

![10-7](https://github.com/user-attachments/assets/ce84f6c8-371c-46c0-83db-dc571fb013f7)

Sağdaki gibi tanımlanan recordlara norminal record ednir. Recordın sınıf olabilmesi için propertylerin hepsinin init ile işaretlenmesi gerekecektir. 

  ✨ Record İle Class Arasındaki Fark Kritiği Yapalım ✨

Record yapılanmalarında istersen değer değiştirebiliyorsun ama record oluşturulma amacı değiştirilemez nesneler oluşturmaktır. Recordlar, değiştirilemez objeler oluşturmamızı sağlar. Peki bu değiştirelemez objeleri classlar ile gerçekleştiremez miyiz? Bunu normal classlar ile de yapabiliyoruz ama record bu nedenle gelmedi zaten, daha anlamlı daha profesyonel çalışmalar yapabilelim diye geldi. 

![10-8](https://github.com/user-attachments/assets/caff6c9b-dc48-4eed-9607-6c9ba5eb04d6)

Classta sadece init kullanabilirm. Ama sen nesneden çok değeri ön planda tutmak istersen record kullanabilirsin. foto8 de alt kısımdaki kod için, bu nesnenin süreçte herhangi bir property değerini değiştirmek istediğimizde bunu gerçekleştirebilmek için yeni bir employee nesnesi üretmemiz ve değişkenliğin yapılacağı property dışında diğer propertyleri bu nesneden eşleştirmemiz gerekecek. 
Foto9 - Yeni bir employee sınıfı oluşturduk. Name ve surname  bilgisiniemployee1 den aldık. Employee1 in positionu 2 olarak değiştirdik. Yani değişmeyecek olan nesnenin propertylerini ilgili nesneden eşleyerek aldık. Bu şekilde kullanımı az property olduğunda yaparız ama çok fazla property olsaydı bunu yapmak can sıkıcı oalcaktı. Ne kadar çok property o kadar zor maliyetli kod demektir. Elbette reflection veya serialization ile kopyalama mantıkları uygulanabilir veya auto mapping kütüphanesi kullanılabilir. Ama bu tarz bir durumda classlar işini zorlaştıracaktır. 
Eğer ki sabit datalarla çalıştığın nesnelerde recordda çalışıyorsan, record ilgili dataları hem ön plana çıakrıyor hem de bu şekilde nesneyi çoğaltma durumlarında yeni expressionlar getirmektedir. 

 ✨ With Expression ✨

Elindeki herhangi bir nesneyi hızlı bir şekilde klonlayabilmek ve yeni bir nesne oluşturmak istiyorsan bunu classlarda yapmak senin için zahmetli olacaktır. Ama recordlarda çalışıyorsan with expression kullanabilrisin. 

İmmutable(değiştirelemez,sabit) türlerde çalışırken nesne üzerinde değişiklik yapabilmek için ilgili nesneyi çoğaltıp/klonlayıp(deep copy)  üzerinde değişiklik yapman gerekmekte yada manuel yeni bir nesne üretip mevcut nesnede değerleri, değişikliği yansıtacak şekilde aktarmamız gerekmektedir. Bu tarz durumlarda with function ile çözüm eskilerde kullanılmıştır.

![10-9](https://github.com/user-attachments/assets/56b5015b-db57-427d-9824-59e012cc41a2)

Ama bu tarz senaryolarda record kullanıyorsan elindeki recordu direkt kopyalamanı sağlayacak syntax olan with ifadesi gelmiştir. 

![10-10](https://github.com/user-attachments/assets/0a6de22c-bf71-414c-a7c4-628a04900441)

Değiştirilecek property {} içinde belirtilmiştir. 
