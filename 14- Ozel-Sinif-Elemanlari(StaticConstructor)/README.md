👋 1 - Static Constructor Metot Nedir ? 

Nesnenin yani sınıf yapılanmasının özel memberlarından olan static constrcutorı inceleyeceğiz. Static constructorı anlayabilmek için static yapılanmayı anlamak gerekir. 

👉 ! Bir sınıftan nesne üretilirken constructora nazaran ilk tetiklenen metot static constructordur. Ondan sonra constructor ondan sonrada ne istiyorsan o tetiklenir. 

👉 ! Constructor, bir sınıftan nesne üretilirken tetiklenen bir fonksiyondur. Statik constructor, ilgili sınıftan ilk nesne üretilirken bir kereye mahsus tetiklenen metottur. 

👉 ! Bir sınıftan ilk defa nesne üretiliyorsa ilk tetiklenen fonksiyon static constructortır sonra constrcutor fonksiyonu tetiklenir. 

👉 ! Static yapılanmalar, uygulama bazlı datalarımızı yerleştirdiğimiz alanlardır. Static, nesneden bağımsızdır.

C# programlama dilinde, bir sınıfın constructor(kurucu) metodunu private olarak tanımladığınızda, bu sınıfın nesnelerini doğrudan o sınıfın dışından oluşturamazsınız. Bu, sınıfın sadece belirli koşullarda ve genellikle sınıfın kendi static metotları veya iç sınıfları tarafından örneklendirilmesini sağlar. Private constructor, genellikle singleton desenini uygularken veya nesne oluşturulmasını kontrol etmek istediğiniz diğer durumlarda kullanılır. 

Static constructorda geri dönüş değeri yoktur. 
İsmi sınıf ismiyle aynı olmalıdır.
static MyClass(){} şeklinde tanımlanır. 
Static constructorda, normal constructordaki gibi erişim belirleyicileri kullanılmaz. 
Geri dönüş değeri bildirilmez. 
Overloading yapılmaz. 
Parametre almaz.
Bir sınıf içinde sadece bir tane static constructor tanımlanabilir.   

![14-1](https://github.com/user-attachments/assets/3ba406c6-0a70-4018-80ab-598a8d4946d6)

![14-2](https://github.com/user-attachments/assets/7cfee9e1-c774-4ecd-a5fd-e454cd71b66a)

Static constructorın tetiklenebilmesi için illa ilk nesne üretimine gerek yok. İlgili sınıf içinde herhangi bir static yapılanmanın tetiklenmesi/static memberın tetiklenmesi de static constructorın tetiklenmesini sağlayacaktır. 
İstersen nesne oluştururken tetiklersin isetrsen static memberları kullanırken tetiklersin. 

👉 ! Dikkat edilmesi gereken şey static constructor bir kez tetiklenir. 

Singleton design pattern kullanırken staic constructor kullanılır. Singleton design pattern, bir sınıftan uygulama bazında sadece tek bir nesne oluşturulmasını istiyorsan kullanabileceğin bir desgin patterndır. Bir sınıfı singleton/tekil yapmak istiyorsan onun constructorını private etmen gerek. Nesne üretimini engellemen gerek. 

![14-3](https://github.com/user-attachments/assets/54d841b7-5d81-460e-943e-55915a6837d1)

Yukarıdaki görsel singelton design pattern örneğidir.

👉 ! Static yapılanmalara sınıf ismi üzerinden erişilir. 
👉 ! Nesneler her daim yapıları ne olursa olsun statşic vs. ne olursa, heapte tutulur. 

👉 ! Static yapılanma, normal constructordan önce tetiklenen fakat ilk nesne üretilirken yada herhangi bir static yapılanma ilk tetiklenirken tetiklenen bir yapılanmadır. Onun dışındaki bütün nesne üretimlerinde normal constructor tetiklenir. 
