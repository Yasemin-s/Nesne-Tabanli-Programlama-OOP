👋 1 - Record Nedir? OOP deki Yeri Neresidir?

Recordı anlayabilmek için ön hazırlık - İnit Only Properties : 

 ✨ İnit Only Properties ✨

C# 9.0 da, herhangi bir nesnenin propertylerine ilk değerlerinin verilmesi ve sonraki süreçte bu değerlerin değiştirilmemesini garanti altına almamızı sağlayan init only properties özelliği gelmiştir. Yani herhangi bir propertyi read only haline getirir. Bu özellik sayesinde nesnenin sadece ilk yaratılış anında propertylerine değer atanmakta ve böylece iş kuralları gereği runtime da değeri değişmemesi gereken nesneler için ideal bir önlem alınmaktadır. 

👉 ! Nesnenin ilk yaratılış anına object initializer denir. Object initializer anında read only bir propertye değer atayamazsın. Atayabilmek istiyorsan init only property kullanmak gerekir. İnit only properties, object initializer dediğimiz nesnenin ilk yaratılış anında değer atamayı ve sadece okunur yapmayı sağlar. 

foto1- Propertyin get set kısımlarından seti kaldırırsan sadece okunur hale getirirsin ve sadece okunur hale getirdiğin için ilk değeri atayamazsın. İşte bu sıkıntıdan doalyı set kalkmış olsa bile ilk değerini = 3 şeklinde verebiliyorsun. 

👉 ! İnit only properties, developer açısından süreç esnasında değiştirilmemesi gereken property değerlerinin - yanlışlıkla - değiştirilmesinin önüne geçmekte ve böylece olası hata ve buglardan yazılım arındırmaktadır. 

👋 2 - İnit Only Properties ve Getter Only Properties Arasında Nasıl Bir Fark Var ? 

Readonly bir propertye değer atamaya çalıştığımızda hata verir. Foto2 - init only properties ise readonly bir propertye değer vermeyi sağlar. 

👋 3 - İnit Only Propertis Nasıl Tanımlanır ? 

Foto3 - İnit only properties özelliğini kullanabilmek için init keywordünü kullanmak yeterlidir. İnit ile, property sadece okunabilir ve object initializer olduğunda değer ataması gerçekleştirilebilir. Ayrıca init, get keywordü olmadan kullanılmaz ve gereği yapısı bu semantikte set bloğu kullanılmaz. 

public string Name { get; init; } = "yase"; bu şekilde direkt değer atamanın adı, auto propert initializerdır ve get init konseptinde ilk değerini constructordan da alabilir. 

Readonly fieldlarda init only property kullanımı kritik: İnit bir yandan set görevi görür. Readonly property de değer atamak istiyorsak init kullanabiliriz. Foto4 

👋 4 - Record Nedir ? 

Record bir nesne hatta class, classın kendisidir. 
C# 9.0 ile gelen init only properties özelliği, nesne üretim esnası dışında değişmez değerler oluşturulması için constructor ve auto property initializer yapısının yanında object initializer yapısının kullanılabilir olmasını sağlıyordu.  

Ftot5 - Eğer ki bir propertyde sabitlik/değişmemezlik/salt okunurluk/readonly/sadece okunabilirlik amaç ediniliyorsa init-only properties özelliği kullanılabilir. Ama eğer ki object bütünsel olarak değişmez olsun istiyorsan bu durumda init yetersiz kalacaktır. İhtiyacımız olan intten fazlasıdır. İşte bu ihtiyaçtan dolayı record türü geliştirilmiştir. 

👉 ! Record, bir propertyin değişmezliğinden ziyade nesnenin genel olarak değerinin değişmemesine odaklanır. Record, bir objenin sabit/değişmez olarak kalmasını sağlamakta ve bu durumu güvence altına almaktadır. Böylece bu obje, artık değeri değişmeyeceğinden dolayı esasında objectten ziyade değer gözüyle bakılan bir yapıya dönüşecektir. 

👉 ! Nesne ön planda ise bu class, nesnenin değerleri ön plandaysa bu recorddır. Buradan yola çıkarak recordları, içerisinde data barındıran  lightweight(hafif) classlar olarak değerlendirebiliriz. Nesneden çok değerler ön planda olduğu için. 

👉 ! Recordlar, classlara istinaden objectten farklı olarak içerisinde bulunan dataları sabitleyerek, nesneden ziyade verileri/dataları ön plana çıkarır. 

👉 ! Recordlar bir classtır. Sadece nesnelerinden ziyade değerleri ön plana çıkmış classtır. foto6

👋 5 - Record Tanımlama

Foto7- Sağdaki gibi tanımlanan recordlara norminal record ednir. Recordın sınıf olabilmesi için propertylerin hepsinin init ile işaretlenmesi gerekecektir. 

  ✨ Record İle Class Arasındaki Fark Kritiği Yapalım ✨

Record yapılanmalarında istersen değer değiştirebiliyorsun ama record oluşturulma amacı değiştirilemez nesneler oluşturmaktır. Recordlar, değiştirilemez objeler oluşturmamızı sağlar. Peki bu değiştirelemez objeleri classlar ile gerçekleştiremez miyiz? Bunu normal classlar ile de yapabiliyoruz ama record bu nedenle gelmedi zaten, daha anlamlı daha profesyonel çalışmalar yapabilelim diye geldi. 

Foto8 - Classta sadece init kullanabilirm. Ama sen nesneden çok değeri ön planda tutmak istersen record kullanabilirsin. foto8 de alt kısımdaki kod için, bu nesnenin süreçte herhangi bir property değerini değiştirmek istediğimizde bunu gerçekleştirebilmek için yeni bir employee nesnesi üretmemiz ve değişkenliğin yapılacağı property dışında diğer propertyleri bu nesneden eşleştirmemiz gerekecek. 
Foto9 - Yeni bir employee sınıfı oluşturduk. Name ve surname  bilgisiniemployee1 den aldık. Employee1 in positionu 2 olarak değiştirdik. Yani değişmeyecek olan nesnenin propertylerini ilgili nesneden eşleyerek aldık. Bu şekilde kullanımı az property olduğunda yaparız ama çok fazla property olsaydı bunu yapmak can sıkıcı oalcaktı. Ne kadar çok property o kadar zor maliyetli kod demektir. Elbette reflection veya serialization ile kopyalama mantıkları uygulanabilir veya auto mapping kütüphanesi kullanılabilir. Ama bu tarz bir durumda classlar işini zorlaştıracaktır. 
Eğer ki sabit datalarla çalıştığın nesnelerde recordda çalışıyorsan, record ilgili dataları hem ön plana çıakrıyor hem de bu şekilde nesneyi çoğaltma durumlarında yeni expressionlar getirmektedir. 

 ✨ With Expression ✨

Elindeki herhangi bir nesneyi hızlı bir şekilde klonlayabilmek ve yeni bir nesne oluşturmak istiyorsan bunu classlarda yapmak senin için zahmetli olacaktır. Ama recordlarda çalışıyorsan with expression kullanabilrisin. 

İmmutable(değiştirelemez,sabit) türlerde çalışırken nesne üzerinde değişiklik yapabilmek için ilgili nesneyi çoğaltıp/klonlayıp(deep copy)  üzerinde değişiklik yapman gerekmekte yada manuel yeni bir nesne üretip mevcut nesnede değerleri, değişikliği yansıtacak şekilde aktarmamız gerekmektedir. Bu tarz durumlarda with function ile çözüm eskilerde kullanılmıştır. Foto9 . Ama bu tarz senaryolarda record kullanıyorsan elindeki recordu direkt kopyalamanı sağlayacak syntax olan with ifadesi gelmiştir. Foto10, değiştirilecek property {} içinde belirtilmiştir. 




