👋 1- Nesne Tabanlı Programlama - Class Members - Field - Property - Encapsulation - Method

OOP' de temel/esas yapılanma objeydi. Objenin fıtratı classtır. Yani bir nesne ortaya koymak için öncelikle o nesneyi modellemek gerekiyor. Modellemeyi de class ile yapıyoruz. Bu derste bu nesnseyi oluşturmamızı sağlayan model olan classın içinde neler tanımlayabiliyoruz bunları inceleyeceğiz. 
Classın içine koyabileceğimiz yapılar classın elemanları olarak nitelendirilir. Terminolojide  class memberı oalrak geçer. Member, üye demektir.

Class içinde,
Field : Bu classtan üretilen nesne üzerinde değer tutmamızı sağlar.
Property : Bu fieldlar üzerinde kontrollü bir şekilde değerleri dışarı açmamızı ve bu dışarıdan gelecek olan değerleri de kontrollü bir şekilde fieldlara atamamızı sağlar.
Method : Nesne üzerinde prosedürel işlemler yapmamızı sağlayan küçük kod parçacıklarını da sınıf içinde tanımlayabiliyoruz.
Indexer : Aynen dizilerde yada koleksiyonlarda olduğu gibi kendi nesnelerimize indexer operatorü kazandıran ve belirli işlemlerde kullanmamızı sağlayan bir özelliktir. 

👉 ! Sınıfın elemanlarında constructor, deconstructor, static constructor da var. Bu özellikler özelleştirilmiş/özel memberladır. Bunlar sen tanımlasan da tanımlamasan da bir classın içnde var olan özel yapılanmalardır. Ama property, field, method dediğimiz yapılanmalar sen tanımladığın sürece var olan nesne içinde vasrayılan olarak olmayan yapılardır. 

👋 2- Field
Nesne içinde veri depoladığımız/tuttuğumuz alanlardır. Bir class modelim var ve bu class modelinden üretilen binlerce nesnem var. Bu nesnelerin her biri kendi içinde kendine ait alanlara sahiptir. İşte bu alanlara field denir. 

Field, class içindeki tanımlanmış değişkenlerdir. Fieldlar herhangi bir türden olabilir. Fieldlar, türüne özgü varsayılan/default değeri alırlar. 

Bir class içinde field tanımlamak istersem class scopeları içine direkt değişkenleri tanımlayabilirim. 

![3-1](https://github.com/user-attachments/assets/5b143d3a-9281-4cc6-ad17-605cbb75b670)

Bu classtan oluşturulan nesnede direkt olarak a fieldı olacaktır ve int türünden bir değer atayabiliyor olacaksın. 

👉 ! Field kelimesi sadece class içindeki değişkenler için kullanılır. Main içinde yada metot içinde değişken tanımlaması varsa değişken diyeceksin, field değil. 

MyClass için nesne oluşturmak istiyorsam, new MyClass() demek yeterlidir. 

![3-2](https://github.com/user-attachments/assets/a050a52c-8f4e-4f8c-a028-911215c27e50)

Oluşan MyClass nesnesini MyClass türünden m1 refernası ile işaretleyeceğim. new MyClass() heap e nesneyi koyacak. m1 referansıyla stackte olup, heapteki nesneyi işaret edecek. Dolayısıyla m1. dediğimde içinde hangi elemanlar varsa ulaşabiliyor olacağım. Ayrıca burada m1. ile a fieldına erişemedik, bunun nedeni access modifier dediğimiz erişim belirleyicisidir. a nın erişim belirleyicisi default olarak privatetır. Dışarısdan m1. ile a ya erişmek istersem a nın erişim belirleyicisini public yapmam gerekir. 

![3-3](https://github.com/user-attachments/assets/34e3f30c-c5e9-4988-91a4-90eadfd9f6ed)

m1. ile açılan pencerede de a nın erişilebilir olduğunu görebilirsin. 

👉 ! 

![3-4](https://github.com/user-attachments/assets/cf15d6c5-65d5-4377-96e0-aa89a6f2dab1)

Fieldlar tanımlanırken değer verilmezse stackte fiedlara varsayılan/default değerler atanır. 

👉 ! Türüne göre otomatik default değer atama işlemi sadece class içinde tanımlanan değişkenlerde/fieldlarda geçerlidir. Sen bu değişkeni main içinde yada metot içinde tanımlasaydın default değer atanmayacaktı. 

👋 3- Property
Nesne içinde özellik sağlar. Peki bu özellik sağlaması ne demek?
Property özünde bir metottur. Yani programatik/algoritmik kodlarımızı inşa ettiğimiz bir metottur. Fakat fiziksel olarak metottan farkı parametre almamakta ve içerisinde get set olmak üzere özelleştirilmiş iki adet blok bulunmaktadır.

![3-5](https://github.com/user-attachments/assets/12a0ebd8-2feb-4431-960d-9452b677edaf)

Normal metottan farkı, metotta parantez vardır ve parametre alabilir. Property de ise parantez yok ve parametre alamaz. Set bloğunda propertye değer atandığı zaman bu değeri set bloğunda yakalarız. Propertyin değeri okunmak istendiğinde de get bloğu tetiklenir/return edilir. 
Propertyin işlevsel açıdan metotlardan farkı yoktur. Fakat davranışsal olarak nesne üzerinde bir değer okuma ve değer atama işlemlerinde kullanılır. 

👉 ! Bir fieldın değerini okuma yada değer atama kısmında property devreye girer. 

👉 ! Derleyici, property'leri arka planda get ve set metotlarına dönüştürür.

👉 ! IL (Intermediate Language) Seviyesinde: Property'ler, get_PropertyName() ve set_PropertyName(value) şeklinde metotlara dönüşür.

👋 4- Property Ne Amaçla Kullanılır?

Biz yazılımcılar nesne içindeki fieldlara direk erişilmesini istemeyiz. Fieldlardaki veriyi kontrollü bir şekilde dışarıya açmak istiyoruz. benim cüzdanımdan para istersen direkt sen alma cüzdanı bana getir ben vereyim gibi düşün. İşte bu durumu propertyler sağlar. Tabi fieldlardaki değerleri göstermemek için fieldlarıdan dışarıdan erişilebilir olmasını engellemek gerekir, yani fieldları private olarak işaretlemek gereklidir. Kontrollü olarak function tanımlayıp verilir. Bu fonksiyonlara göndereceğim veriler de tamamen bana bağlı istersem hepsini istersem bir kısmını gönderirim yani benim kontrolümde. 

![3-6](https://github.com/user-attachments/assets/f71f848c-f7dc-41e8-a704-567b5d9524e7)

Cüzdan örneğinde senden 100 ₺ para istediler, sen dur getir cüzdanı ben veririm dedin. 100 ₺ değil 50 ₺ vermek istedin/verdin. Halbuki cüzdanında olan diğer 50 ₺ den onun haberi yok. Bunu bilemez, çünkü arada sen varsın senin kontrolün var. 

Bu dışarıdan erişilme mevzusunda C# metot yerine property getirmiş, evet metotla da bu işlemi gerçekleştirebilirsin ama biz property ile yaparak fark yaratalım demiş. Yani property yapıları özünde nesne içindeki fieldın dışarıya kontrollü açılmasını ve kontrollü bir şekilde dışarıdan değer almasını sağlayan yapılardır. İşte biz propertylerin bu işlevine encapsulation(kapsülleme/sarmalama) diyoruz. Benim fieldıma sen erişemezsin/okuyamazsın dememiz, property üzerinden erişebilirsin dememiz aslında o fieldı kapsüllememiz anlamına geliyor. 

👋 4- Encapsulation - Kapsülleme - Sarmalama

Encapsulation, bir nesne içindeki dataların(fieldlardaki veriler) dışarıya kontrollü bir şekilde açılması ve dışarıdan kontrollü bir şekilde veri almasıdır.

![3-7](https://github.com/user-attachments/assets/f019fb95-34bb-4259-bb6b-682595215196)

İşte bu şekilde fieldlardaki verilerin erişim kontrolünü yapmamız için geliştirilmiş olan yapılara property denir. Property kullanıyorsan encapsulation uyguluyorsun demektir. 

👋 5- Property İmzaları - Nasıl Oluşturulur?

Property yapısı oluşturabilmenin yapısal olarak birkaç farklı yolu/imzası vardır. Bunlar, 
fullproperty, 
prop, 
auto property initializer, 
ref readonly returns, 
computed(hesaplanmış) properties, 
expression-bodied property(readonly property), 
init-only properties ve init accessor C#9.0
eğer sen bir sınıf içine property koyacaksan burdaki imazları kullanarak yapabilirsin.

✨ Full Property ✨

En sade/temel property yapılanmasıdır. 
İçinde get ve set blokları tanımlanmalıdır.
Erişim_belirleyici geri_donus_tipi property_ismi şeklinde tanımlanır.

![3-8](https://github.com/user-attachments/assets/5e330abb-f518-4e8e-8562-ad2db6614f81)
Burada m1. dendiğinde erişilsin mi erişilmesinnmi bunu belirtmek için Erişim_belirleyici kullanılmıştır. Bu property hangi değeri alacak hangi değeri döndürecek bunu berlitmek için geri_donus_tipi yani bir nevi property_turu, ve property için isim bildirilecektir. 

Erişim belirleyici yapılanması kalıtım konusu altında incelenecektir.
Ayrıca full propertyde set bloğu tanımlanmazsa sadece okunabilir(readonly), get bloğu tanımlanmazsa sadece yazılabilir(writeonly) olacaktır.

Şimdi property ile encapsulation yapacaksam önce nesne üzerinde fieldlara erişimi engellemem gerek.

Property hangi fieldı temsil ediyorsa/hangi field üzerinde işlem yapıyorsa o fieldın türüyle aynı olmak zorundadır. 

Property isimlendirmelerinde field adını büyük harfle başlatarak kullanabilirsin.
int yas; fieldı int Yas{get; set;} şeklinde propertyi olacaktır.

![3-9](https://github.com/user-attachments/assets/7208272b-605e-4a1e-9255-a6f081886773)

Property tanımladık ve get metotunda property üzerinden değer talep edildiğinde bu blok tetiklenir. Yani değer buradan gönderilir/return edilir. Set metotundan, dışarıdan gelen değer value keywordü ile karşılanır ve value property türü neyse ona bürünür. 

Property oluşturma nedeni, metotlarda bu işlem daha zahmetli/uğraştırıcıdır. Property kolaylık olması için oluşturulmuştur.

![3-10](https://github.com/user-attachments/assets/54f8c238-8c4f-42d6-823f-b82c07500354)

Fieldlar mavi kutucukken, ingiliz anahtarı property pembe olanlar da metotlardır.

✨ Prop ✨

Bir property her ne kadar encapsulation yapsa da temsil ettiği fielddaki datayı hiç müdahale etmeden erişilmesini ve veri atamasını sağlıyorsa böyle bir durumda kullanılan property imzasıdır. Yani property, herhangi bir kontrol yapmaz if else vs kullanmaz.

![3-11](https://github.com/user-attachments/assets/8ce068f2-8341-45f7-98aa-3b14689be823)

Encapsulation var ama isteyen istediğini veriyor/yazıyor/okuyor. O zaman ne gerek var encapsulationa? Ahlaken gerek. Feilddaki değerlere müdahhele olsun olmasın biz direkt erişilmesini istemeyiz. Sen oraya propertyini koy, alışkanlığın olsun.

![3-12](https://github.com/user-attachments/assets/2975fe9a-c236-4817-81bd-8d78f42e1ba4)

Haliyle prop imzası, tanımlaması bu şekilde olacaktır.

Prop şeklinde oluşturulan propertylerde, compile edilirken arka planda kendi fieldlarını oluştururlar. Haliyle bir field tanımlamaya gerek yok. 

![3-13](https://github.com/user-attachments/assets/753a5813-52d3-47b7-ae28-ded33bb6f8bd)

![3-14](https://github.com/user-attachments/assets/87d9a667-54c2-470c-9fdb-72c837f7f118)

İlk görselde normal bir field ve property oluşturuyorsun, property baş harfi büyükle başlayıp {} kullanılıyordu. İkinci görselde de property oluşturuyorsun arka planda senin için field oluşturuluyor. Dkkat edilirse herhhangi bir müdahale olmadan yasi değerini döndürdün ve gelen değeri yasi değerine atadın. İlk görselde fieldı sen tanımlıyorsun, İkinci görselde fieldı senin tanımlamana gerek yok kendi arka planda tanımlıyor. 

Ayrıca prop imzalarında ilgili property readonly olabilir ama writeonly olamaz.

✨ Auto Property İnitializers  C#6.0 ✨

Bir propertyin ilk değerini nesne ayağa kaldırır kaldırmaz aşağıdaki gibi verebiliriz.

![3-15](https://github.com/user-attachments/assets/4852eab2-eb58-4d99-a004-5ec87c3e388f)

Direkt değer verebiliyorsun çünkü bu prop propertysi olduğundan arka planda bunun için bir field oluşturuluyor ve biz aslında o fielda değer atıyoruz. 

Prop propertyler, public int Yasi {get;} = 15; readonly olabilir ama writeonly {set;} olamaz. Çünkü zaten arkada oluşturulan fielda sen değer atayacaksında bir yerde kullanmadıktan sonra bir yerde get edemedikten sonra ne anlamı var. Readonly olmasının sebebi de ilk değeri atıyorsun ya en azından daha sonra onu bir yerlerde kullanabilirsin diyor. 

Auto property initializer özelliği sayesinde readonly olan proplara hızlıca değer atanabilmektedir. 

✨ Ref Readonly Returns C#7.2 ✨

Ref metotlarda, metodun parametresine verilen değer eğer ki bir değişkenden geliyorsa değerini değil referansını metot içine almamızı sağlayan bir keyworddür. 
İşte bunu class içinde propertylerde yapmamızı sağlayan bir özelliktir.
Ref readonly returns, bir sınıf içinde fieldı referansıyla döndürmemizi sağlayan ve bir yandan da bu değişkenin değerini readonly yapan özelliktir. 

![3-16](https://github.com/user-attachments/assets/4317b343-0c3e-4a36-9471-82c7703aef82)

Ben nesne oluşturup adi fieldına ulaşmak istersem, değeri değil adi nın referansına ulaşmış olacağım.

✨ Computed(Hesaplanmış) Property ✨

İçinde türetilmiş bir bağıntı taşıyan propertydir. 

![3-17](https://github.com/user-attachments/assets/ca41e16a-5fb0-4cc3-b3ab-dbe226cbb923)

Get yada set de hesaplanma işlemleri(aritmetik) yapıyorsan adı computed property oluyor. 

✨ Expression - Bodied Property ✨

Tanımlanan propertyde lambda expression kullanmanızı sağlayan söz dizimidir.

![3-18](https://github.com/user-attachments/assets/6152bef0-0701-45e8-91d5-4747c56da991)

Sadece readonlydir.
Expression-bodied property, auto property initializer ile akrabadır diyebiliriz, ikiside ilk değer alıyor gibi düşün.

✨ Init-only Properties - İnit Accessor C#9.0 ✨

Init only properties nesnenin sadece ilk yaratılış anında propertylere değer atanmaktadır. Böylece iş kuralı gereği runtime da değerinin değişmemesi gereken nesneler için önlem alınmaktadır. 
Init-only properties, develper açısından süreç esnasında değiştirilmemesi gereken property değerlerinin yanlışlıkla değiştirilmesinin önüne geçmekte ve böylece oalsı hata ve buglardan yazılımı arındırmaktadır. Böyle bir durumda akla direkt auto property initializer gelmiş olabilir, o hahlde init-only propertiesin getiri nedir? Sonraki derslerde göreceğimiz objjject initializer desteğidir. 

![3-19](https://github.com/user-attachments/assets/0c7f39ba-1f8d-488e-9c1f-c0180e0eb195)

Auto property initializer, object initializera izin vermemektedir. 

![3-20](https://github.com/user-attachments/assets/df442595-f3e4-4113-92ff-290b2b87f966)

Fakat bu özellik init-only propertiesi desteklemekte ve sonrasında read only özelliği göstermektedir.

👋 6 - Metot

Nesne üzerinde, fieldlarda ki yahut dışarıdan parametreler eşliğinde gelen değerler üzerinde işlemler yapmamızı sağlayan temel programatik parçalardır. 

👉 ! Hiçbir property void olamaz. Kesinlikle bir türü olmalıdır. 

Ama metotlar void olabilir yani geri dönüş değeri oladabilir olmayadabilir. Property ise kapsülleme yapacağı için veri transferi yapcağı için arada olacak ve gelen giden verinin türünde oalcaktır. 

Metotlarda, nesneadi.metotadi(); şeklinde kullanım vardır.

✨ Indexer ✨

Nesneye indexer özelliği kazandıran, fıtrat olarak property ile birebir aynı olan elemandır. 
Bir sınıfın içindeki nesneye idnexer özelliği kazandırmak istiyorsan thhis keywordü kullanılmalıdır. Eğer isim verirsen normal property olur.

![3-21](https://github.com/user-attachments/assets/07ebba06-3857-4deb-9be1-e5bbcee7b543)

[parametreler] köşeli parantez indexerı temsil eder.

![3-22](https://github.com/user-attachments/assets/664440bf-7a73-4ff8-8268-ebbf593cf824)

Burda başka classta nesne oluşturup myClass[5] = 10; dedik. Ayrıca set içinde de parametredeki a ya erişebilirim.












👉 !
