# NASA_SAR_PROJECT
📂 Dataset / Veri Seti

This project uses the Sentinel-1 & Sentinel-2 image pairs dataset from Kaggle.
Instead of uploading the dataset directly to this repository, you can automatically download it with KaggleHub
.

Installation
pip install kagglehub

Downloading the dataset
import kagglehub

# Download the dataset
path = kagglehub.dataset_download("requiemonk/sentinel12-image-pairs-segregated-by-terrain")

print("Path to dataset files:", path)

This will download the latest version of the dataset from Kaggle and return the local file path where it is stored.

Türkçe
Bu proje, Kaggle’daki Sentinel-1 & Sentinel-2 görüntü çiftleri veri setini kullanmaktadır.
Veri setini doğrudan bu repoya yüklemek yerine, KaggleHub
 ile otomatik olarak indirebilirsiniz.

Kurulum
pip install kagglehub

Veri setini indirme
import kagglehub

# Örnek Veri setini indir
path = kagglehub.dataset_download("requiemonk/sentinel12-image-pairs-segregated-by-terrain")

print("Veri seti dosyalarının yolu:", path)

Bu kod, Kaggle’dan veri setinin en güncel sürümünü indirir ve yerel olarak kaydedildiği klasör yolunu döndürür.
