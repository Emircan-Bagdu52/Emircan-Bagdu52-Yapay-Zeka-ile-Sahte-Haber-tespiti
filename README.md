<!DOCTYPE html>
<html lang="tr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Sahte Haber Tespiti Projesi</title>
</head>
<body>
    <h1>Sahte Haber Tespiti Projesi</h1>
    
    <h2>Problem</h2>
    <p>Son yıllarda dijital çağın çok hızlı gelişmesiyle birlikte, insanların bilgi haber alma kaynakları da değişmiştir. Radyo, televizyon ve dergi gibi geleneksel medya platformları yerine sosyal medya kullanımı giderek artmaktadır. Sosyal medyadaki haberlerin kalitesi geleneksel medyadaki haberlerin kalitesine göre daha düşüktür. Geleneksel medyada sadece gazeteciler haber yaparken sosyal medyada herkes haber yapabilmektedir. Bu da sosyal medyada sahte haber yayılımını arttırmaktadır.</p>
    <p>Sahte haber; insanları yanıltma veya propaganda amacıyla sahte kullanıcılar tarafından yayılan haberlerdir. Sahte haberler yanlış olmasının yanı sıra ilgi çekici olduklarından sosyal medyada hızla yayılmaktadır.</p>
    <p>Sosyal medya platformlarında sahte haber tespiti uzman kişiler tarafından yapılmaktadır. Sosyal medya platformlarında sahte haberlerin uzmanlar tarafından tespit edilmesi, yoğun paylaşım trafiği yüzünden mümkün olmamaktadır. Bu yüzden sahte haber kısa sürede birçok işi tarafından bilinçsizce paylaşılıp sahte haberin tespiti anlamında negatif etkiler oluşturmaktadır.</p>
    <p>Günümüz medyasının en büyük sorunlarından biri haline gelen dezenformasyon, yayılma hızı nedeniyle gerçek bilgilerin önünü kapatmaktadır. Dezenformasyonla Mücadele Yasası hayatımıza çok sayıda yenilik getirerek yalan haberin yayılmasını engelleme konusunda önemli bir rol oynamaktadır.</p>
    <p>Projemizde, insanlar tarafından paylaşılan sahte haber sayısını azaltmak için geliştireceğimiz yazılım ile Dezenformasyonla Mücadele Yasası’na bir katkıda bulunmayı planlanmaktadır. Bu kapsamda projemizde yapay zekâ algoritmaları kullanarak yazılan haberlerin sahte haber kapsamına girip girmediğini sınıflandırarak sahte haberin yayılmasını önlemeyi hedeflenmektedir.</p>
    
    <h2>Veri Seti</h2>
    <p>Haberler Teyit.org ve Github ortamlarından manuel olarak toplanarak veri seti oluşturulmuştur. Veri seti 642 doğru haber, 926 yanlış etiketli olmak üzere 1568 haberden oluşmaktadır.</p>
    
    <h2>Algoritma</h2>
    <p>Projede haberleri doğru veya yanlış olarak sınıflandırmak için oluşturulan algoritma metin ön işleme, öznitelik çıkarımı ve sınıflandırma algoritması olmak üzere 3 adımdan oluşmaktadır.</p>

    <h3>3.1. Metin Ön İşleme</h3>
    <p>Metin ön işlemede Python dili üzerinde, NLTK ve ZEMBEREK kütüphaneleri ağırlıklı olmak üzere bu kütüphanelere ek olarak bazı farklı modüller ve Python’da gömülü gelen fonksiyonlar kullanılacaktır. NLTK ile cümlelerdeki noktalama işaretlerini, sayısal ifadeleri, durak kelimeleri çıkarmak ve tüm karakterleri küçük karakterlere çevirmek gibi işlemler yapılacaktır. ZEMBEREK kütüphanesi ise kelimeleri köklerine ve gövdelerine ayırmak için kullanılacaktır. İki ayrı kütüphane kullanılmasının nedeni ise NLTK kütüphanesinin Türkçe gibi sondan eklemeli dillerde kelimenin köklerini ve gövdelerini çoğu kez doğru bir şekilde bulamamasıdır.</p>
</body>
</html>
