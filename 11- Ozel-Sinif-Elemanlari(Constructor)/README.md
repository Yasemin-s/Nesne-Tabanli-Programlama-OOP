👋 1 - Özel Sınıf Elemanları - Constructor Metodu

Bir sınıf, içinde farklı memberlar barındıran field, property, metot ve indexer gibi memberlar barındıran ve bu memberlar eşliğinde ürettiğimiz nesne üzerindeki değerlerde işlemler yapmamızı sağlayan tanımlayıcı bir yapılanmaydı. Yani sınıf, nesne modeliydi. 
Bu sınıf üstünden üretilecek olan nesnenin üzerinde, bu nesnenin üretim esnasındaki yapılacak operasyonları tanımlamamızı sağlayacak olan aynı şekilde üretilen bu nesne bir gün imha edilecek ve bu imha edilme sürecinde son kez yapılacak işlemlere dair tanımlamaları sağlayacak olan özel fonksiyonlar vardır. Bu tarz durumlarda işlem yapmamızı sağlayan fonksiyonlara classın özel memberları diyeceğiz. Üç tanedir, constructor, static constructor, deconstruct(yıkıcıdır). Bu özel memberlar tüm sınıflarda ortak olarak kullanılabilir yapılanmalara sahiptir. 

👉 ! Özel sınıf elemanları kesinlikle fonksiyondur, property vs. olamaz.

👋 2 - Constructor Nedir ? 

new T(); ile nesne üretiyoruz. Burada metot tetiklenir ve bu metot constructor metottur. Constructor metot adı üstünde yapıcı metot, inşa edici metottur. Nesnenin yapıcılığı ilk ayağa kaldırılırken inşasını/konfigürasyonlarını yapıyor. 

👉 ! Constructor, bir nesne üretimi sürecinde ilk tetiklenen metottur. 
👉 ! Constructor, nesne oluşturma sürecinde mutlaka tetiklenmek zorundadır. 

Bir sınıfım var, bu sınıftan bir instance, nesne, örnek üetirken bu sınıftaki değerlere başlangıç değerleri verilsin istiyorum. Constructorda, oluşturduğun nesneye dair ilk konfigurasyonları yapabilirsin. Yapmak zorunda değilsin ama genelede constructor bu amaçla kullanılır.

👉 ! Constructor, new ile nesne yaratma talebi geldikten ve ilgili nesneye hafızada yer ayırdıktan sonra tetiklenir. Şöyle düşün, new MyClass ile nesne oluşturuldu, hafızada yer aldı. () ile de önceden var olan nesnenin constructor metodu çağrıldı gibi düşün.

👋 3 - Constructor Metot Nasıl Oluşturulur ?

![11-1](https://github.com/user-attachments/assets/a3d17ee8-dd70-44e1-bcb9-7f9ddaf8b578)

Constructor, C# 9.0 da gelen MyClass a = new(); kullanımında bile belirtilmek zorundadır. Yani nesne oluşturuken () belirtmek zorundasın.
Constructor, özel bir sınıf elemanıdır. Özel olsada fıtart olarak bir metottur. Fakat bildiğimiz metot imzalarından bir nebze farklıdır.

👉 ! Constrcutorların, metot adı sınıf adıyla aynı olmalıdır. Özel sınıf elemanlarının dışında hiçbir member sınıf adıyla aynı olamaz. Geri dönüş değer olamaz/belirtilemez. Erişim belirleyicisi public olmalıdır. Private olduğu durum ayrı incelenecektir. 

✨ Default Constructor ✨

Her sınıfın içinde tanımlamasak da default bir constructor mevcuttur. Şimdiye kadar biz constructor oluşturmadan bir classdan nesne oluşturup constructorı tetikliyorduk, bu nasıl oluyordu?. Çünkü, default constructor vardı. Eğer sen bir class içine constructor yazarsan default constructorı ezmiş olursun.

✨ Parametreli Constructor ✨

![11-2](https://github.com/user-attachments/assets/734dbe0a-afb1-44c5-ba17-aeef58ff35be)

Constructorlar, parametre alabilen yapılardır. Ben bir nesne üretirken, ilk konfigurasyonları constrcutor metodu içinde yapabilirm aynı şekilde nesneyi üretirken dışarıdan, dış dünyadan alınacak parametreleri/değerleri de constructor üzerinden verebilirm. Dolayısıyla constructor parametre alabilen yapılardır. 

✨ Constructor Overload ✨

Bir sınıf için birde fazla constructor tanımlaması yapabiliriz.

👋 4 - Constructorın Erişim Belirleyicisinin Private Olma Sorunsalı 

Constructor private olursa, nesne üretimi engellenmiş olur. Çünkü nesne oluşması için constructor metodu tetiklenmek zorundadır. 

![11-3](https://github.com/user-attachments/assets/59d50fb8-f1a8-47f1-b147-a2a7fcb0d114)

MyClass(){} yada private MyClass(){} şeklinde kullanabilirsin. Bu nesne oluşumunu engellemek bizim nerede işimize yarıyor? Örneğin singleton design patternda işe yarıyor. 
Private ile nesne oluşumunu engelliyoruz ama dışarıdan oluşumu engelliyoruz. İlgili sınıf içinden privatea biz erişebildiğimiz için orada nesne oluşturulabiliyor. Nesne oluşturmayı dışarıdan engelleyip içeriden nesne oluşturma sürecini yönetmek istediğinizde o sınıfın nesnesinin dışarıdan talep edilmesini engellemeniz gerekir. Nesne üretimi dışarıdan engellenir. Yani constructorın olduğu sınıf değil olmadığı sınıfta erişim engellenir.

![11-4](https://github.com/user-attachments/assets/a327b11d-40ba-449a-8303-76c273da857d)

👋 5 - This Keywordü İle Constructorlar Arası Geçiş

Bir sınıfta birden fazlqa overloading yaparak constructor tanımladığımızda herhangi bir constructor üzerinden sınıftan nesne inşa ederken this keywordünü kullanabiliriz. 

👉 ! Bir sınıfın içinde this keywordü o sınıfın o anki nesnesini temsil eder. 

This keywordü nasıl ki o anki sınıfın nesnesini temsil ediyor aynı şekilde this keywordü bir sınıfın nesnesinin içindeki birden fazla constructorlar arası geçiş yapabilme sorumluluğunu da üstlenir. Nihayetinde nesneyi temsil eden nesne içindeki constructorlarında aralarında geçiş yapmasını sağlayan nitelik taşımaktadır. 

![11-5](https://github.com/user-attachments/assets/b9184f4e-8210-42c9-905f-66f5291dae34)

Burada parametreli constructor çalıştırılsın ve aynı zamanda parametresiz olan constructor da çalışsın istiyorum. Bu durumda this keywordü kullanılır. :() operatör, kalıtımda kullanılan bir operatördür. This ile bu nesnenin constructorlarını bana getir demiş olduk. Bu şekilde this kullandığında o constructor dışında olan constructorlara erişmeni sağlar. 

![11-6](https://github.com/user-attachments/assets/ae68c86f-20da-4bf0-b311-0085aef73bb3)

Buradaki this de constructorlardaki değişkenler kullanılır. Örneğin sen MyClass sınıfının içinde public int c tanımladıysan ve this keywordünü kullandığın yerde c yazdıysan hata verecektir.Böyle bir kullanım yok. Ama erişilebilen değişkenlerin dışında manuel değer de verebilirsin, this(123) gibi.

👋 6 - Recordlarda Constructor

![11-7](https://github.com/user-attachments/assets/aa095a38-6651-4c30-a441-6f963c122d64)

Recordlarda bir class olduğu için classda ne yaptıysak aynen burda da onları uygulayabiliriz, kullanabiliriz.
