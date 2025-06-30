# Hiperspektral Beyin Doku Sınıflandırma Üzerine Bir Çalışma
Bu çalışmada https://hsibraindatabase.iuma.ulpgc.es/ adresindeki veri setinden yararlanılmıştır.
Hiperspektral görüntülerde beyin doku sınıflandırmasına ait bir çalışma
  
  **hyper_isleme_raw.jpynb** dosyası Ham olan hyperspectral görüntüleri kalibre ederek belirtilen farklı bir klasöre kopyalayıp kullanıma hazır hale getirir.
    
  3 Kampanyadan elde edilen hasta görüntülerinin hepsi işlenerek her bir hasta için 4 adet image dosyası oluşturur.
  - (**calibrated_raw**) Öncelikle siyah-beyaz kalibrasyonu yapılan ve bant sayısı 826 dan 644 e indirgenen bir image dosyası oluşturulur.
  - (**calibrated_pca_128**) 644 banta düşürülmüş kalibre image dan sırası ile her 5 bantın pca sı alınarak 1 bant elde edilir. Toplamda 128 bantlık yeni bi image oluşturulur.
  - (**calibrated_par_128**) 644 banta düşürülmüş kalibre image dan sırası ile her 5. bant alınarak 1 bant elde edilir. Toplamda 128 bantlık yeni bi image oluşturulur.
  - (**calibrated_ort_128**) 644 banta düşürülmüş kalibre image dan sırası ile her 5 bantın ortalaması alınarak 1 bant elde edilir. Toplamda 128 bantlık yeni bi image oluşturulur.

**yogunluk_grafik.jpynb** dosyası işlenmiş olan hasta imagelarından sınıfların ortalama ve varyanslı spektral imza grafiklerini almak için kullanılır.

**models_trains_validates.jpynb** dosyası tasarlanan 3 adet modeli eğitime hazırlama, eğitme ve çıktılarını almak için kullanılır. Modeller tek bir hasta/kalibre image için eğitilebileceği fonksiyonlarla birlikte toplu olarakta eğitebileceği fonksiyonları içerir. Eğitilen modeller üzerinde tek tek veya topluca hasta image doğrulaması yapan fonksiyonlarda mevcuttur.
