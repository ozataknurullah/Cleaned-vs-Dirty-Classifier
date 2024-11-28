# Cleaned vs Dirty Sınıflandırma Projesi

## 📄 Proje Açıklaması
Bu proje, Kaggle'dan alınan **"Cleaned vs Dirty"** veri seti ile temiz (`cleaned`) ve kirli (`dirty`) görüntülerin sınıflandırılmasını amaçlamaktadır. Proje, temel bir CNN modeli kullanılarak gerçekleştirilmiştir.

---

## 📁 Veri Seti
- **Eğitim Verileri (Train Data):** `data/train/` dizininde bulunuyor.
- **Test Verileri (Test Data):** `data/test/` dizininde bulunuyor.
- **Etiketler (Labels):** `data/sample_submission.csv` dosyasında mevcut.

---

## 🛠️ Adımlar

### Veri Ön İşleme
- Görseller 224x224 boyutuna küçültüldü ve normalleştirildi.
- `cleaned` sınıfı için veri artırımı yapılarak modelin bu sınıfı daha iyi öğrenmesi sağlandı.

### Model Eğitimi
- Temel bir CNN modeli kullanılarak eğitim yapıldı.
- Model, sınıf dengesizliği nedeniyle `class_weights` ile desteklendi.

### Model Değerlendirmesi
- Doğruluk, confusion matrix ve sınıflandırma raporu ile değerlendirildi.
- Modelin doğruluğu %97.3 olarak hesaplandı.

---

## 🏆 Sonuçlar
- **Genel Doğruluk:** %97.3
- **Confusion Matrix:** Aşağıda belirtilmiştir:

| Gerçek (Actual) \ Tahmin (Predicted) | Cleaned | Dirty |
|--------------------------------------|---------|-------|
| **Cleaned**                         | 18      | 2     |
| **Dirty**                           | 18      | 706   |

---

## 🚀 Nasıl Çalıştırılır?

### Gereksinimler
Aşağıdaki komutla bağımlılıkları yükleyin:
```bash
pip install -r requirements.txt
```

# Kodları Çalıştırma
Veri ön işleme ve model eğitimi için src klasöründeki Jupyter Notebook'ları çalıştırın.
Sonuçları results/ klasöründen analiz edin.

📂 Dosyalar
Ana Dosyalar:
src/data_preprocessing.ipynb: Veri yükleme ve ön işleme adımları.
src/model_training.ipynb: Model oluşturma, eğitme ve değerlendirme.
requirements.txt: Kullanılan Python kütüphanelerini içerir.

Sonuçlar:
results/confusion_matrix.png: Confusion matrix görseli.
results/accuracy_plot.png: Eğitim doğruluğu ve kaybını gösteren grafikler.

🔗 Veri Seti
Veri setini şu adresten indirebilirsiniz: [Cleaned vs Dirty Dataset](https://www.kaggle.com/competitions/platesv2/data)

Veri setini data/ klasörüne şu şekilde yerleştirin:

data/train/ klasörü: Eğitim görselleri.
data/test/ klasörü: Test görselleri.
data/sample_submission.csv: Etiket dosyası.


# Cleaned vs Dirty Classification Project

## 📄 Project Description
This project aims to classify images as **cleaned** and **dirty** using the **"Cleaned vs Dirty"** dataset from Kaggle. The project was implemented using a basic CNN model.

---

## 📁 Dataset
- **Training Data:** Located in the `data/train/` directory.
- **Test Data:** Located in the `data/test/` directory.
- **Labels:** Available in the `data/sample_submission.csv` file.

---

## 🛠️ Steps

### Data Preprocessing
- Images were resized to 224x224 dimensions and normalized.
- Data augmentation was applied to the `cleaned` class to improve the model's learning.

### Model Training
- A basic CNN model was trained on the dataset.
- Class weights were used to handle the class imbalance in the dataset.

### Model Evaluation
- The model was evaluated using accuracy, confusion matrix, and classification report.
- The final model achieved 97.3% accuracy.

---

## 🏆 Results
- **Overall Accuracy:** 97.3%
- **Confusion Matrix:** As shown below:

| Actual \ Predicted | Cleaned | Dirty |
|---------------------|---------|-------|
| **Cleaned**         | 18      | 2     |
| **Dirty**           | 18      | 706   |

---

## 🚀 How to Run?

### Requirements
Install the required dependencies using the following command:
```bash
pip install -r requirements.txt
```

Running the Code
Execute the Jupyter Notebooks in the src folder for data preprocessing and model training.
Analyze the results in the results/ folder.

📂 Files
Main Files:
src/data_preprocessing.ipynb: Data loading and preprocessing steps.
src/model_training.ipynb: Model creation, training, and evaluation.
requirements.txt: Lists all Python libraries used.

Results:
results/confusion_matrix.png: Visualization of the confusion matrix.
results/accuracy_plot.png: Accuracy and loss plots.

🔗 Dataset
You can download the dataset from the following link: [Cleaned vs Dirty Dataset](https://www.kaggle.com/competitions/platesv2/data)

Place the dataset in the data/ directory as follows:

data/train/: Training images.
data/test/: Test images.
data/sample_submission.csv: Labels file.
