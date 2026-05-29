# Telekom Müşteri Kaybı (Churn) Tahmini - Kaggle Yarışması

Bu proje, bir telekom şirketinin müşterilerinin hizmeti bırakıp bırakmayacağını (churn) tahmin etmek amacıyla düzenlenen bir Kaggle yarışması için geliştirilmiştir. Projede müşteri demografik bilgileri, abonelik detayları ve kullanım alışkanlıkları içeren tabular bir veri seti kullanılmıştır.

##  Projenin Amacı
Doğru tahmin modelleri sayesinde risk altındaki müşterileri önceden belirleyerek, şirketin müşteri sadakatini artıracak proaktif stratejiler geliştirmesine yardımcı olmak.

* **Hedef Değişken:** `churn` (1: Ayrıldı, 0: Hizmette Kalıyor)
* **Değerlendirme Metriği:** ROC AUC Score

##  Kullanılan Teknolojiler ve Yöntemler
* **Dil:** Python 3.12
* **Kütüphaneler:** Pandas, NumPy, Scikit-learn, LightGBM
* **Model:** LightGBM Classifier (Gradient Boosting)
* **Doğrulama Stratejisi:** 5-Fold Stratified Cross-Validation (Veri setindeki sınıf dengesizliğini korumak ve aşırı öğrenmeyi engellemek için).

##  Modelleme ve Başarı Kriterleri
Projede veri ön işleme aşamasında kategorik değişkenler doğrudan LightGBM'in yerel kategori desteği kullanılarak optimize edilmiştir. Eksik değerler (NaN) modelin kendi algoritması içindeki karar ağacı yönlendirmeleriyle yönetilmiştir.

* **Tek Seferlik Bölme (Train-Test Split) ROC AUC Skoru:** ~0.829
* **5-Fold Cross-Validation Ortalama ROC AUC Skoru:** ~0.825

##  Projeyi Yerelde Çalıştırma
Bu projeyi kendi bilgisayarınızda çalıştırmak için aşağıdaki adımları takip edebilirsiniz:

1. Bu depoyu klonlayın:
   ```bash
   git clone [https://github.com/berna1727/telecom-churn-prediction.git](https://github.com/KULLANICI_ADINIZ/telecom-churn-prediction.git)
