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

foto1 - Bu classtan oluşturulan nesnede direkt olarak a fieldı olacaktır ve int türünden bir değer atayabiliyor olacaksın. 

👉 ! Field kelimesi sadece class içindeki değişkenler için kullanılır. Main içinde yada metot içinde değişken tanımlaması varsa değişken diyeceksin, field değil. 

MyClass için nesne oluşturmak istiyorsam, new MyClass() demek yeterlidir. Foto2 - Oluşan MyClass nesnesini MyClass türünden m1 refernası ile işaretleyeceğim. new MyClass() heap e nesneyi koyacak. m1 referansıyla stackte olup, heapteki nesneyi işaret edecek. Dolayısıyla m1. dediğimde içinde hangi elemanlar varsa ulaşabiliyor olacağım. Ayrıca burada m1. ile a fieldına erişemedik, bunun nedeni access modifier dediğimiz erişim belirleyicisidir. a nın erişim belirleyicisi default olarak privatetır. Dışarısdan m1. ile a ya erişmek istersem a nın erişim belirleyicisini public yapmam gerekir. 

Foto3 - m1. ile açılan pencerede de a nın erişilebilir olduğunu görebilirsin. 

👉 ! Foto4- Fieldlar tanımlanırken değer verilmezse stackte fiedlara varsayılan/default değerler atanır. 

👉 ! Türüne göre otomatik default değer atama işlemi sadece class içinde tanımlanan değişkenlerde/fieldlarda geçerlidir. Sen bu değişkeni main içinde yada metot içinde tanımlasaydın default değer atanmayacaktı. 

👋 3- Property
Nesne içinde özellik sağlar. Peki bu özellik sağlaması ne demek?
Property özünde bir metottur. Yani programatik/algoritmik kodlarımızı inşa ettiğimiz bir metottur. Fakat fiziksel olarak metottan farkı parametre almamakta ve içerisinde get set olmak üzere özelleştirilmiş iki adet blok bulunmaktadır.
Foto5- Normal metottan farkı, metotta parantez vardır ve parametre alabilir. Property de ise parantez yok ve parametre alamaz. Set bloğunda propertye değer atandığı zaman bu değeri set bloğunda yakalarız. Propertyin değeri okunmak istendiğinde de get bloğu tetiklenir/return edilir. 
Propertyin işlevsel açıdan metotlardan farkı yoktur. Fakat davranışsal olarak nesne üzerinde bir değer okuma ve değer atama işlemlerinde kullanılır. 

👉 ! Bir fieldın değerini okuma yada değer atama kısmında property devreye girer. 

👉 ! Derleyici, property'leri arka planda get ve set metotlarına dönüştürür.

👉 ! IL (Intermediate Language) Seviyesinde: Property'ler, get_PropertyName() ve set_PropertyName(value) şeklinde metotlara dönüşür.

👋 4- Property Ne Amaçla Kullanılır?

Biz yazılımcılar nesne içindeki fieldlara direk erişilmesini istemeyiz. Fieldlardaki veriyi kontrollü bir şekilde dışarıya açmak istiyoruz. benim cüzdanımdan para istersen direkt sen alma cüzdanı bana getir ben vereyim gibi düşün. İşte bu durumu propertyler sağlar. Tabi fieldlardaki değerleri göstermemek için fieldlarıdan dışarıdan erişilebilir olmasını engellemek gerekir, yani fieldları private olarak işaretlemek gereklidir. Kontrollü olarak function tanımlayıp verilir. Bu fonksiyonlara göndereceğim veriler de tamamen bana bağlı istersem hepsini istersem bir kısmını gönderirim yani benim kontrolümde. 
Foto6- Cüzdan örneğinde senden 100 ₺ para istediler, sen dur getir cüzdanı ben veririm dedin. 100 ₺ değil 50 ₺ vermek istedin/verdin. Halbuki cüzdanında olan diğer 50 ₺ den onun haberi yok. Bunu bilemez, çünkü arada sen varsın senin kontrolün var. 

Bu dışarıdan erişilme mevzusunda C# metot yerine property getirmiş, evet metotla da bu işlemi gerçekleştirebilirsin ama biz property ile yaparak fark yaratalım demiş. Yani property yapıları özünde nesne içindeki fieldın dışarıya kontrollü açılmasını ve kontrollü bir şekilde dışarıdan değer almasını sağlayan yapılardır. İşte biz propertylerin bu işlevine encapsulation(kapsülleme/sarmalama) diyoruz. Benim fieldıma sen erişemezsin/okuyamazsın dememiz, property üzerinden erişebilirsin dememiz aslında o fieldı kapsüllememiz anlamına geliyor. 

👋 4- Encapsulation - Kapsülleme - Sarmalama

Encapsulation, bir nesne içindeki dataların(fieldlardaki veriler) dışarıya kontrollü bir şekilde açılması ve dışarıdan kontrollü bir şekilde veri almasıdır. 
Foto7- İşte bu şekilde fieldlardaki verilerin erişim kontrolünü yapmamız için geliştirilmiş olan yapılara property denir. Property kullanıyorsan encapsulation uyguluyorsun demektir. 

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
Erişim belirleyici yapılanması kalıtım konusu altında incelenecektir.
Ayrıca full propertyde set bloğu tanımlanmazsa sadece okunabilir(readonly), get bloğu tanımlanmazsa sadece yazılabilir(writeonly) olacaktır.

Şimdi property ile encapsulation yapacaksam önce nesne üzerinde fieldlara erişimi engellemem gerek.

Property hangi fieldı temsil ediyorsa/hangi field üzerinde işlem yapıyorsa o fieldın türüyle aynı olmak zorundadır. 

Property isimlendirmelerinde field adını büyük harfle başlatarak kullanabilirsin.
int yas; fieldı int Yas{get; set;} şeklinde propertyi olacaktır.

Foto9 - Property tanımladık ve get metotunda property üzerinden değer talep edildiğinde bu blok tetiklenir. Yani değer buradan gönderilir/return edilir. Set metotundan, dışarıdan gelen değer value keywordü ile karşılanır ve value property türü neyse ona bürünür. 

Property oluşturma nedeni, metotlarda bu işlem daha zahmetli/uğraştırıcıdır. Property kolaylık olması için oluşturulmuştur.

Foto10 - Fieldlar mavi kutucukken, ingiliz anahtarı property pembe olanlar da metotlardır.

✨ Prop ✨

Bir property her ne kadar encapsulation yapsa da temsil ettiği fielddaki datayı hiç müdahale etmeden erişilmesini ve veri atamasını sağlıyorsa böyle bir durumda kullanılan property imzasıdır. Yani property, herhangi bir kontrol yapmaz if else vs kullanmaz.

Foto11- Encapsulation var ama isteyen istediğini veriyor/yazıyor/okuyor. O zaman ne gerek var encapsulationa? Ahlaken gerek. Feilddaki değerlere müdahhele olsun olmasın biz direkt erişilmesini istemeyiz. Sen oraya propertyini koy, alışkanlığın olsun.

foto12 - Haliyle prop imzası, tanımlaması bu şekilde olacaktır.

Prop şeklinde oluşturulan propertylerde, compile edilirken arka planda kendi fieldlarını oluştururlar. Haliyle bir field tanımlamaya gerek yok. 

Foto13-14- Bu iki fotoda 13 de normal bir field ve property oluşturuyorsun, property baş harfi büyükle başlayıp {} kullanılıyordu. 14 de property oluşturuyorsun arka planda senin için field oluşturuluyor. Dkkat edilirse herhhangi bir müdahale olmadan yasi değerini döndürdün ve gelen değeri yasi değerine atadın. Foto13 de fieldı sen tanımlıyorsun, 14 de fieldı senin tanımlamana gerek yok kendi arka planda tanımlıyor. 

Ayrıca prop imzalarında ilgili property readonly olabilir ama writeonly olamaz.

✨ Auto Property İnitializers  C#6.0 ✨

Bir propertyin ilk değerini nesne ayağa kaldırır kaldırmaz aşağıdaki gibi verebiliriz.
Foto15- Direkt değer verebiliyorsun çünkü bu prop propertysi olduğundan arka planda bunun için bir field oluşturuluyor ve biz aslında o fielda değer atıyoruz. 

Prop propertyler, public int Yasi {get;} = 15; readonly olabilir ama writeonly {set;} olamaz. Çünkü zaten arkada oluşturulan fielda sen değer atayacaksında bir yerde kullanmadıktan sonra bir yerde get edemedikten sonra ne anlamı var. Readonly olmasının sebebi de ilk değeri atıyorsun ya en azından daha sonra onu bir yerlerde kullanabilirsin diyor. 

Auto property initializer özelliği sayesinde readonly olan proplara hızlıca değer atanabilmektedir. 

✨ Ref Readonly Returns C#7.2 ✨

Ref metotlarda, metodun parametresine verilen değer eğer ki bir değişkenden geliyorsa değerini değil referansını metot içine almamızı sağlayan bir keyworddür. 
İşte bunu class içinde propertylerde yapmamızı sağlayan bir özelliktir.
Ref readonly returns, bir sınıf içinde fieldı referansıyla döndürmemizi sağlayan ve bir yandan da bu değişkenin değerini readonly yapan özelliktir. 
Foto16- Ben nesne oluşturup adi fieldına ulaşmak istersem, değeri değil adi nın referansına ulaşmış olacağım.

✨ Computed(Hesaplanmış) Property ✨

İçinde türetilmiş bir bağıntı taşıyan propertydir. Foto17- Get yada set de hesaplanma işlemleri(aritmetik) yapıyorsan adı computed property oluyor. 

✨ Expression - Bodied Property ✨

Tanımlanan propertyde lambda expression kullanmanızı sağlayan söz dizimidir. 
Foto18- Sadece readonlydir.
Expression-bodied property, auto property initializer ile akrabadır diyebiliriz, ikiside ilk değer alıyor gibi düşün.

✨ Init-only Properties - İnit Accessor C#9.0 ✨

Init only properties nesnenin sadece ilk yaratılış anında propertylere değer atanmaktadır. Böylece iş kuralı gereği runtime da değerinin değişmemesi gereken nesneler için önlem alınmaktadır. 
Init-only properties, develper açısından süreç esnasında değiştirilmemesi gereken property değerlerinin yanlışlıkla değiştirilmesinin önüne geçmekte ve böylece oalsı hata ve buglardan yazılımı arındırmaktadır. Böyle bir durumda akla direkt auto property initializer gelmiş olabilir, o hahlde init-only propertiesin getiri nedir? Sonraki derslerde göreceğimiz objjject initializer desteğidir. 
Foto19- Auto property initializer, object initializera izin vermemektedir. 
Foto20- Fakat bu özellik init-only propertiesi desteklemekte ve sonrasında read only özelliği göstermektedir.

👋 6 - Metot

Nesne üzerinde, fieldlarda ki yahut dışarıdan parametreler eşliğinde gelen değerler üzerinde işlemler yapmamızı sağlayan temel programatik parçalardır. 

👉 ! Hiçbir property void olamaz. Kesinlikle bir türü olmalıdır. 

Ama metotlar void olabilir yani geri dönüş değeri oladabilir olmayadabilir. Property ise kapsülleme yapacağı için veri transferi yapcağı için arada olacak ve gelen giden verinin türünde oalcaktır. 

Metotlarda, nesneadi.metotadi(); şeklinde kullanım vardır.

✨ Indexer ✨

Nesneye indexer özelliği kazandıran, fıtrat olarak property ile birebir aynı olan elemandır. 
Bir sınıfın içindeki nesneye idnexer özelliği kazandırmak istiyorsan thhis keywordü kullanılmalıdır. Eğer isim verirsen normal property olur.
Foto21- [parametreler] köşeli parantez indexerı temsil eder.
Foto22- Burda başka classta nesne oluşturup myClass[5] = 10; dedik. Ayrıca set içinde de parametredeki a ya erişebilirim.












👉 !
