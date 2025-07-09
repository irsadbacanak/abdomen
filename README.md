Abdominal BT Görüntülerinde Organ ve Lezyon Tespiti
Bu proje, bilgisayarlı tomografi (BT) taramalarındaki karın bölgesi (abdomen) görüntülerinde çeşitli anatomik yapıları (organlar) ve potansiyel lezyonları otomatik olarak tespit etmek ve sınıflandırmak için derin öğrenme tabanlı bir nesne algılama modeli (YOLOv8) geliştirmeyi amaçlamaktadır.

🚀 Proje Amacı
Projenin temel hedefleri:

Tıbbi görüntüleme alanında yapay zeka uygulamalarını göstermek.

Radyologların tanı süreçlerini hızlandırmak ve potansiyel hata oranlarını azaltmak.

Hastalıkların erken teşhisine ve tedavi planlamasına katkıda bulunmak.

DICOM formatındaki tıbbi görüntüleri işleyerek YOLO modeline uygun hale getirmek.

Eğitilmiş bir nesne algılama modeli ile karın bölgesindeki 11 farklı tıbbi sınıfı tespit etmek.

🌟 Özellikler
DICOM'dan PNG'ye Dönüşüm: DICOM formatındaki tıbbi görüntüleri okunabilir PNG formatına dönüştürme ve pencereleme (windowing) uygulama.

Veri Analizi ve Görselleştirme: Etiketlenmiş veri setindeki sınıf dağılımını analiz etme ve sınırlayıcı kutuların görüntüler üzerinde görselleştirilmesi.

YOLOv8 Entegrasyonu: Ultralytics YOLOv8 mimarisini kullanarak nesne algılama modeli eğitimi.

Veri Seti Hazırlığı: Eğitim, doğrulama ve test setlerine ayrılma ve YOLO formatına uygun data.yaml dosyasının oluşturulması.

Model Eğitimi ve Değerlendirmesi: Hiperparametre ayarları ile model eğitimi ve mAP gibi standart metriklerle performans değerlendirmesi.

Ensemble Tahmin: Birden fazla modelin tahminlerini birleştirerek daha sağlam sonuçlar elde etme (isteğe bağlı/geliştirme aşamasında).

Google Drive Entegrasyonu: İşlenen verilerin ve eğitilmiş modellerin Google Drive'a kalıcı olarak kaydedilmesi.
Teknolojiler
Python 3.x

pydicom: DICOM dosyalarını okumak ve işlemek için.

opencv-python (cv2): Görüntü işleme ve kaydetme işlemleri için.

numpy: Sayısal işlemler için.

pandas: Veri analizi ve Excel dosyalarını işlemek için.

matplotlib & seaborn: Veri görselleştirme ve grafikleri oluşturma için.

tqdm: İşlem ilerlemesini göstermek için.

ultralytics: YOLOv8 modeli eğitimi ve çıkarımı için.

PyYAML (veya dahili yaml kütüphanesi): data.yaml dosyalarını oluşturmak ve işlemek için.

Kurulum ve Çalıştırma
Google Colab'da Açın: Bu proje, Google Colab ortamında çalıştırılmak üzere tasarlanmıştır. abdomen.py dosyasını Colab'a yükleyin.

Gerekli Kütüphaneleri Yükleyin:
!pip install pydicom opencv-python pandas matplotlib seaborn tqdm ultralytics PyYAML
Google Drive Bağlantısı: Colab ortamında Google Drive'ınızı bağlayın:
from google.colab import drive
drive.mount('/content/drive')
Veri Hazırlığı:

Ham DICOM dosyalarınızı /content/drive/MyDrive/abdomen/images_raw dizinine yerleştirin.

Etiketleme bilgilerinizi içeren Bilgi.xlsx dosyasını (TRAININGDATA adlı bir sayfa içermelidir) projenin çalıştığı ana dizinde (veya erişilebilir bir yolda) bulundurun.

Betiği Çalıştırın: abdomen.py betiğini Colab'da sırayla veya tüm hücreleri çalıştırarak çalıştırın.

📝 Kullanım
Betiği çalıştırdıktan sonra aşağıdaki ana adımlar otomatik olarak gerçekleştirilecektir:

DICOM Dönüşümü: images_raw dizinindeki DICOM dosyaları images_png dizinine PNG olarak kaydedilecektir.

Veri Analizi ve Görselleştirme: Bilgi.xlsx dosyası okunacak, sınıf dağılımı grafiği oluşturulacak ve etiketli görüntüler rastgele seçilerek sınırlayıcı kutularla birlikte gösterilecektir.

Veri Seti Hazırlığı: Görüntüler ve etiketler eğitim, doğrulama ve test setlerine ayrılacak, dataset_abdomen klasörüne kopyalanacak ve bir data.yaml dosyası oluşturulacaktır.

Model Eğitimi: YOLO modeli, hazırlanan veri seti üzerinde belirtilen hiperparametrelerle eğitilecektir. Eğitim sonuçları runs/detect/ dizinine kaydedilecektir.

Model Değerlendirme: Eğitilmiş model, test seti üzerinde değerlendirilecek ve performans metrikleri (mAP, Precision, Recall) çıktıda gösterilecektir.

Ensemble Tahmini: (Eğer aktifse) Birden fazla tahmin birleştirilecek ve ensemble_output dizinine kaydedilecektir.

Kaydetme: Eğitilmiş model ağırlıkları (best.pt) ve nihai veri seti (dataset_final), Google Drive'daki ilgili dizinlere kalıcı olarak kaydedilecektir.
Sonuçlar ve Performans
Model eğitimi tamamlandıktan sonra, runs/detect/<model_tag>/ dizininde eğitim metriklerini (kayıp grafikleri, mAP eğrileri vb.) gösteren çeşitli grafikler ve tablolar bulacaksınız. Konsol çıktısında ise test seti üzerindeki nihai mAP değerleri görüntülenecektir.
Katkıda Bulunma
Proje geliştirmeye açık olup, her türlü katkı (kod, hata raporu, özellik önerisi) memnuniyetle karşılanır. Lütfen bir pull request oluşturmaktan veya bir issue açmaktan çekinmeyin.
