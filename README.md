# 📞 Telco Customer Churn Prediction & Business Intelligence

## 📌 Proje Özeti
Bu proje, telekomünikasyon sektöründeki müşteri kayıplarını (churn) önceden tahmin etmek ve makine öğrenmesi modeli çıktılarını veriye dayalı iş kararlarına (Business Intelligence) dönüştürmek amacıyla geliştirilmiştir. Yalnızca yüksek Accuracy elde eden bir model kurmak yerine, şirket için asıl maliyet yaratan "gerçekte ayrılacak müşterileri (False Negative) gözden kaçırma" problemine odaklanılmış ve **Recall** metriği optimize edilmiştir.

## 🎯 İş Problemi ve Yaklaşım
Müşteri kazanım maliyetlerinin (CAC), müşteriyi elde tutma (Retention) maliyetlerinden çok daha yüksek olduğu gerçeğinden yola çıkarak;
* Dengesiz sınıf (Imbalanced Data) problemi analiz edildi.
* Lojistik Regresyon algoritması ile `class_weight='balanced'` yaklaşımı uygulandı.
* `GridSearchCV` kullanılarak optimizasyon hedefi Accuracy'den **Recall** değerine kaydırıldı.
* Model çıktıları, şirketin pazarlama ve müşteri ilişkileri departmanlarının kullanabileceği "Risk Skorlaması" mantığına dönüştürüldü.

## 📈 Elde Edilen Temel Sonuçlar
* **Baseline Model Recall:** %51
* **Optimize Edilmiş Model Recall:** %80
* **ROC-AUC Skoru:** 0.83
* *İş Etkisi:* Churn riski taşıyan müşterileri yakalama oranı optimize edilerek, şirketin proaktif retention kampanyaları düzenlemesine olanak sağlandı.

## 🛠️ Kullanılan Teknolojiler
* **Programlama Dili:** Python
* **Veri Manipülasyonu:** Pandas, NumPy
* **Makine Öğrenmesi:** Scikit-Learn (Logistic Regression, GridSearchCV, MinMaxScaler)
* **Veri Görselleştirme:** Matplotlib, Seaborn

## 📂 Klasör Yapısı
* `data/` : Projede kullanılan veri setini barındırır.
* `Telco_Customer_Churn_Prediction.ipynb` : Keşifçi Veri Analizi (EDA), veri ön işleme, model eğitimi ve iş zekası yorumlamalarını içeren ana çalışma dosyasıdır.

## 📝 Medium Makalesi
Bu projenin adım adım nasıl geliştirildiğini, kodların arkasındaki iş mantığını ve istatistiksel sonuçların şirket stratejilerine nasıl entegre edilebileceğini detaylıca anlattığım Medium makaleme buradan ulaşabilirsiniz:
👉 https://medium.com/@yusufgungor997/makine-%C3%B6%C4%9Frenmesi-ile-m%C3%BC%C5%9Fteri-kayb%C4%B1n%C4%B1-churn-%C3%B6nlemek-u%C3%A7tan-uca-lojistik-regresyon-projesi-4eddcccb5a46

## 👨‍💻 Geliştirici
**Yusuf Erdem Güngör** 
Veri Bilimi ve Yapay Zeka alanında çalışmalar yapıyorum. Geri bildirimleriniz ve iletişim için benimle bağlantı kurabilirsiniz.
