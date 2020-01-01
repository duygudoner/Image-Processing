# Image-Processing
## Görüntü İşleme
*Dijital ortama aktarılmış görseller üzerinden ilgili ihtiyaca göre faydalı bilgiler elde etmek için farklı yöntemlerle özdeşleştirebilen bir yöntemdir. Görüntü işleme yöntemi, kaydedilmiş olan belirli görüntülerin işlenip mevcut resim ve grafiklerin değiştirilerek istenen verilerin elde edilmesi veya iyileştirilmesi için kullanılmaktadır.*

*Görüntü işlemede kullanılan bu yöntemlerden birisi CNN(Convolutional neural network/Evrişimsel Sinir Ağları) algoritmalarıdır. CNN,  resim tanıma için kullanılan çok etkili bir mekanizmadır.*

## CNN(Convolutional neural network/Evrişimsel Sinir Ağları)
 **Evrişimsel Sinir Ağlarının Yapısı:**
 
*Bahsedilen işlevselliği elde etmek için, CNN görüntüyü çeşitli katmanlara ayrıştırarak işler. Bu katmanlar ve amaçları şöyledir:*
    
• **Convolutional Layer (Konvolüsyon Katmanı)** — *Üzerinde işlem yapılacak görüntünün özelliklerini belirlemek için kullanılır. Bu katmanda işlenecek görüntüye filtreler uygulanarak boyutlarında küçültme yapılır. Bu boyutlandırma görüntüdeki çok düşük veya çok yüksek değerleri ortalama değere çekmek için kullanılır. Bu filtreleme ile görüntünün özellikleri hakkında bilgi edinilmiş olunur. Birçok farklı filtreleme uygulanabilir.*
    
• **Non-Linearity Layer (Doğrusal Olmayan Katman)** — *Sisteme doğrusal olmayanlığın (non-linearity) tanıtılmasının gerçekleştirildiği katmandır. Tüm katmanlar doğrusal bir fonksiyon olabildiğinden dolayı Sinir Ağı tek bir perception gibi davranır, yani sonuç, çıktıların linear kombinasyonu olarak hesaplanabilir. Diğer görüntü işleme yöntemlerinde sigmoid ve tahn gibi doğrusal olmayan fonksiyonlar kullanılır, ancak Sinir Ağı eğitiminin hızı konusunda en iyi sonucu Rectifier(ReLu) fonksiyonu verdiği için artık bu fonksiyon kullanılmaya başlanmıştır.
        ReLu Fonksiyonu f (x) = max (0, x)
İlk katmanda filtre uygulanmış görüntüdeki siyah değerler negatiftir. Relu fonksiyonu uygulandıktan sonra siyah değerler kaldırılır onun yerine 0 konur.*
    
• **Pooling (Downsampling) Layer(Havuzlama(Altörnekleme) Katmanı)** — *Ağırlık sayısını azaltır ve uygunluğu kontrol eder. Bu katman sayesinde değerler arasındaki uyumsuzluk kontrol edilir. Birçok Pooling işlemleri vardır, fakat en popüleri max pooling’dir. Yine aynı prensipte çalışan average pooling, ve L2-norm pooling algoritmalarıda vardır.*
    
• **Flattening Layer (Düzleştirme Katmanı)** — *Klasik Sinir Ağı yani son katman için giriş verilerini hazırlar. Genel olarak sinir ağları, giriş verilerini tek boyutlu bir diziden alır. Bu sinir ağındaki veriler ise Convolutional ve Pooling katmanından gelen matrislerin tek boyutlu diziye çevrilmiş halidir. Yani çok boyutlu gelen matrisler tek boyuta düşürülerek son katmana gönderilir.*
    
• **Fully-Connected Layer (Tam Bağlı Katman)** — *Verileri Flattening işleminden alır ve Sinir ağı yoluyla öğrenme işlemini geçekleştirir. Yapının en önemli ve asıl işlemin gerçekleştirildiği katmandır.*

*Kısacası CNN, sınıflandırma sorununun çözümü için standart Sinir Ağı kullanır, ancak bilgileri belirlemek ve bazı özellikleri tespit etmek için diğer katmanları kullanır.*

*Kaynak: https://medium.com/@tuncerergin/convolutional-neural-network-convnet-yada-cnn-nedir-nasil-calisir-97a0f5d34cad*
