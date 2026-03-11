# 🔔 ObjectAlarm

Alarmı kapatmak için fiziksel bir nesneyi kameraya göstermeniz gereken akıllı Android alarm uygulaması.  
Artık alarmı kapatıp tekrar uyumak yok — kalkıp nesneyi bulmak zorundasınız! 😄

---

## 📱 Uygulama Hakkında

**ObjectAlarm**, kullanıcıların alarm kurarken bir hedef nesne (örn. banyodaki sabunluk, mutfak masasındaki bardak) belirlemesine olanak tanır. Alarm çaldığında, yalnızca o nesneyi kameraya göstererek alarmı durdurabilirsiniz.

### Nasıl Çalışır?
1. Alarm kurulurken kamera ile bir nesne taranır ve kaydedilir
2. Alarm çaldığında ekran açılır ve kamera aktif olur
3. Kullanıcı kayıtlı nesneyi kameraya gösterir
4. AI nesneyi tanır → alarm durur ✅

---

## ✨ Özellikler

- ⏰ Tekrarlayan alarm desteği (Pzt–Paz)
- 🤖 AI destekli nesne tanıma (ML Kit)
- 📷 Gerçek zamanlı kamera önizlemesi
- 🔒 Kilitli ekranda alarm açılır
- 🌙 Dark mode desteği
- 📳 Titreşim + özel zil sesi

---

## 🛠️ Teknoloji Stack

| Katman | Teknoloji |
|---|---|
| Dil | Kotlin |
| Mimari | MVVM + Clean Architecture |
| DI | Hilt |
| Veritabanı | Room |
| Kamera | CameraX |
| AI / Nesne Tanıma | ML Kit Object Detection |
| Async | Kotlin Coroutines + Flow |
| Min SDK | API 26 (Android 8.0) |
| Target SDK | API 35 (Android 15) |

---

## 🚀 Kurulum

### Gereksinimler
- Android Studio Hedgehog veya üzeri
- JDK 17
- Android SDK API 35

### Adımlar

```bash
# Repoyu klonla
git clone https://github.com/kullanici-adi/objectalarm.git
cd objectalarm
```

1. Android Studio'da projeyi açın
2. Firebase kullanılıyorsa `google-services.json` dosyanızı `app/` klasörüne koyun
3. `local.properties` dosyasının doğru SDK yolunu gösterdiğinden emin olun
4. **Run** ▶️ butonuna basın

---

## 📁 Proje Yapısı

```
app/src/main/java/com/yourpackage/objectalarm/
│
├── data/
│   ├── local/              # Room veritabanı ve DAO
│   ├── model/              # Alarm, RecognitionObject veri sınıfları
│   └── repository/         # Repository implementasyonları
│
├── domain/
│   ├── usecase/            # İş mantığı use case'leri
│   └── repository/         # Repository interface'leri
│
├── presentation/
│   ├── alarm/              # Alarm listesi ekranı
│   ├── setup/              # Nesne kayıt ekranı
│   └── dismiss/            # Alarm kapatma ekranı
│
├── service/
│   ├── AlarmReceiver.kt    # BroadcastReceiver
│   └── AlarmService.kt     # Foreground Service
│
└── ml/
    └── ObjectRecognizer.kt # ML Kit wrapper
```

---

## 👥 Geliştirme Ekibi

| İsim | Rol | İşletim Sistemi |
|---|---|---|
| Emin| Geliştirici | macOS |
| [Maho | Geliştirici | Windows |

---

## 🤝 Katkı Sağlama

```bash
# Yeni bir branch oluştur
git checkout -b feature/ozellik-adi

# Değişikliklerini commit'le
git commit -m "feat: yeni özellik eklendi"

# Branch'i push'la
git push origin feature/ozellik-adi

# Pull Request aç
```

### Commit Mesajı Formatı
```
feat:     yeni özellik
fix:      hata düzeltme
refactor: kod iyileştirme
docs:     dokümantasyon
style:    UI değişikliği
test:     test ekleme
```

---

## ⚠️ Önemli Notlar

- `google-services.json` dosyasını **asla** commit'lemeyin
- `.jks` / `.keystore` imza dosyalarını **asla** commit'lemeyin
- Büyük ML model dosyaları (`.tflite`) için **Git LFS** kullanın:
  ```bash
  git lfs install
  git lfs track "*.tflite"
  ```

---

## 📄 Lisans

```
MIT License — Dilediğiniz gibi kullanabilirsiniz.
```
