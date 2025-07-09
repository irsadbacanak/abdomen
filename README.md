🧠 Abdominal BT Görüntülerinde Organ ve Lezyon Tespiti 

Bu proje, bilgisayarlı tomografi (BT) taramalarındaki karın bölgesi (abdomen) görüntülerinde çeşitli anatomik yapıları (organlar) ve potansiyel lezyonları otomatik olarak tespit etmek ve sınıflandırmak için YOLOv8 tabanlı bir derin öğrenme nesne algılama modeli geliştirmeyi amaçlamaktadır.

🎯 Proje Amacı
🔹 Tıbbi görüntüleme alanında yapay zeka uygulamalarını göstermek.
🔹 Radyologların tanı süreçlerini hızlandırmak ve potansiyel hata oranlarını azaltmak.
🔹 Hastalıkların erken teşhisine ve tedavi planlamasına katkı sağlamak.
🔹 DICOM formatındaki görüntüleri işleyerek YOLO modeline uygun hale getirmek.
🔹 11 farklı tıbbi sınıfı YOLOv8 ile tespit etmek.

🌟 Özellikler
📸 DICOM'dan PNG'ye Dönüşüm
➡ DICOM formatındaki görüntüler okunur, pencereleme (windowing) uygulanarak PNG'ye dönüştürülür.

📊 Veri Analizi ve Görselleştirme
➡ Etiketli veri kümesinin sınıf dağılımı analiz edilir, sınırlayıcı kutular görsellerle birlikte gösterilir.

🚀 YOLOv8 Entegrasyonu
➡ Ultralytics mimarisi kullanılarak yüksek performanslı model eğitimi sağlanır.

🗂 Veri Seti Hazırlığı
➡ Eğitim/Doğrulama/Test setlerine ayrılır, data.yaml dosyası oluşturulur.

📈 Model Eğitimi ve Değerlendirme
➡ Hiperparametrelerle eğitim yapılır, mAP, Precision, Recall gibi metrikler hesaplanır.

🧠 Ensemble Tahmin (Opsiyonel)
➡ Birden fazla modelin tahminleri ortalanarak daha kararlı sonuçlar elde edilir.

💾 Google Drive Entegrasyonu
➡ Eğitim sonuçları ve veri seti Drive’a otomatik olarak yedeklenir.

🧰 Kullanılan Teknolojiler
🐍 Python 3.x

🧪 pydicom, opencv-python, numpy, pandas

📊 matplotlib, seaborn

🔁 tqdm, yaml

🧠 ultralytics (YOLOv8)

⚙️ Kurulum ve Çalıştırma
📂 Google Colab'da Açın
→ abdomen.py dosyasını yükleyin.

📦 Kütüphaneleri Yükleyin
!pip install pydicom opencv-python pandas matplotlib seaborn tqdm ultralytics PyYAML
🔗 Google Drive’ı Bağlayın
from google.colab import drive
drive.mount('/content/drive')
📁 Verileri Yerleştirin

DICOM’lar → /content/drive/MyDrive/abdomen/images_raw

Etiketler → Bilgi.xlsx (sayfa adı: TRAININGDATA)

▶️ Betiği Çalıştırın

Tüm hücreleri çalıştırarak sıralı işlem başlatın.

🧪 Otomatik İşlem Adımları
✅ DICOM Dönüşümü
✅ Veri Analizi ve Görselleştirme
✅ Veri Seti Hazırlığı
✅ Model Eğitimi
✅ Test Üzerinde Değerlendirme
✅ (Opsiyonel) Ensemble
✅ Google Drive’a Kayıt

📊 Sonuçlar ve Performans
📂 runs/detect/<model_tag>/ dizininde:

Eğitim kayıpları (loss)

mAP eğrileri

Precision–Recall grafikleri
ve daha fazlası grafikler ve results.csv olarak kaydedilir.

🤝 Katkıda Bulunma
Bu proje geliştirilmeye açıktır!
🛠️ Pull request gönderebilir veya bir issue açarak katkı sağlayabilirsiniz.
Her katkı, klinik yapay zekâ uygulamaları için büyük bir adımdır.

