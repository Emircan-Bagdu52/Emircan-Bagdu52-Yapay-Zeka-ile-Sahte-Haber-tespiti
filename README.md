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
 <h4><3.2.4.TF-IDF/h4>
Doğal dil işleme çalışmalarında, metinsel ifadelerin vektörel ifadelere     dönüştürülmeleri gerekmektedir. Bu şekilde matematiksel işlemler yapılabilmektedir. Bu işlem için TF-IDF, doğal dil işlemede sıkça kullanılmaktadır. TF-IDF, tahmin yapmak amacıyla makine öğrenmesi algoritmalarına verilecek olan verilerde, verinin içerisindeki bir kelimenin ne kadar öneme sahip olduğunu hesaplamaktadır. Terim frekansı (TF) ile Ters Doküman Frekansı (IDF) çarpılarak hesaplanmaktadır. Bu işlem dokümanlardaki her kelime için yapılmaktadır.[6]
TF-IDF(t,d)=TF(t,d)  x IDF(t)	
<h3>3.3.Sınıflandırma</h3>
Sınıflandırma işlemleri yapay zekanın alt dalı olan makine öğrenmesi çatısı altındaki sınıflandırma algoritmaları kullanılarak yapılmıştır. Bu projede sınıflandırma, ikili sınıflandırma (Binary Classification) türüdür. Veri gerekli ön işlem ve öznitelik çıkarımlarından sonra doğru veya yanlış olarak sınıflandırma işlemine tabi tutulmaktadır. Sınıflandırma algoritması için Sklearn kütüphanesi içerisindeki sınıflandırma algoritmaları knn ve naive bayes kullanılmıştır.
<h4>3.3.1.K-NN</h4>
Sınıflandırma problemleri için kullanılan denetimli bir makine öğrenmesi algoritmasıdır.
K-NN sınıflandırmasında, çıktı sınıf üyeliğidir. Bir nesne, komşularının çoğunluk oyuyla sınıflandırılır; nesne, en yakın komşuları arasında en yaygın olan sınıfa verilir.
<h4>3.3.2.Naive Bayes</h4>
Bayes‘in teoremine dayanır ve her değeri diğer değerlerden bağımsız olarak sınıflandırır. Olasılık kullanarak ve belirli bir dizi özelliğe dayanarak bir sınıfı / kategoriyi tahmin etmemizi sağlar.
<h4>3.3.3.Sınıflandırma Algoritmasının Değerlendirilmesi </h4>
Karmaşıklık matrisi veri setindeki var olan durum ile sınıflandırma modelimizin doğru ve yanlış tahminlerinin sayısını tablo olarak göstermektedir. Accuracy (Doğruluk): Sistemde doğru olarak yapılan tahminlerin tüm tahminlere oranıdır.
![image](https://github.com/Emircan-Bagdu52/Emircan-Bagdu52-Yapay-Zeka-ile-Sahte-Haber-tespiti/assets/95845060/d2f4b696-e791-4c7c-be3f-77fd27706cba)

<h2>4.UYGULAMA</h2>
Projenin çözümü için tasarlanan algoritma, Python programlama dili üzerinde kodlanmıştır.
<h3>4.1.Metin Ön İşleme Aşaması</h3>

	Gerekli Kütüphanelerin Dahil Edilmesi
![image](https://github.com/Emircan-Bagdu52/Emircan-Bagdu52-Yapay-Zeka-ile-Sahte-Haber-tespiti/assets/95845060/2f7e68af-bf6a-4bee-8161-8e64a3b6f3da)

	Veri Setinin Dahil Edilmesi 
![image](https://github.com/Emircan-Bagdu52/Emircan-Bagdu52-Yapay-Zeka-ile-Sahte-Haber-tespiti/assets/95845060/894538b1-9a8e-45e9-8c06-69d273b86b89)
	Metin Düzenlenme İşlemi
![image](https://github.com/Emircan-Bagdu52/Emircan-Bagdu52-Yapay-Zeka-ile-Sahte-Haber-tespiti/assets/95845060/312cfa69-ea72-42b7-ae24-4a80c052a9d2)
<h3> 4.2.Öznitelik Çıkarım Aşaması</h3>
	Veri Setinin Train-Test Olarak Bölünmesi
![image](https://github.com/Emircan-Bagdu52/Emircan-Bagdu52-Yapay-Zeka-ile-Sahte-Haber-tespiti/assets/95845060/b5c40af3-99a4-48cd-969f-259da67c3a92)
	Vektörizasyon İşlemi
![image](https://github.com/Emircan-Bagdu52/Emircan-Bagdu52-Yapay-Zeka-ile-Sahte-Haber-tespiti/assets/95845060/ac0b6855-9dec-496f-9896-8d55a64fc7de)
	TF-IDF Skoru Hesaplama İşlemi
![image](https://github.com/Emircan-Bagdu52/Emircan-Bagdu52-Yapay-Zeka-ile-Sahte-Haber-tespiti/assets/95845060/e52c8510-a7ce-4e66-b22a-570cc0b5f30d)
<h3>4.3.Sınıflandırma Aşaması</h3> 
	NAİVE BAYES Sınıflandırma Modelinin Test Edilmesi
![image](https://github.com/Emircan-Bagdu52/Emircan-Bagdu52-Yapay-Zeka-ile-Sahte-Haber-tespiti/assets/95845060/0ff96afc-2068-45a0-bf76-a52f2c5722d5)
![image](https://github.com/Emircan-Bagdu52/Emircan-Bagdu52-Yapay-Zeka-ile-Sahte-Haber-tespiti/assets/95845060/ff60f6f9-6f28-4364-814d-d650c7c8418c)
	KNN Sınıflandırma Modelinin Test Edilmesi
![image](https://github.com/Emircan-Bagdu52/Emircan-Bagdu52-Yapay-Zeka-ile-Sahte-Haber-tespiti/assets/95845060/106a1e17-4b33-46e0-bb3d-901525b02a52)
![image](https://github.com/Emircan-Bagdu52/Emircan-Bagdu52-Yapay-Zeka-ile-Sahte-Haber-tespiti/assets/95845060/0e27224f-a8ad-469f-a448-5f618fd2e1e2)

<h2>Kaynakça</h2>
[1] Toğaçar, M., Eşidir, K. A., & Ergen, B. (2022). Yapay Zekâ Tabanlı Doğal Dil İşleme Yaklaşımını Kullanarak İnternet Ortamında Yayınlanmış Sahte Haberlerin Tespiti. Journal of Intelligent Systems: Theory and Applications, 5(1), 1-8. 
[2] YILDIRIM, E. (2022). HIZLANDIRILMIŞ MAKİNE ÖĞRENMESİ ALGORİTMALARI İLE TÜRKÇE SAHTE HABER TESPİTİ (Doctoral dissertation).
 [3] TAŞKIN, S. G., Küçüksille, E. U., & Topal, K. Twitter üzerinde Türkçe sahte haber tespiti. Balıkesir Üniversitesi Fen Bilimleri Enstitüsü Dergisi, 23(1), 151-172.
 [4] https://yalansavar.org/2020/03/03/podcast-22-uydurma-haberler/ 
[5] Onur Dayıbaşı. (Aug 13, 2015). TF-IDF (Term Frequency — Inverse Document Frequency). Medium. https://medium.com/algorithms-data-structures/tf-idf-term-frequency-inverse-document-frequency-53feb22a17c6
 [6] Şevval Ayşe Yurtekin. (23 OCA 2022). Doğal dil işlemede temel kavramlara hızlı bir bakış. miuul. https://www.miuul.com/not-defteri/dogal-dil-islemede-temel-kavramlara-hizli-bir-bakis




