👋 1 - Inheritance - Kalıtım

✨ Bir Programcı Açısından Kalıtım Nedir ? ✨

Object orianted dediğimiz yaklaşım gerçek hayattan modellenerek yazılıma uygulanmış/uyarlanmış yaklaşımdır. Kalıtım, OOP'nin en önemli özelliğidir. Üretilen nesneler farklı nesnelere özellikelrini aktarabilmekte ve böylece hiyerarşikbir düzenleme yapılabilmektedir. Bu aktarma işine kalıtım/inheritance denir.
Elimde bir nesne var belirli özellikleri field/member/metot/proeprty bunlardan belirlediklerini başka bir nesneye aktarmayı sen kalıtım ile sağlıyorsun. 

![16-1](https://github.com/user-attachments/assets/caaa0f75-b6a7-4ff6-9f2a-c045337f6643)


Bir programcı açısından, aynı aile grubundan gelen nesnelerin yada yatayda eşit seviyede olan tüm olguların benzer özelliklerini tekrar tekrar herbirinde tanımlamaktansa bir üst sınıfta tanımlamasını ve her bir sınıfın bu zöellikleri üst sınıftan kalıtımsal olarak almasını sağlar. Erkek kadın insan grubundan, insan hayvan bakteri bitki canlı sınından. 
Örneğin, erkek ve kadın yani insan için ikisininde ortak özellikleri olabilir. İşte bunu bir sınıftta yap ve bundan kalıtım al diyoruz. İkisininde kulağı ağzı vs. var. Ama kadına yada erkeğe ait özellikler ortak değildir. Böylece hem kod maliyeti düşmekte, hem de mimarisel tasarım açısından avantaj sağlanmaktadır. 

👉 ! Bir çok design pattern OOP'deki kalıtım üzerine kuruludur.

✨ Her Sınıfı Kalıtımsal Operasyona Tabi Tutmalı Mıyım ? ✨

Bütün sınıfları kalıtımsal olarak kullanmak zorunda dweğilsin. Her yerde kalıtım kullanmak zorunda değilsin, kaltıımı ihtiyacın varsa/lazımsa kullanırsın.

![16-2](https://github.com/user-attachments/assets/b8769bd3-406a-48d7-8883-d16bc204ba99)

Görselde, kadın ve erkekte de aynı özellikleri tanımlayarak kod maliyetini arttırdım. Aynı olguda olan sınıfları tekrar eden memberlarını bir başka sınıfta toplayarak ilgil sınıflara kalıtımsal oalrak aktarmak daha doğrudur. Erkek ve kadın sınıfları insan sınıfından kalıtım alırsa/türetilirse/miras alırsa insan sınıfındaki tüm memberlar(erişime izin verilen/miras olarak aktarılmasına izin verileren memberlar) miras olarak aktarılır. Güncellenemeyen/diğerlerinde olmayan ve sadece o sınıfa ait olan özellikelr direkt ilgili sınıfta tanımlanmaldıır. 

✨ Kalıtımın Kullanılmadığı Durumlar ✨

![16-3](https://github.com/user-attachments/assets/a1b2ebe0-b73f-4488-b390-661d3e44f971)

✨ Kalıtımın Kullanıldığı Durumlar ✨

![16-4](https://github.com/user-attachments/assets/fd4afa73-2931-4b97-9b93-806ef9751b16)

İleride, görseldeki kaltıım veren ve kalıtım alan sınıfları terminolojik olarak isimlendireceğiz. Birine base class vs. dieyecğiz. 

Kalıtım gelişigüzel bir şekilde tasarlanmamlıdır. Ortak olguda olan nesneleri temsil edecek olan bir üst sınıf olmalı ve daha evrensel nitelikte bir olgu olmaldıır. Opel, mercedes ve fiat ortak olgudur. Yani üçüde bir arabadır. Haliyle bunların kaltıım operasyonunda, kalıtım veren sınıfın erişilebilen tüm memberları kaltıım alan sınıfa kalıtsal olarak aktarılacaktır.

Kalıtım veren sınıf neyi kalıtım vereceğini, içindeki memberların erişim belirleyicisi dediğimiz keywordler sayesinde belirtilir. Örneğin, public bütün kalıyımsal durumlarda aktarılır. Protected da akatılır. Erişim belirleyicileri de ileride incelenecektir. 

Aynı kodları tekrar tekrar tüm sınıfta yazmaktansa kaltıımdan faydalanmak en doğrusudur. Bu sayede bir merkezi yerden tekrar eden, ortak olan yapılanmaları yönetebiliyorsun. Yarın bir gün marka property adını(örnekteki) değiştirmek istersem tek tek her sınıfta değil tek bir yerde güncellemek kolaylıktır. 

👉 ! Polimorfizm de kalıtımın bir soncuudur. 

✨ Bir Programcı Açısından Kalıtım Nedir ? ✨

OOP'de kalıtım özünde nesnelerin birbirlerinden türemesini sağlayan bir özelliktir. Bu özellik yanında da bir çok özellik ve stratejik yapılanma gerektirmektedir(virtual, polimorfizm, abstraction ...). Bu eğitim srüecinde OOP'deki kalıtımı ve kalıtımın getirisi olan tüm stratejik yapılanmları tam teferruatlı ele alacağız.  

✨ C# Programlama Dilinde Hangi Yapılar Kalıtım Alabilirler ? ✨

👉 ! C# programlama dilinde kaltıım sınıflara özel bir niteliktir. Yani bir sınıf sadece bir sınıftan kaltıım alabilir. 

👉 ! Abstract class, inheritanceden kalıtım almaz onların adı başkadır(implementasyon). 

👉 ! Abstract class (Soyut sınıf): Bir sınıf, abstract class'tan "inherit" edilir veya "kalıtım alır". Inheritance (Kalıtım)

👉 ! Inheritance (Kalıtım) : Bir sınıf, bir interface'i "implement" eder veya "uygular". Implementation (Uygulama)

👉 ! Nesne yönelimli programlamada, bir sınıf abstract class'tan kalıtım alırken (inheritance), interface'leri ise uygular (implementation); bu iki kavram, sınıfların farklı yapılardan özellikler ve davranışlar edinme yöntemlerini belirtir ve her biri kendi amacına hizmet eder.

- Peki recordlar için özünde sınıf demiştik, bunlar kaltıım alabiliyor mu ?
Ever recordlar da kalıtım alabilirler fakat sadece kendi aralarında. Kalıtım alabildikleri istisnai tek sınıf ise ileride göreceğimiz object sınıfıdır.
Recorda class üzerinden kalıtım veremezsin. Sadece kendi aralarında kalıtım alıp verebilirler. Object ise kalıtımda önemli rol oynayan özel bir sınıftır. 

👉 ! Kalıtım sınıflarda uygulanır. 

👋 2 - C# da Kalıtım Nasıl Alınır - : Operatorü ?

C# da iki sınıf arasında kalıtımsal ilişki kurabilmek için : operatorü kullanılmaktadır. 
Her gördüğün : kalıtım demek değildir. 
Kalıtımsal tüm ilişkiler : operatorü ile sağlanır, abstarct interfacedekilerde.

![16-5](https://github.com/user-attachments/assets/97a7dfbf-081b-42b2-a764-a8d4799c5612)

Görselde, : ile oper bir şeyden kalıtım alacak dedik. Soldaki sağdakinden kalıtım alsın dedik. Artık compiler seviyesinde araba sınıfındaki erişilebilir propertyler opele aktarılmış oldu. 

![16-6](https://github.com/user-attachments/assets/efe119fe-acca-40bc-a37a-39fb75a4f7ec)

Görselde, : operatorü sadece classın modeli üzerinde kullanabilirsin. 

![16-7](https://github.com/user-attachments/assets/5c94c669-79ff-4938-90c2-83a215faf38f)

Görselde, public aktarılır, private aktarılmaz. 

👉 ! Kalıtım, operasyonel olarak gerçekleştirildikten sonra compiler seviyesinde member aktarımı sağlanır. Yani artık opel sınıfından nesne ürettiğimizde içerisinde marka ve model propertyleri kalıtımsal olarak aktarıldığı için erişilebilir olacaktır. 

![16-8](https://github.com/user-attachments/assets/e689c22d-26ed-4073-801c-d806bf257b2f)

Görselde, muhasebecideki Adi, kaltıım aldığı için Personel sınıfından gelmiştir.

👋 17 Inheritance - Kalıtım Nedir ?

👋 3 - Base Class ve Derived Class Nedir ?

Kalıtımsal ilişkide olan iki sınıf arasında kalıtım veren sınıfa base class yada parent class, kalıtım alan sınıfa ise derived class yada child class denir. 

![17-1](https://github.com/user-attachments/assets/93d34ab2-475e-470a-b63d-70ebaf0853e2)

Görselde, tüm atalar tüm torunların base classı mı yani, a b'nin base classıdır peki bi yandan b'nin bi yandan c'nin de base classı mıdır? Hayır değildir. c'nin base classı b'dir ama a değildir. Peki neden ? Unutmayın bir sınıfın sadece tek bir base classı olabilir. Direkt türediği sınıftır base class, ataları değildir. d ve a arasında dolaylı da olsa bir ilişki vardır.

👉 ! Base dediğimiz kavram direkt birebir kalıtım aldığımız sınıftır. Yani bir sınıfın base classı direkt türediği sınıftır. Fakat atalarındaki tüm sınıflar base classı değildir.

Peki bir classın birden fazla drived classı olabilir mi ? Evet olabilir, şöyle düşün, benim bir babam var ve babamın birden çok kızı var.

👉 ! Bir class hem drived hem de base class olabiliyor. 
👉 ! Bir sınıfın drived classları bizzat kendisinden türeyen olacaktır.

✨ Kalıtımın Altın Kuralı ✨

Bir classın sadece bir base classı olur dedik. Bunun nedeni, C# programlama dilinde bir classın sadece tek bir classtan türetilmesine izin verilmektedir. Aynı anda birden fazla classtan türeme işlemi gerçekleştirilemez. Dikey boyutta büyükbaba baba oğul şeklinde türetebilirsin ama yatay boyutta türetemezsin. Bu durum yatayda türeyememe, belirli problemlerden dolayı engellenmiştir. 

👉 ! Bir sınıfın birden fazla yatay düzlemde sınıftan kalıtım alabilmesine çoklu kalıtım denmektedir. İşte bu çoklu kalıtım yaşanan birçok problemden dolayı engellenmiştir. Java ve C# çoklu kalıtıma izin vermez ama veren başka diller vardır.

👉 ! class Y : X, Y, Z, T{...} şeklinde kullanım yoktur. İleride bu şekilde birden fazla kalıtım tanımlamasının yapıldığını göreceksiniz. Fakat orada Z ve T bir sınıf olmayacaktır. 

✨ Kalıtımda Nesne Üretim Sırası ✨

👉 ! Bir sınıftan nesne üretimi yapılırken kalıtım aldığı üst sınıflar varsa eğer önce o sınıflardan SIRAYLA nesne üretilecektir. Yazılım, sen üretmesende compiler seviyesinde ilgili kalıtım veren sınıftan bir nesne üretecektir. Hatta öncelikle o sınıftan nesne üretilecek sonra kalıtım alan sınıftan nesne üretilecektir. Buradaki sıralama hiyerarşik bir şekilde olacaktır.

![17-2](https://github.com/user-attachments/assets/a7189a38-8519-49b6-a3ba-d8aeb6088470)

Görselde, c'den nesne üretilmeden önce b'ye, b'den önce base classı olan a'dan nesne üretilir. Sonra b sonra da c'den nesne üretilir. new c ile sen bir tane nesne üretiiğini düşünürken heapte 3 tane nesne olacaktır. Burada base classın var mı şeklinde sorarak ilerliyoruz.

![17-3](https://github.com/user-attachments/assets/71a4b633-f7de-4d1c-88df-5c3ea95ea462)

Görselde, d'den nesne üretmek istediğimizde diğerlerinden(atalarından) nesne üretimini constructor ile gösterdik. Yani buradan anlaşılıyor ki, nir sınıftan nesne üretilirken siz 1 adet nesne ürettiğinizi düşünsenizde kalıtımsal açıdan birden fazla nesne üretimi gerçekleşebilmektedir.

✨ Bir Sınıftan Base Class Constructorına Ulaşım ✨

Madem ki, herhangi bir sınıftan nesne üretimi gerçekleştirirken öncelikle base classından nesne üretiliyor, bu demektir ki önce base classın constructorı tetikleniyor. Haliyle bizler nesne üretimi esnasında base classta üretilecek olan nesnenin istediğimiz constructorlarını tetikleyebilmek, varsa parametrelerine bu değerleri verebilmeliyiz. İşte bunun için base keywordü kullanmaktayız. Benden nesne üretilirken base classtaki hangi constructorın tetiklenmesini istiyorsam onu benim üzerimden belirleyebilmeliyim. Yani drived class üzerinden bunu belirleyebilmeliyim. 

Base classın iki amacı vardır. 
 - Base classın constructorlarına erişimi sağlar.
 - This gibi, ...(sonra açıklanacak)

![17-4](https://github.com/user-attachments/assets/3924a14e-a6c9-40af-a4b3-ebde0a864f25)

Görselde, base ile basedeki sınıfın constructorlarına geçiş yapmayı sağlar, this olsaydı o da o sınıfın içindeki constructorlar arasında geçişi sağlayacaktı.

![17-5](https://github.com/user-attachments/assets/a4520330-cc9b-43b7-a9f4-74ee79ae4edf)

Görselde, eğer ki base classın constructorı sadece parametre alan constructor ise drived classlarda o constructora bir değer göndermek zorundayız. Bunu da base keywordü ile yaparız. 

![17-6](https://github.com/user-attachments/assets/3a3e249b-f1ab-45cf-8987-9ce848b64c67)

Görselde, base constructorda parametreli ve parametresiz birden fazla constructor olsaydı o zaman drived classta base keywordünü kullanmaya gerek yoktu çünkü default olarak basedeki boş olan constructora gidecekti. Eğer ki base classta boş parametreli bir constrcutor varsa drived classta base ile bir bildirimde bulunmak zorunda değiliz. Çünkü varsayılan olarak kalıtımsal durumda base classtaki boş olan parametreli constructor tetiklenir. 
Base classta 4 farklı constructor olsaydı ve bunu kalıtım alan bir sınıftan bir nesne oluşturmak isteseydik, nesne oluşturacağımız sınıfın constructorından base keywordünü kullandığımızda o classın(atası olan base classın yani) base classın constructorlarını bize getirir. 

![17-7](https://github.com/user-attachments/assets/078aea8a-3bdf-452a-be01-b33d08a8f815)

Görselde, MyClass'ta dört farklı constructor var ve MyClass2'den nesne oluşturulmak isteniyor. Bu durumda MyClass2'nin constructorında kullanılan base keywordü ile MyClass'ın constructorlarına erişim sağlarız. Bir classın constructorının yanında : base() keywordü kullanırsak eğer o classın base classının tüm constructorlarını bize getirecektir. Haliyle ilgili sınıftan bir nesne üretilirken base classtan nesne üretimi esnasında hangi constructorın tetiklendiğini bu şekilde belirleyebiliriz. 

✨ Base Keywordü ve This Keywordü ✨

![17-8](https://github.com/user-attachments/assets/95e764ed-c458-4a3c-8d47-2eb2bf6c2b1b)

👉 ! This, bir sınıftaki constructorlar arasında geçiş yapmamızı sağlar. Base, bir sınıfın base classının constructorlarıdnan hangisinin tetikleneceğini belirlememizi ve varsa paramterlerinin değerlerinin drived classtan verilmesini sağlar.  
Ayrıca nasıl ki, ilgili sınıfta o anki nesnenin memberlarına erişebilmemizi sağlıyor, aynı şekilde base de, base classtaki memberlara erişebilmemizi sağlamaktadır.

![17-9](https://github.com/user-attachments/assets/eb68eab1-d05c-4f3f-92a2-84675ff96600)

Görselde, base classta erişilebilir olmayan memberlar base keywordü ile erişilemez. Dolayısıyla base keywordü ile a fieldına ve Y metoduna erişim sağlanmaz. Base classta erişilebilir olmayanlar zaten kalıtımsal olarak aktarılamaz.  

![17-10](https://github.com/user-attachments/assets/961a55a9-77a6-4407-911f-a0bc1c0756dd)

Görselde, this ile B sınıfındaki b fieldına da erişi sağladık çünkü kalıtım oldu. Aynı şekilde MyProperty'e de erişebildik. a fieldına erişim yok çünkü private tanımlanmıştır. 

![17-11](https://github.com/user-attachments/assets/407b93d0-ccd5-411c-afaf-7f69a39d80bf)

Görselde, base dediğimizde ise sadece base classtaki erişilebilir olanlara ulaşıyoruz. 

![17-12](https://github.com/user-attachments/assets/2c918050-616e-4515-b622-79b63ec45692)

Görselde, başına base koymadan kullanırsan da kalıtım olduğu için hatasız kullanabilirsin. Aynı şekilde this.c de diyebilirsin yada direkt c diyebilirsin. Direkt c dersen arka planda zaten başına this konuluyor. 
