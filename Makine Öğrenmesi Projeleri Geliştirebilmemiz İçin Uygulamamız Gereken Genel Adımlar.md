# Makine Öğrenmesi Projeleri Geliştirebilmemiz İçin Uygulamamız Gereken Genel Adımlar

## Problemin Belirlenmesi ve Verilerin Toplanması
Problemimize göre ham verilerin elde edildiği bölümdür. Bu veriler; web verilerinden, sensör verilerinden, deney verilerinden, araştırmalardan vb. yollardan elde edilebilir. Kişisel verilerle ilgileniyorsanız toplanan veriler, yetkisiz kişilerin erişimine açılmamalı ve kişilik haklarını ihlal etmemelidir.

***Patika.dev platformunda anlık olarak 1200 kullanıcının aktif olması bir veri örneğidir. Fakat, 'Bu platformda kullanıcılar en çok 22:00 ve 02:00 saatleri arasında aktiftir.' bir bilgidir.***

## Verilerin Hazırlanması
Veri setinin hazırlanması için verilerin seçilmesi (Veri setinin içinde problemimize uygun bağımsız değişkenlerimizin belirlenmesi), temizlenmesi (Veri setimizin grafiğini çizdirdiğimizde ve incelendiğimizde az sayıda veri grafiğimizi bozuyorsa, çalıştığımız probleme uygun olarak o veriyi temizleyebiliriz.), formatının uygunluğu (Örneğin, kullandığımız veri setinde hasta,sağlıklı gibi metin formatında veriler olabilir.  Scikit-learn bunu bilemeyeceğinden 0, 1 şeklinde bilebileceği uygun formata getirmeliyiz.) vb. durumlar gözden geçirilir. 

***Veri hazırlama süreci her bir veri seti için projenin amacına göre değişiklik 
göstermektedir.***

## Modelin Seçilmesi ve Eğitilmesi
Problem çözümü için kullanılacak olan makine öğrenmesi modeli kullanılacak olan veri setinin özelliğine göre seçilmelidir.Örneğin, bağımlı değişkenleriniz ve bağımsız değişkenleriniz varsa Gözetimli Öğrenme (Supervised Learning) modellerini kullanmalısınız. Eldeki veri setinin büyük bir kısmı eğitim seti olarak kullanılır ve model eğitilir. İlk aşamada en doğru modeli seçmek zor olacaktır bu nedenle en uygununu bulabilmek için denemeliyiz. (Kullandığımız modellerin çalışma mantığını bilmek bize kolaylık sağlayabilir.)

## Modelin Değerlendirilmesi
Gerçek değerlerin olduğu test verileri ile eğitim verileri karşılaştırılarak modelimizin performansı değerlendirilir. Sadece Doğruluk (Accuracy) değerine bakılmamalı (Örneğin, veri setimde 990 tane sağlıklı 10 tane hasta verisi var. Test veri setinde hasta verisini kaçırabilirim.), problemin türüne göre diğer başarı (Kesinlik (Precision), Duyarlılık (Recall), F1 Skor (F1 Score)) kriterlerine de bakılmalıdır.

## Modelin Geliştirilmesi
Bir modelin tam performansını (Tahmin gücünü arttırmak ya da modeli daha hızlı hale getirebilmek.) alabilmek için problemimize uygun hiper-parametre değerlerini seçmeliyiz. Hiper-parametre probleme, veri setine, donanıma bağlı değişkenlik gösterebilir.
