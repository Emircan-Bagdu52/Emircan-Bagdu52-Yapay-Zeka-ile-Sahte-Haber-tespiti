<h1>Sahte Haber Tespiti Projesi</h1>
    
<h2>1.Problem</h2>
Son yıllarda dijital çağın çok hızlı gelişmesiyle birlikte, insanların bilgi haber alma kaynakları da değişmiştir. Radyo, televizyon ve dergi gibi geleneksel medya platformları yerine sosyal medya kullanımı giderek artmaktadır. Sosyal medyadaki haberlerin kalitesi geleneksel medyadaki haberlerin kalitesine göre daha düşüktür. Geleneksel medyada sadece gazeteciler haber yaparken sosyal medyada herkes haber yapabilmektedir. Bu da sosyal medyada sahte haber yayılımını arttırmaktadır.Sahte haber; insanları yanıltma veya propaganda amacıyla sahte kullanıcılar tarafından yayılan haberlerdir. Sahte haberler yanlış olmasının yanı sıra ilgi çekici olduklarından sosyal medyada hızla yayılmaktadır.Sosyal medya platformlarında sahte haber tespiti uzman kişiler tarafından yapılmaktadır. Sosyal medya platformlarında sahte haberlerin uzmanlar tarafından tespit edilmesi, yoğun paylaşım trafiği yüzünden mümkün olmamaktadır. Bu yüzden sahte haber kısa sürede birçok işi tarafından bilinçsizce paylaşılıp sahte haberin tespiti anlamında negatif etkiler oluşturmaktadır.Günümüz medyasının en büyük sorunlarından biri haline gelen dezenformasyon, yayılma hızı nedeniyle gerçek bilgilerin önünü kapatmaktadır. Dezenformasyonla Mücadele Yasası hayatımıza çok sayıda yenilik getirerek yalan haberin yayılmasını engelleme konusunda önemli bir rol oynamaktadır.Projemizde, insanlar tarafından paylaşılan sahte haber sayısını azaltmak için geliştireceğimiz yazılım ile Dezenformasyonla Mücadele Yasası’na bir katkıda bulunmayı planlanmaktadır. Bu kapsamda projemizde yapay zekâ algoritmaları kullanarak yazılan haberlerin sahte haber kapsamına girip girmediğini sınıflandırarak sahte haberin yayılmasını önlemeyi hedeflenmektedir.
<h2>2-Veri Seti</h2>
Haberler Teyit.org ve Github ortamlarından manuel olarak toplanarak veri seti oluşturulmuştur. Veri seti 642 doğru haber, 926 yanlış etiketli olmak üzere 1568 haberden oluşmaktadır.
![image](https://github.com/Emircan-Bagdu52/Emircan-Bagdu52-Yapay-Zeka-ile-Sahte-Haber-tespiti/assets/95845060/df8e7ab2-9421-48aa-83b1-8e961088ae98)

<h2>3.Algoritma</h2>
Projede haberleri doğru veya yanlış olarak sınıflandırmak için oluşturulan algoritma metin ön işleme, öznitelik çıkarımı ve sınıflandırma algoritması olmak üzere 3 adımdan oluşmaktadır.

<h3>3.1.Metin Ön İşleme</h3>
     Metin ön işlemede Python dili üzerinde, NLTK ve ZEMBEREK kütüphaneleri ağırlıklı olmak üzere bu kütüphanelere ek olarak bazı farklı modüller ve Python’da gömülü gelen fonksiyonlar kullanılacaktır. NLTK ile cümlelerdeki noktalama işaretlerini sayısal ifadeleri, durak kelimeleri çıkarmak için ve tüm karakterleri küçük karakterlere çevrilmesi gibi işlemleri yapılacaktır. ZEMBEREK kütüphanesini ise kelimeleri, köklerine ve gövdelerine ayırmak için kullanılacaktır. İki ayrı kütüphane kullanılmasının nedeni ise NLTK kütüphanesi Türkçe gibi sondan eklemeli dillerde kelimenin köklerini ve gövdelerini çoğu kez doğru bir şekilde bulamamasıdır.
<h3>3.2.Öznitelik Çıkarımı</h3>
      Önişleme adımlarından sonra eldeki metin verisi makine öğrenmesi algoritmaların işleyeceği hale TF-IDF doküman temsili ile getirilecektir.
<h4>3.2.1.Vektörizasyon</h4>
 Doğal Dil İşleme çalışmalarında, matematiksel işlemlerin yapılabilmesi için metinsel ifadelerin vektörel ifadelere dönüştürülmesi gerekmektedir.[4]
<h4>3.2.2.Terim Frekansı (TF)</h4>
 Bir dokümanda geçen terimlerin terim ağırlıklarını hesaplamak için kullanılır. Metindeki bir terimin metinde toplam kullanılma sayısının, metindeki tüm terimlerin toplam sayısına oranıdır. [5]
 Terim Frekansı(TF)=((Terimin dokümanda görülme sayısı))/((Doküman terimi sayısı))
 <h4>3.2.3.Ters Doküman Frekansı (IDF)</h4>
 Kelimenin kaç farklı dokümanda geçme sayısını bularak bu kelimenin terim olup olmadığını bağlaç vb. (Durak Kelimeler) olduğu anlamaya çalışır. Toplam doküman sayısının, terimi içeren doküman sayısına oranıdır. [5]
 Ters Doküman Frekansı(IDF)=log⁡((Toplam doküman sayısı)/(Terimi içeren doküman sayısı))

