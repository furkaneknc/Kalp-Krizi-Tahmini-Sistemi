# Kalp Hastalığı Tahmin Sistemi (Tkinter + Keras)

Tkinter arayüzlü bir **kalp hastalığı riski tahmin** uygulaması. Veri ön işleme olarak **LabelEncoding**, **StandardScaler** ve sınıf dengesizliği için **SMOTE** kullanır. Model, **Keras** ile eğitilen iki katmanlı bir yapay sinir ağıdır.

> ⚠️ **Tıbbi Uyarı:** Bu proje sadece **eğitim ve demo** amaçlıdır. Klinik karar desteği olarak kullanılamaz. Tanı ve tedavi için hekiminize danışınız.

✨ Özellikler

- Basit ve hızlı **masaüstü GUI** (Tkinter)
- **SMOTE** ile dengesiz veri yönetimi
- **StandardScaler** ile ölçeklendirme
- **Keras** tabanlı ikili sınıflandırma (sigmoid çıkış)
- Model karşılaştırma, normal değerler ve göğüs ağrısı tipi açıklamaları için bilgi pencereleri
- Tahmin sonrası **risk seviyesi** ve **yüzde skoru**



📂 Proje Yapısı
├─ app.py # Tkinter arayüzü ve model
├─ requirements.txt # Bağımlılıklar
├─ data/
│ └─ heart.csv # (Kullanıcı tarafından temin edilen veri; lisansını kontrol edin)
├─ assets/
│ └─ screenshot.png # Uygulama ekran görüntüsü
└─ README.md


🧠 Model
Ön işleme: LabelEncoder, StandardScaler
Dengeleme: SMOTE (random_state=42)
Mimari: Dense(16, relu) → Dense(1, sigmoid)
Kayıp / Metrik: binary_crossentropy / accuracy
Optimizasyon: Adam(lr=0.001)
Not: heart.csv kolon adlarının (Age, Sex, ChestPainType, ... , HeartDisease) kodda beklenenlerle uyumlu olması gerekir.


📊 Örnek Model Karşılaştırma (Uygulama içi bilgilendirme)

                      Doğruluk   Hız        Yorum
- Yapay Sinir Ağı    – ~%88.8 – Orta hız  – Yorumlaması zor
- Lojistik Regresyon – ~%85.5 – Çok hızlı – Yorumlaması çok kolay
- Random Forest      – ~%70.7 – Hızlı     – Yorumlaması kolay
- Karar Ağaçları     – ~%31.2 – Hızlı     – Yorumlaması kolay
Bu sayılar örnek/demodur; veri ve tohum değerine göre değişebilir.


## 🖼️ Ekran Görüntüsü

<img width="493" height="521" alt="k1" src="https://github.com/user-attachments/assets/3bd3dbc3-3075-491b-a3c6-e2c95d963ca1" />
<img width="620" height="655" alt="k2" src="https://github.com/user-attachments/assets/edb94e4a-fa30-49b7-8fee-33dac47ed49a" />
<img width="397" height="357" alt="k3" src="https://github.com/user-attachments/assets/1fd3d4b3-74b4-4226-b319-fbde585b4577" />
<img width="352" height="317" alt="k4" src="https://github.com/user-attachments/assets/5641be01-3147-488c-a929-c00197ee8d4d" />
<img width="388" height="342" alt="k5" src="https://github.com/user-attachments/assets/db0e3020-c0c8-4cb0-b41c-3ca568dadd4f" />


🔐 Veri ve Gizlilik

Bu depoda örnek veri paylaşılmamıştır. Kendi verinizi /data/heart.csv olarak ekleyin ve veri lisansını/mahremiyetini kontrol edin.


