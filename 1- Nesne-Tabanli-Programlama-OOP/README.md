👋 1 - Nesne Tabanlı/Yönelimli Programlama - Object Orianted Programming - Nesne Anatomisi - Referans Türlü Değişkenler

Günümüzde nesne tabanlı programlama bir çok modern dil tarafından desteklenir. (java, C#, C++)
Nesne tabanlı programlama bir programlama dili, bir yapı, bir kütüphane değildir. Bir yaklaşımdır.

Yaklaşım şudur, işi yapma ahlakıdır. İşi düzenleme, işi matematiğe/mantığa dökmektir, hangi formülü kullanman gerektiğini bilmektir. Dolayısıyla yaklaşım dediğimiz olay, bir olguya bir yapıya bir inşaaya yaklaşma biçimidir. Yaklaşım dediğimiz olay, o işi o olguyuu hangi felsefe ile ele aldığımızdır. 

OOP yaklaşımını yazılımda kullandıysan bu yaklaşımı bilenler senin geliştirmiş olduğun koda bu yaklaşımın mantığıyla bakıp yorumlayabilirler.                                                                              
Nesne tabanlı programlamada amaç şudur: 
Gerçek hayatı, programlama için simüle eden nesneleri baz alan bir programlama tekniğidir. Buradaki nesne kavramı gerçek hayattaki bütün olguları bütün nesneleri yazılımda simule edebilmemizi sağlayan bir yapıdır. Nesne tabanlı programalama da bu nesneyi kullanarak program yazmamızı sağlayan bir yaklaşımdır.                                                                            
Her şey nesneden ibarettir. Sen ben personel satış araba ve diğerleri, aklına ne geliyorsa.

Gerçek bir sistem, nesnel parçalara ayrılır ve bu parçalar(nesneler) aralarında ilişkiler kurulur. Nesneler kendi aralarında haberleşebiliyorlar. 
                                                                                
👉 ! Nesne tabanlıprogramlama, programlama dillerinin içinde kullanılan bir yaklaşım ve bu yaklaşımdaki temel esas her şeyin bir nesne olmasıdır. 
                                                                                
  ✨ Nesne Anataomisi ✨

![1-1](https://github.com/user-attachments/assets/cb62dbf6-defb-491a-81e7-f8e8146c6d36)

Nesne anatomisini bilirsen nesne tabanlı programlamanın büyük bir kısmı tamamlanacaktır. 
Nesne anatomisinde merkezde nesne vardır. Nesne tabanlı programlamada en küçük esas parça nesne/object/objedir.                                                                     
👉 ! Bu nesneye ileride instance diyeceğiz. Bu nesne günlük hayatta olabilecek herhangi bir olguya karşılık gelebilir, personel olabilir, araba, ürün telefon...   

Nesnenin/merkezdeki yapılanmanın belirli parçaları vardır. Neseneler içerisinde veri tutabilecekleri alanlar barındırılar. Biz bu alanlara field deriz. Yani senin en temel/esas parçan nesne ve bu nesne içerisindeki alanlarda veriler tutabiliyorsun.

👉 ! Bu alanlara class elemanlarında field dieyceğiz. 
                                                                                
Class elemanları olan fieldlarda bool, char, ahmet, mehmet gibi herhangi bir değer tutabilirsin. Nesne içindeki bu alanların sınırı yoktur. 

Nesne içinde operasyonel işlemler yapmamızı sağlayan metotlar/functionlar vardır. Nesneler, içinde bulunan fieldlardaki değerleri işleyebilmesi için fonksiyonlara ihityaç duyar. Bu fonksiyonlar aracılığıyla, nesne içindeki değerleri işleyerek sonuçlar üretebiliyor ve farklı değerler ortaya koyabiliyoruz. 

👉 ! Yani nesne tek başına bir ekosisteme sahiptir. 

Bu fonksiyonlara ileride metotlar, propertyler yada indexerlar diyeceğiz. 

Prosedürel programlamada bir sınıftaki butün çğrencilerin yaşlarını tutacaksam tek tek değişkenlerde bu yaşları tutabilirm. Pekii, hangi öğrencinin yaşı nedir diye sorsam işte bu sorunun cevabını prosedürel programlamada vermek çok zordur. Çünkü, ilk önce ismini  tutacaksın daha sonra yaşını vs tutacaksın. Bunu her öğrenci için yaptıktan sonra hangisi hangisine aitti vs derken kodlar iyice karmaşıklaşacak. Bunun yerine bir sınıftaki her bir öğrenciyi nesne olark tanımlasan bu öğrencilerin adı ve yaşı fieldları olsa işler çok daha kolay olur. Kodu nesnel hale getirmek artık daha sistematik kod inşaası oluşturmamızı sağlıyor ve yorumlanabilme açısından da olay daha sistematik hale geliyor.                                                                                
👉 ! OOP dillerinde nesneyi oluşturabilmek için ilk önce o nesneyi modellememiz gerekiyor. 
                                                                                
👉 ! Nesneler esasında bir sınıf modellemesinin örneğidir. Yani senin bir nesneyi modelleyebilmen için önce bir sınıf/class oluşturman gerekiyor. 

👉 ! Nesne = classtır, interface, abstract vs değildir.
👉 ! Nesne, classın bir ürünüdür. Sadece classtan nesne oluşturabilirsin.
👉 ! Bir classtan birden fazla nesne üreterek modelleme yapabiliyorsun. Örnek, tc kimlik kartının bir modeli vardır ve 80 milyon da nesnesi vardır. 
👉 ! Modelleme, bir tane tanımlamadır. Bu tanımlamadan/modelden n adet/istediğin kadar nesne üretebiliyorsun. Tabi buradaki sınırın senin belleğindeki sınıra kadardır. 

  ✨ Nesne Kavramı ✨                                                                  
Nesne, nesnellik felsefesine dayanan bir kavramdır. Dünyadaki her şeyi bir nesne olarak görme ve o şekilde yorumlamak fikrine dayanır.
Nesne, gerçek hayatta elle tutulur gözle görülür objelerdir. Dolayısıyla programlamada nesnelerimiz günlük hayatta kullandığımız gibi elle tutulur gözle görünür objelermiş gibi yorumlanacak ve o gerçek objelerin modellemesi/muadili olarak tanımlanacaktır. Nesne tabanlı programlama, o yazılım simülasyonunda sana gerçek hayatın ta kendisini sunuyor. Gerçek hayattaki herhangi bir olguyu, nesneyi, objeyi programlama dünyasında tarif ederken de onu bir nesne olarak tarif edecek ve o şekilde modelleyeceğiz.                                                                    
  ✨ Nesne Modellemesi ✨  
Bir nesneyi nesne olarak kullanabilmen için öncelikle kodun içinde o nesneyi modellemen gerekiyor. Modelledikten sonra o modelden nesne oluşturabiliyorsun.

👉 ! Yani nesnelerin kullanılabilmesi için önce nesnenin modellenmesi gerekiyor. Nesne modeli ouşturabilme ihtiyacı classlar ile karşılanır. 

![1-2](https://github.com/user-attachments/assets/1d01a4b6-4197-4629-8736-d4c683514f71)

Buradaki nesnelerin her biri car nesnesidir. Ama her biri birbirinden farklı nesnelerdir. Hepsinin km si var, hepsinin tekeri var, beygiri var, rengi var. İşte bunlar classta modelleniyor yani oluşturduğum classta araba için şu özellikler(km,teker,beygir,renk) olması gerek diyorum. Modellenen bu değerler değiştirilebiliyor. Değişkenlikler nesne üzerinde olur ama ortak tanımlamalar modelde olur. Car modelinden üretilen nesneler birbiriyle haberleşme yeteneğine sahip ama birbirinden bağımsız sadece o olguyu tarif eden nesneler olmuş oluyor. 

  ✨ Nesneler Hangi Türdedir? ✨  
Şimdiye kadar değer türlü ve referans türlü değişkenler öğrendik. 
👉 ! Nesneler, referans türlü değişkenlerdir.
Peki referans türlü değişkenler/değerler nelerdir?

![1-3](https://github.com/user-attachments/assets/2ce06a13-0086-447f-a59f-c6f37bb10a58)                               
                                                                                
Stackte değer türlü değişkenler ve değerleri ayrıca referanslar tutulur. Heapte ise sadece nesneler tutulur. Nesne, içinde bir veya birden fazla değer barındıran bir değerler bütünüdür. Developer olarak stackteki değişkenlere direk erişebilirm ama heapteki nesnelere direk erişemem ama stack, heap'e erişebilir. Stackte tanımlamış olduğumuz referanslar/değişkenler heap'e erişebilirler. Dolayısıyla biz stackte, heapteki nesneleri işaret eden referanslar tanımlayabiliyoruz ve böylece ben stacke , stackteki referansta heape erişmiş oluyor. Yani dolaylı olarak heape erişebiliyorum. Örnekteki, nesne1 in değeri stackte yoktur, bunun değeri heapteki nesne1 dir. Stackteki r1 ile heapteki nesne1 e erişebiliyorum/onu referanslıyorum/referans gösteriyorum/referans ediyorum.                                                        
  ✨ Sınıf/Class Kavramı ✨  
Sınıf, OOP'nin temelidir. OOP de merkezde olan nesnedir ve nesne classtan oluşturulur. Classtan nesne modeli oluşturuyoruz ve ardından bundan/sınıftan ürettiğin şey nesne oluyor.
