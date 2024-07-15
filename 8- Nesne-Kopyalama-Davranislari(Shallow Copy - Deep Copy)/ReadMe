👋 1 -  Nesne Kopyalama Davranışları - Shallow Copy - Deep Copy
Nesne/Değer kopyalama ile kastedilen nedir?
Değer türlü değişkenler belleğin stack kısmında tanımlanan ve değeri de stack kısmında tutulan değişkenlerdir. Nesnelerden farkı sadece değersel olmalarıydı sadece veri olmalarıydı. 

foto1- deep copydir. Burada elimizdeki veri birken iki oldu. Yani veri çoğaltıldı.

Nesne kopyalama özünde iki davranış biçimi üzerinden seyreden bir operasyondur. Shallow ve deep copy yöntemleridir. 

👉 !  Nesnelerde bir değerdir ama complex değerleredir.
                                                              
  ✨ Shallow Copy ✨

Var olan bir nesnenin,değerin referansının kopyalanmasıdır. Shallow copy neticesinde eldeki değer çoğaltılmaz. Sadece birden fazla referansla işaretlenmiş olur. 

Değer türlü değişkenler üzerinde atama işlemi yapılıyorsa deep copy olur. Eğer ki bu davranış referans türlü değişkenlerde oluyorsa shallow copy olur. 

Foto2-3 Bir nesne birden fazla referansla işaretleniyorsa bunların hepsi shallow copydir. Deep copy değildir çünkü deep copyde derin kopyalamada eldeki veri çoğaltılıyordu, burada öyle bir şey yok.

👉 !  Bir referans sadece tek bir nesneyi işaret eder. 

foto4 - m1 ve m2 ile nesneler oluştu. m3 = m1 için, m3 referansı m1 in işaret ettiği nesneyi işaret edecektir. m1 = m2 durumunda, m1 zaten m1 nesnesini işaret ediyordu ama artık m1 nesnesini işaret etmeyi bırakıp m2 nin işaret ettiği nesneyi işaret edecektir. Dolayısıyla m1 in işaret ettiği nesne heapte boşa düşmüş olacaktır. m2 = m1 için, m2 referansı m1 in işaret ettiği nesneyi işaret edecektir. m1 = m1 için, m1 in işaret ettiği nesnenin bağlantısının kopup tekrar m1 in işaret ettiği nesneyi işaret ettiğini düşünün. Bu durumda elde var olan değerler türetilmediği için bütün hepsinde shallow copy yapılmış oldu. 

foto5- Nesne tek fakat işaretleyen referans sayısı birden fazla. Bu durum shallow copydir. 

  ✨ Deep Copy ✨

Var olan bir nesne, deep copy ile kopyalanıyorsa eğer ilgili nesne miktarı çoğalır. Aynı özelliklere ve değerlere sahip bellekte farklı bir nesne daha oluşur. 

foto6 - 
Shallow Copyde: referans türlü değişkenlerin değerlerinin default davranışı shallow copydır. 
Deep Copyde: Değer türlü değişkenlerde default davranış deep copydir. Deep copy kısmındaki a için metot(a) olsa, buraya a nın değeri olan 5 değeri gelecektir, a nın kendisi değil. Derin kopyalamada a nın üstünde ne yaparsan yap b yi etkilemez. b nin değeri aynen kalacaktır. Aynı şey b içinde geçerlidir. 

foto7 - Şimdi, değer türlü ve referans türlü değişkenlerin defaultunu söyledik. Referans türlü değişkenlerde deep copy nasıl yaparız? IClonable dediğimiz, klonlama yapabileceğimiz bir arayüzden bunu türetmemiz gerekir. OOP de deep copy yapabilmek için referans trlü değişkenlerde illa bir metota ihtiyaç vardır. Syntax üzerinden bunu yapmayız. 

foto8- Geriye object türü dönecek ve unboxing yapman gerekecektir. MyClass m3 = m1.Clone() demek gerekir. 

Shallow copyde, bir nesneyi birden çok referans ederse ve o nesne üzerinde değişiklik yapılırsa diğer referans edenlerde etkilenmiş olur. Çünkü hepsi tek bir nesneyi ve aynı nesneyi işaret ediyor. 

















