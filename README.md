# Hiperspektral Beyin Doku Sınıflandırma Üzerine Bir Çalışma
Bu çalışmada https://hsibraindatabase.iuma.ulpgc.es/ adresindeki veri setinden yararlanılmıştır.
Hiperspektral görüntülerde beyin doku sınıflandırmasına ait bir çalışma
  
  **hyper_isleme_raw.jpynb** dosyası ham olan hiperspektral görüntüleri kalibre ederek belirtilen farklı bir klasöre kopyalayıp kullanıma hazır hale getirir.
    
  Belirlenen hasta görüntüleri işlenerek her bir hasta için 4 adet görsel dosyası oluşturulur.
  
  - (**calibrated_raw**) Öncelikle siyah-beyaz kalibrasyonu yapılan ve bant sayısı 826 dan 644 e indirgenen bir görsel dosyası oluşturulur.
  - VK1 (**calibrated_ort_128**) 644 banta düşürülmüş kalibre görselden sırası ile her 5 bantın ortalaması alınarak 1 bant elde edilir. Toplamda 128 bantlık yeni bir görsel oluşturulur.
  - VK2 (**calibrated_par_128**) 644 banta düşürülmüş kalibre görselden sırası ile her 5. bant alınarak 1 bant elde edilir. Toplamda 128 bantlık yeni bir görsel oluşturulur.
  - VK2 (**calibrated_pca_128**) 644 banta düşürülmüş kalibre görselden sırası ile her 5 bantın pca sı alınarak 1 bant elde edilir. Toplamda 128 bantlık yeni bir görsel oluşturulur.
  
**yogunluk_grafik.jpynb** dosyası işlenmiş olan hasta görsellerinden sınıfların ortalama ve varyanslı spektral imza grafiklerini almak için kullanılır.

**models_trains_validates.jpynb** dosyası tasarlanan modeli eğitime hazırlama, eğitme ve çıktılarını almak için kullanılır. Modeller tek bir hasta/kalibre görsel için eğitilebileceği fonksiyonlarla birlikte toplu olarakta eğitebileceği fonksiyonları içerir. Eğitilen modeller üzerinde tek tek veya topluca hasta görsel doğrulaması yapan fonksiyonlarda mevcuttur.
