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
