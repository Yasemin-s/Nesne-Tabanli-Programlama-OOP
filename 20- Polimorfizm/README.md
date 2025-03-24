👋 1 - POLİMORFİZM (ÇOK BİÇİMLİLİK) NEDİR - DERİNLEMESİNE İNCELEYELİM 1

OOP'de temelin üzerine level atlamamızı sağlayan bir basamaktır kalıtım. Bunun getirisi olan mihenk taşları var.

Interface'i Abstract Class'ı anlayabilmek için işte oradaki Abstract Class'ın referansıyla bu Abstract Class'tan türetilmiş olan herhangi bir Instance'ı işaretleyebilmek için Polimorfizmi bilmek gerekir.

✨ NEDİR, NE AMAÇLA KULLANILIR, HANGİ KURALLARI VARDIR ✨

Bir nesnenin birden fazla türle referansla işaretlenebilmesidir.

✨ POLİMORFİZM NEDİR ✨

Poli (Çok)
Form (Morfizmos)
Polimorfizm esasında kalıtım gibi bir biyolojik terimdir. Biyolojik olarak, iki veya daha fazla farklı fenotipin aynı tür popülasyonda bulunmasıdır. Yazılımda ise Polimorfizm, iki veya daha fazla nesnenin aynı tür Class'lardan/referanslardan referans almasıdır/işaretlenebilmesidir.

✨ OOP'DE POLİMORFİZM ✨



İki ya da daha fazla nesnenin aynı tür sınıf tarafından karşılanabilmesidir/referans edilebilmesidir. Bir başka deyişle, bir nesnenin birden fazla farklı türdeki referans tarafından işaretlenebilmesi Polimorfizmdir.

Örnek: Mouse nesnesi var elimde, Mouse bir Class Ürün sınıfından kalıtım alıyorsa eğer bu fare bir yandan da üründür. Farenin fare olması bu 1. biçimdir. Farenin ürün olması ise 2. biçimdir. Bu fare nesnesi, hem fare referansı tarafından hem de ürün referansı tarafından referans edilebilmesi durumu Polimorfizmdir.

Bir nesne kalıtımsal açıdan ataları ne ise atalarının referansı ile işaretlenebilir.
Polimorfizm, bir nesnenin kalıtımsal olarak ilişkisi olan diğer nesnelerin referanslarıyla işaretlenebilmesini sağlar.

Polimorfizm, OOP tasarımlarında geliştirilen koda daha manevrasal bir şekilde nitelik kazandıran ve yaklaşım sergilememizi sağlayan bir özelliktir.

![20-1](https://github.com/user-attachments/assets/f7569879-45c6-47d9-b93d-6939f3d44a77)

Polimorfizm, programlamadaki temel prensip olan sol/sağ prensibini aşıp eldeki nesnenin birden fazla referansla işaretlenebilmesini sağlar. Yani Polimorfizm şunu söylüyor: Polimorfizmin dışında elindeki herhangi bir nesneyi sadece o nesnenin referansıyla işaretleyebiliyorsun. Ama Polimorfizm sayesinde, elindeki bir nesneyi o nesnenin türünün dışında referanslarla da işaretleyebilirsin. İşte bu nesneye farklı türlerdeki referanslarla işaretleyebilme niteliği kazandıran yapılanmaya Polimorfizm denir. Yani A türünden bir nesneyi A türünden bir referansla işaretleyebilmenin yanında A türünden bir nesneyi B türünden C türünden bir referansla işaretleyebilmeyi sağlar. İşte farklı türlerden, çok türlerden işaretleyebilmek çok biçimliliktir.

✨ BİR NESNENİN BİRDEN FAZLA REFERANSLA İŞARETLENMESİ NEYE YARAR? ✨



Bir nesnenin, birden fazla referansla işaretlenebilmesi, o nesnenin birden fazla türün davranışını sergilemesini sağlar.

✨ POLİMORFİZM FELSEFESİ 1 ✨



Yazılımsal açıdan çok biçimliliğin söz konusu olabilmesi için teknik olarak kalıtım olması gerekmektedir.

✨ PROGRAMLAMADA POLİMORFİZM NEREDEN KULLANILMAKTADIR? ✨

Programlamada Polimorfizm esasında taa en temelden beri kullanılmaktadır.

Örnek: Elimizdeki herhangi bir byte türündeki veriyi ister byte istersek de byte'dan büyük olan herhangi bir türde tutmak çok biçimliliktir.
Ya da Object türünü herhangi bir türdeki değeri alabilmesi yahut bir başka deyişle Object türüne herhangi bir türdeki veriyi atayabilmek Polimorfizmdir.

![20-2](https://github.com/user-attachments/assets/71787ebc-9f78-4a2a-ab3a-32de075486ab)

Bütün sınıflar Object'ten türüyorsa eğer, Object'te bize bu sınıfları referans edebilme niteliği kazandırıyor. Yani Polimorfizm çok biçimlilik var. X diye bir sınıfım var, X sınıfı doğal olarak Object'ten türediğinden dolayı X hem X referansıyla hem de Object referansı ile işaretlenebilir. İşte Object referansı ile işaretleyebilmemizin altında yatan sebep kalıtımın bize sunduğu Polimorfizm özelliğidir.

Tabi çok biçimlilik dendiğinde temel programlamadaki bu durumlardan ziyade (String'in, String olarak ve Object olarak tutulabilmesi) esas nesne tabanlı programlamadaki getirileri önemlidir. Haliyle nesne tabanlı programlamada bir nesneyi kendi türünün referansıyla birlikte farklı türdeki referanslarla işaretleyerek Polimorfizmi uygulayabilmekteyiz.

Peki bunu nasıl yapıyoruz? Normal şartlarda bir nesne kendi sınıfının referansı dışında başka bir sınıfın referansıyla işaretlenemez. Evet, bir nesnenin başka bir nesne ile işaretlenebilmesi/referans edilebilmesi için kesinlikle arada kalıtımsal bir ilişki olması gerekmektedir. Yani bir başka deyişle, nesne tabanlı programlamada Polimorfizm uygulamak istiyorsanız türler arasında kalıtım uygulanmış olmalıdır. Ya da bambaşka bir deyişle, nesne tabanlı programlamada Polimorfizm aralarında kalıtımsal ilişki olan sınıflarda uygulanabilir. Aksi mümkün değildir.

![20-3](https://github.com/user-attachments/assets/ba0f9d60-8c3c-4946-be58-5e3ef59eaa6c)


✨ POLİMORFİZM KALITIM İLİŞKİSİ ✨



Bir nesneyi, kendi türünün dışındaki bir tür ile/referansla işaretleyebilmek için kesinlikle ilgili nesne, o türden türemiş olması gerekir.

![20-4](https://github.com/user-attachments/assets/44d327e3-e983-488a-9a55-abab9d884306)

![20-5](https://github.com/user-attachments/assets/a2d33727-942f-4542-8614-f7dfc8363cd2)

👉 ! Kalıtım bize Polimorfizm sağlıyor.


👉 ! Birden fazla tür ile farklı türdeki nesneyi referans etmeye çok biçimlilik, Polimorfizm denir.

✨ POLİMORFİZM BİR NESNE YÖNETİMİNDE NEYE YARAR? ✨



Daha önce de söylediğimiz gibi, bir nesnenin birden fazla referansla işaretlenmesi, o nesnenin birden fazla türün davranışlarını gösterebilmesini sağlar.

![20-6](https://github.com/user-attachments/assets/645c6832-880c-4d36-87f3-f43694ee71c8)

![20-7](https://github.com/user-attachments/assets/02ad6e83-ff97-46cf-87c3-3691ae440478)

![20-8](https://github.com/user-attachments/assets/a0ea2fb4-0a67-456b-bafd-59cf500070db)

Polimorfizm, bir nesnenin kendi türünün dışında bir veya birden fazla türle işaretlenebilmesidir/referans edilebilmesidir. Ve bunun bize getirmiş olduğu farklı davranışları sergileyebilme niteliğidir.
