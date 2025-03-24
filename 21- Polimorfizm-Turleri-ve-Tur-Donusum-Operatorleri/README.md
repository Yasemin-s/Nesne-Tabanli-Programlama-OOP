👋 1 - Polimorfizm Türleri ve Tür Dönüşüm Operatörleri (Bölüm 2) (7. ve 8. görseller doğru yerde olmayabilir.)

Bir nesnenin birden fazla farklı türdeki referans tarafından işaretlenebilmesine polimorfizm denir.

✨ Polimorfizm Türleri ✨



Dinamik ve statik polimorfizm bilmek genel kültürümüzü arttıracak ama teknik boyutta bize çok fazla bir şey kazandırmayacaktır. Nesneleri referans ederken buradaki tür dönüşümlerini ne şekilde yapabildiğimizi inceleyeceğiz.

✨ Statik Polimorfizm ✨



Static, ileride göreceğimiz bir kavramdır. Polimorfizme static ismi verilmiş yani bir duruma statik polimorfizm denir. Statik polimorfizm, derleme zamanında sergilenen polimorfizmdir. Hangi fonksiyonun çağrılacağına derleme zamanında karar verilir.

C#'da statik polimorfizm deyince aklımıza metot overloading terimi gelmelidir. Metot overloading: aynı isimde birbirinden farklı imzalara sahip olan metotların tanımlanmasıdır. Ya da başka bir deyişle bir isme birden fazla farklı türde metot yüklemektir. Haliyle burada bir metodun birden fazla formunun olması polimorfizmken, bunlardan kullanılacak olanın derleme zamanında bilinmesi statik polimorfizm olarak nitelendirilir.

![21-1](https://github.com/user-attachments/assets/c3ba7a98-bfef-409d-84f6-ca2fb5a0289e)

Burada kodu yazdığım anda hangi overload'u/fonksiyonu kullanacağım biliniyor. 2 parametreli olacağı burada biliniyor. Overload edilmiş metotlarda derleme zamanında kullanılması durumuna statik polimorfizm denir.

✨ Dinamik Polimorfizm ✨



Çalışma zamanında sergilenen polimorfizmdir. Yani hangi fonksiyonun çalışacağına run time'da karar verilir. Statik polimorfizmde hangi fonksiyonun çalışacağına biz derleme zamanında karar veriyoruz. Ama dinamik çok biçimlilikte hangi fonksiyonun çalışacağına runtime'da yani o anda çalışma sürecinde karar verilir.

C#'da dinamik polimorfizm deyince akla metot override gelmektedir. Base class'tan gelen metotları sen eziyorsan eğer o ezme durumları runtime'da gerçekleşecektir.

![21-2](https://github.com/user-attachments/assets/69a9572a-f831-4882-9b73-906605fac30a)

Burada Arac t = new Taksi() dersek Arac sınıfındaki mi yoksa Taksi sınıfındaki t.calistir çalışacak runtime'da karar verilecek. Haliyle bu durum dinamik polimorfizmdir.

Base class'larda tanımlanmış olan herhangi bir virtual/sanal yapılanmanın derived class'ta ezilip ezilmeme durumu/yani override edilip edilmediği durumu çalışma zamanında karar verilir.

Taksi t2 = new Taksi(); t.calistir dediğimde buradaki calistir Taksi'den gelecekti işte bunun kararı runtime'da verilir. Metot override, base class'ta virtual olarak işaretlenmiş metotların derived class'ta override edilerek ezilmesi/yeniden yazılması işlemidir. Haliyle burada aynı isimde birden fazla forma sahip fonksiyonun olması polimorfizmken bunlardan hangisinin kullanılacağının çalışma zamanında bilinmesi dinamik polimorfizm olarak nitelendirilir.

✨ Polimorfizm Durumlarında Tür Dönüşümleri ✨ 



Polimorfizm, birden fazla nesneyi farklı türdeki nesneleri tek bir referans üzerinden işaretleyebiliyorduk ya da bir nesneyi birden fazla referansla işaretleyebiliyoruz.

Polimorfizm, OOP'de bir nesnenin kalıtımsal açıdan ataları olan referanslar tarafından işaretlenebilmesidir. Haliyle, ilgili nesne, bu ataları olan referans türlerine göre dönüştürülebilmektedir.

![21-3](https://github.com/user-attachments/assets/89195cff-ec62-4c81-9461-78631b32d985)

![21-4](https://github.com/user-attachments/assets/3bd29382-eda6-43ac-a7d6-9425c54c4db0)

Burada A, C'nin atası olduğundan dolayı C'yi referans edebilir. A referansı ile işaretlenmiş olan C nesnesi ihtiyaç durumunda B referansı ile de işaretlenebilecek şekilde dönüştürülebilir. Ya da C referansı ile de işaretlenebilecek şekilde dönüştürülebilir. Haliyle ihtiyaç doğrultusunda A referansı üzerinden diğer kalıtımsal ilişkide olduğu referanslara yahut kendi referansına dönüştürülebilir.

C c = (C)a; bizim cast operatörümüz vardı. A referansı C'den büyük yani C'nin atası ve C'yi referans ettiğinden dolayı A referansına ben cast operatörüyle içindeki C nesnesini bana ver dediğimde sağ taraf artık kesinlikle C nesnesine dönüştürülmüş bir tür olduğundan dolayı bunu da C nesnesi ile işaretleyebiliyorum.

Burada C c = a yapamam, polimorfizmde alt türler (C), üst türün (A) referansını karşılayamaz. Haliyle görselde A referansı A türünde olduğu için, içinde her ne kadar C nesnesini barındırıyor olsa da bu şekilde tanımlama yapamazsın. Bu işlem için cast operatörü kullanılmalıdır. Bu durumun tersi de geçerlidir. Yani ilgili nesne kendi türünden kalıtımsal olarak ataları olan diğer türlere cast edilebilir.

![21-5](https://github.com/user-attachments/assets/85b21381-9e29-4624-82df-c00d3bdb8178)

A referansı C'nin atası olduğu için direkt karşılayabilir.

Dikkat edersen eğer polimorfizm durumlarında kalıtımsal açıdan üst bir referans ile işaretlenebilmiş herhangi bir nesneyi kendi türünden işaretleyebilmek için cast operatörünü kullanarak object türüne özel olan unboxing'e benzer bir hamlede bulunmuş oluyoruz.

Object zaten bir class bir nesne/obje. Haliyle bu obje durumunda da tür dönüşümü yaparken de özünde biz polimorfizmde bu anlatılan yapılanma kullanılıyor. Sen bunu object'te yapıyorsan boxing unboxing diyorsun. Bunun dışında başka bir yerde yapıyorsan bir şey demiyorsun.

Buradan anlıyoruz ki, object türünde gerçekleştirilen unboxing durumu esnasında object türü ile gerçekleştirilebilen polimorfizmin bir sonucudur.

Object bütün türlerin atası olduğundan dolayı, buradaki A gibi, altındaki herhangi bir türü kendi türünde elde edebilmek için cast operatörünü kullanıyorduk. Haliyle A'nın altındaki C'yi elde edebilmek için A referansı içinden elde edebilmek için bu sefer de A'ya cast operatörü ile bildirimde bulunuyoruz. Yani aynı işlemi yapmış oluyoruz.

! Object'e bir değer atma işlemine boxing derken, object'in içinden bir değeri kendi türünden elde etmeye unboxing deriz.

![21-6](https://github.com/user-attachments/assets/13ceedb5-c2cd-4e17-a533-2cceb144743f)

Burada nasıl object tüm türlerin atasıysa tüm türleri karşılayabiliyorsa, A - B - C içinde A, B ve C'nin atasıdır.

![21-7](https://github.com/user-attachments/assets/a10c3bdb-587a-4243-9b67-833c666e02e7)

A a = new C(), A türüne C'yi kutulamış oluyoruz, boxing diyebiliriz. Benzer mantıkla A kutusundaki C nesnesini C olarak almak istiyorsak buna da unboxing diyebiliriz. A kutusunun içindeki A'yı C nesnesi olarak ver dersek C c = (C)a; şeklinde yaparız.

Boxing unboxing dediğimiz kavram özünde OOP'deki nesnelerin davranışı ile alakalı bir durumdu. Bu polimorfizm olmadığı sürece bir anlam ifade etmez. Bu yapılanma OOP'de tüm nesneler arasındaki geçişlerde sağlanabilir.

Boxing ve unboxing'i şu şekilde özetleyenler vardır: Primitive türleri/stack'teki değerleri heap'e alabilmek için (nesneye çevirmek) yapılan bir stratejidir, uygulamadır.

✨ Polimorfizm Durumlarında Tür Dönüşümü Operatörleri ✨ 



Polimorfizm durumlarında tür dönüşümü gerçekleştirebilmek için cast ya da as operatörleri kullanılabilir.

✨ Cast Operatörü ✨ 



Üst türden alt türe kalıtımsal ilişkide dönüşüm sağlar. Yani A'dan, B ya da C'ye dönüşüm yapacaksan ya da benzer mantıkla object'ten int'e string'e yani object'in altındaki herhangi bir türe dönüşüm yapacaksan cast operatörünü kullanabilirsin.

![21-8](https://github.com/user-attachments/assets/d8d8a6ef-426c-4550-aad0-142c54276f47)

A a = new C(), A C'yi kalıtımsal hiyerarşide sağlayabilir. Yani atası olduğundan dolayı A referansı ile C nesnesini çok rahat bir şekilde tutabiliyoruz. Tuttuğumuzdan dolayı C c = (C)a, A referansı içindeki C nesnesini C referansıyla tekrardan elde edebilmek için ne yapıyorum? A'nın içinden bunu cast operatörü ile çekiyorum/cast etmiş oluyorum.

Şimdi bu operatörün de kendine göre kritikleri var. Eğer ki, kalıtımsal ilişki olmayan herhangi bir türe dönüştürülmeye çalışılırsa derleyici hatası verecektir. Gelin bunu şu şekilde örneklendirelim:

![21-9](https://github.com/user-attachments/assets/52c2084a-f4bb-4946-b21c-c2ba12c762f4)

A referansı içindeki C'yi, ben C referansına direkt A'ya cast ederek bu şekilde alabiliyorum. Burada compiler hata vermez. Çünkü A referansının türü ne A, A zaten C'nin atası olduğundan dolayı ve derleyici bunu bildiğinden dolayı herhangi bir derleyici hatası vermiyor. Ve bu konsepte izin veriyor. Yani evet C referansı A'nın bir türünü olduğundan dolayı, yani A türü C'nin bir atası olduğundan dolayı A referansı ile herhangi bir C nesnesi işaretlenebilir haliyle A referansında da o A referansı ile işaretlenme ihtimali olan C nesnesini ben C'ye cast edip alabilirim. Derleyici bunu bildiğinden dolayı herhangi bir derleyici hatası vermiyor. Çünkü arada herhangi bir hiyerarşik ilişki var.

![21-10](https://github.com/user-attachments/assets/0b5b4433-d6f5-455b-ac2c-71942d92187f)

Peki ben A'nın içinden örnek veriyorum D nesnesini almaya çalışsaydım. Normalde bu mümkün değil direkt compiler hata verir. Çünkü zaten D, A'nın doğrudan ya da dolaylı olarak torunu değil. Aralarında kalıtımsal bir ilişki yok. Sen zaten üstlerde A referansıyla D nesnesini zaten karşılayamazsın. A referansının içinden kesinlikle sana D nesnesi gelemez. Çünkü aralarında hiyerarşik kalıtımsal ilişki yok. Yani kalıtımsal ilişki olmadığı takdirde cast operatörü hata verecektir.

Bir örnek daha veriyorum:
object o = 123
int i = (int)o burada hata vermez. Çünkü int, object'in bir torunudur. Object'ten türediği için doğrudan ya da dolaylı haliyle bu durum gerçekleşebilir. Object türündeki o referansı içinde 123 değeri olabilir. Bu olabilme ihtimaline istinaden cast işleminde ((int)o kısmında) compiler hata vermez. Bu dönüşümü dönüştürebiliyorsa dönüştürür, dönüştüremiyorsa neden dönüştüremiyor buna birazdan bakacağız.

Eğer kalıtımsal ilişkide olup fiziksel nesnenin hiyerarşik altında olan bir türe dönüştürülmeye çalışılırsa runtime hatası verecektir.

![21-11](https://github.com/user-attachments/assets/cb153cfc-7b06-436d-aeeb-ae1a5a6c47d8)

class D : C{} olsaydı dolaylı olarak A'dan da kalıtım almış olacaktı. D d = (D)a hatası ortadan kalktı. Compiler biliyor ki A referansı ile D referansı ilişkili yani A, D'ye miras vermiş. Yani A referansının içinde A türünden olan, A referansının içinde D türünde olan bir nesne olabilir. Haliyle D d = (D)a konseptine izin veriyor compiler. Ama dikkat A referansının içinde ne var C türünden bir nesne var. Şimdi C türünden olan bir nesneyi ben D türünden bir referansla ver dediğimde derleme sürecinde bana bunun hatasını vermez ama ben bu kodu derleyip runtime ettiğim zaman hata verir. Runtime'da diyecek ki A referansı içindeki nesne D değil, haliyle D ile işaretlenebilir bir referans da değil. Çünkü D kalıtımsal olarak C'nin altında olduğu için sen bu C nesnesini D ile işaretleyemeyeceğinden dolayı compiler hata verir. Yani bu A referansının işaretlediği C nesnesini ben D ile işaretleyip sana gönderemiyorum diyor ve runtime'da patlıyor.

Bu durumu çizerek anlatmak gerekirse 

![21-12](https://github.com/user-attachments/assets/275e0b39-f290-4a82-90b1-409955376965)

Şimdi C nesnesi, A türünde a referansıyla işaretlenmiştir. Şimdi C, A’dan miras alan bir nesne olduğu için a ile işaretlenebiliyor. Biz diyoruz ki, (D d = (D)a koduyla) a referansının işaretlemiş olduğu C nesnesini sen bana D ile işaretleyip getir/yani D olarak getir/D ile işaretlenebilir olarak getir. Ama polimorfizm kuralları gereği neydi? Bir nesneyi kendisi ve üstündeki, hiyerarşik olarak üstlerindeki nesneler, üstlerdeki sınıfların referansları işaretleyebilir. Dolayısıyla D referansı C’nin hiyerarşik olarak altında olduğu için sen C’yi D ile işaretleyemezsin. Haliyle burada D türündeki oluşturulmuş olan d referansı ile C’yi işaretleyemezsin. Bu nedenle a’nın içindeki C türünden olan bu nesneyi D’ye cast etsen dahi runtime’da hata alacaksın.

D d = (D)a, D türü A’dan kalıtım almıyorsa eğer, hiyerarşide yer edemeyeceğinden dolayı bu durumda derleyici hata verecektir. Yok eğer kalıtımsal olarak C’nin altında A’nın torunu ise, fiziksel C nesnesinin kendisinden küçük olan D referansıyla işaretlenmesi, Polimorfizm mantığı gereği mümkün olamayacağı için runtime hatası verecektir. Yani bir derleyici sürecinde hata verme durumu var bir de runtime sürecinde hata verme durumu var. Her ikisini de incelemiş olduk.

Tersine olarak, kalıtımsal ilişkide alt türden üst türe cast operatörü ile de bir dönüşüm sağlanmaktadır. 

![21-13](https://github.com/user-attachments/assets/9ec71fa4-7c1a-4be6-933c-9ef80167885c)

C c = new C(); burada c referansının içinde C nesnesi var. C nesnesini direkt A referansına bu şekilde gönderebilirim (A a = c). Bu durum bilinçsiz bir dönüşüm sağlayacak ve direkt ilgili C nesnesini A referansı ile işaretleyecektir. Benzer mantıkla A türünde a2 referansıyla (A)c ile [C'nin içindekini A'ya cast et, sonra A'ya bir daha işaretle, ama biz diğerini (A a = c) kullanacağız buna gerek yok].

C c = new C();
A a = (A)c; burada da kalıtımsal ilişki gerekmekte, aksi takdirde derleyici hatası ile karşılaşılabilmektedir. C'yi cast ile ya da castsiz A'ya atayabilmem için C'nin A'nın bir torunu olması gerekiyor.

✨ As operatörü ✨ 

Cast gibi kalıtımsal ilişki olan türler arasında referans dönüşümü yapabilmemizi sağlayan operatördür. 

![21-14](https://github.com/user-attachments/assets/e15ccc28-baf6-4846-b482-476ab40222db)

A a = new C(); burada a referansı ile gene A'nın torunu olan C nesnesini işaretlediğimi varsayıyorum. Normalde ben A'nın içinden C'yi C olarak elde etmek istiyorsam, cast operatörünü kullanıyorduk. Artık cast operatörünü kullanmıyoruz. C c = a as C; ile A'nın içindeki nesneyi bana C türünde ver diyorsun. Haliyle (a as C) kısmı sana C türünde nesne dönecektir. Bu yüzden C türünde c referansı ile C c şeklinde tutabilirsin/işaretleyebilirsin.

Dönüşüm esnasında hiyerarşik olarak tüm türler dönüşüm sağlar (burada A, B, C hiyerarşisini düşünürsen, yani polimorfizm kuralı gereği kalıtım hiyerarşisinde cast operatörü ile ne yapıyorsan as operatörü ile de aynısını yaparsın). Lakin kalıtımsal ilişkide olmayan türlerde derleyici hatası verecektir.

Ya da kalıtımsal ilişkide olup fiziksel nesnenin türünden daha alt hiyerarşide olan nesnelere dönüştürülmeye çalışıldığında polimorfizm mantığı gereği ilgili referans o nesneyi karşılayamayacağından runtime hatası vermeyecek! Geriye null (değersiz) dönecektir.

![21-14](https://github.com/user-attachments/assets/ba3374c8-55d6-426b-9da0-bc1eed3e96ab)

Şimdi A referansı içindeki C nesnesini cast operatörü ile D olarak elde etmeye çalışsaydım, zaten bu bana runtime'da hata verecekti. Çünkü C nesnesini D ile işaretleyemiyorduk. Ama ben bunu cast operatörü ile değil de as operatörü ile sağlarsam, bu sefer runtime'da hata vermeyecektir. Peki ne olacak? Hani A'nın içindeki nesne D ile işaretlenemiyordu. D d = a as D kısmında null dönecektir. Birinde hata veriyor, diğerinde null dönüyor. Hata durumlarında try-catch yapılanmalarını kullanabilirsiniz. Null durumlarında da gelen değerin null olup olmadığını kontrol etmeniz gerekiyor.

As operatörü uygulamayı patlatmaz, ya null döner ya da dönüşüm sağlayıp ne dönüşüm yaptıysa onu döndürür.

Cast operatörünün as operatöründen farkı: Biri dönüşüm sağlayamıyorsa hata fırlatır (cast), diğeri null döner (as).

✨ Is operatörü ✨ 

Burada aslında bir tür dönüşümü yok. Ama tür ile ilgili bilgi edinmemizi sağlayan bir operatördür. Is operatörü, kalıtımsal ilişkiye sahip nesnelerin polimorfizm özelliğine nazaran fiziksel olarak hangi türde olduğunu veren bir operatördür. Yani sen bir referansın içinden hangi türden nesneyi işaretlediğini merak ediyorsan, is operatörünü kullan.

![21-15](https://github.com/user-attachments/assets/d28245b7-021e-430e-8ab9-ac8d62f115a1)

A referansı ile C türünden bir nesneyi işaretliyorsan, is ile soruyorsun (a is B ile a, B türünden bir nesneyi mi işaretliyor vs.). Sonucunda true/false döner. Fotografta sadece C nesnesinin true, diğerlerinin false olmasını beklersiniz. Halbuki burada aklına direkt şu gelmeli: Kalıtımsal hiyerarşide nesne üretim sırası vardı. 

![21-16](https://github.com/user-attachments/assets/7d4131c7-b854-45db-bad4-153b906007cd)


C sınıfından nesne oluşturduğumda compiler der ki, C'ye gidip seni bir base class'ım var mı diye sorar. Ona da aynı şeyi yapar, en üst class'a gidene kadar ve en üstteki atadan ilk nesneyi oluşturur ve sırasıyla en son talep edilen nesneye doğru gelir (C sınıfına, yani önce A, sonra B, en son C nesnesi oluşur).

![21-15](https://github.com/user-attachments/assets/bc7ef5a5-66d0-4a4a-a019-ed4049cdb6a0)

için, bu yüzden A, B ve C için true döndü. Haliyle sen buradaki A referansıyla sen B'ye de A'ya da erişebiliyorsun. Erişebildiğin için A referansı özünde bir B'dir, bir C'dir, bir A'dır ama bir D değildir. Çünkü kalıtımsal hiyerarşide yok

![21-16](https://github.com/user-attachments/assets/f3a6ff98-d813-4336-a3d2-6137e5b00325)

Diyelim ki kalıtımsal ilişkide var, 

![21-17](https://github.com/user-attachments/assets/28ca160d-8813-4a1e-a65c-0bb45c6b9e16)

için), böyle bir durumda A yine bir D değildir. Çünkü sen C'den bir nesne oluşturuyorsan, atalardan C'ye kadar gelecektir. Yani D yine false olacaktır, D oluşturulmayacaktır. Çünkü sen C'ye kadar istemişsin, C'ye kadar oluşturur (A a = new C()). D'yi isteseydin (A a = new D() olsaydı), A, B, C, D hepsi oluşup true dönecekti.

Haliyle dikkat edilirse, fiziksel nesnenin kalıtım hiyerarşisine uygun olan türlere true, olmayan türlere ise false sonucu dönecektir. Kalıtımsal ilişki olmayan sınıflara yapılacak kontrollerde de beklenildiği gibi false değeri dönecektir. Hiyerarşik olarak ilgili nesnenin altında kalıyorsa, yine false dönecektir.

Haliyle çok biçimlilik (polimorfizm) uygulanmış bir nesnenin ihtiyaç doğrultusunda (uygun olan) farklı bir türe dönüştürülebilmesi için, işi garantiye alabilmek adına önce is kontrolü (tür kontrolü), ardından cast ya da as operasyonu sağlanması kafidir. 

![21-18](https://github.com/user-attachments/assets/54ca4152-3ecb-4c82-a3e6-9e51f5ded52f)

A bir D midir? Eğer D ise, D'ye cast et. Burada D d = (D)a kısmı tetikleniyorsa, runtime'da hata vermeyecektir. Zaten A eğer D ise, bu kısm/kod (D d = (D)a) çalışacaktır.
