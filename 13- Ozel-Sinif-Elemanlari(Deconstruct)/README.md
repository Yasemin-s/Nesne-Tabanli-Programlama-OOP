👋 1 - Deconstruct Metot Nedir ?

Bir sınıf içinde deconstruct ismiyle tanımlanan metot, compiler tarafından özel olarak algılanmakta ve sınıfın nesnesi üzerinden geriye hızlıca Tuple bir değer döndürmeyi sağlamaktadır. 

👉 ! Özel sınıf memberları dediğimğiz yapılanmaların şöyle bir ortak özelliği vardır. Tüm özel elemanların adı sınıf adıyla aynı olmalıdır. Bu özel sınıf memberlarının arasında bir tane istisna vardır. Deconstruct fonksiyonudur. Deconstruct fonksiyonu sınıf ismiyle aynı olamaz. Deconstruct metodunun ismi deconstruct olmalııdır. 

![13-1](https://github.com/user-attachments/assets/ed9276ce-5657-4227-b0f1-9f284443899a)

Elimizde obje var ve belirli property var. Bu nesnenin hızlı bir şekilde tuple nesnesini almak istiyorsak bu sınıfın nesnesinin içerisinde yada bu sınıfın modeli olan classın içinde deconstruct dediğimiz fonksiyon tanımlaması gerekir. Eğer tanımlanmadıysa var(X,Y) = A; semantiği geçerli olmayacak ve hata verecektir.

✨ Prototip ✨

![13-2](https://github.com/user-attachments/assets/8ec42c14-141b-4c70-ad9e-e574b4e91cce)

Void ile işaretlenmelidir. Diğer sınıf özel elemanlarının adı sınıfın adıyla aynı olması gerekiyorken, burada deconstruct olacaktır. Fonksiyonun dışarıdan erişilebilir olması gerekir. Deconstruct sayesinde geriye tuple nesne döner. 

👉 ! Fonksiyon void ise geriye nasıl değer dönüyor?

Tuple olarak geriye döndürülecek değerler deconstruct fonksiyonunda out keywrodü ile tanımlanmış parametreler olamlıdır. 

C# programlama dilinde bir deconstruct(yapı bozucu), bir nesneyi bileşenlerine ayırmak ve bu bileşenlerin değerlerini döndürmek için kullanılır. Deconstruct yöntemi, void dönüş türüne sahip olarak tanımlanır çünkü dönüş değeri, metot imzasında yer almaz. Bunun yerine, çıkış(out) parametreleri aracılığıyla değerler dışarıya aktarılır. 
