# Çember Atölyesi

5. sınıf öğrencileri için kesişen çemberlerle üçgen inşa etme uygulaması. Çember ekle, yarıçapını sürgüyle değiştir, çemberleri sürükle. Merkezleri ve kesişim noktalarını doğru parçalarıyla birleştir; oluşan üçgenin çeşitkenar, ikizkenar ya da eşkenar olduğu ve nedeni anında görünür.

*made by us*

## Kazanımlarla ilişkisi

| Kazanım | Uygulamada |
|---|---|
| a) Üçgenlerin kenar özelliklerine yönelik varsayımlarda bulunur | **Varsayımlar** sekmesinde “Eğer … ise … üçgen olur” cümlesi kurulur ya da serbest yazılır |
| b) Çeşitkenar, ikizkenar ve eşkenar üçgenleri belirler | **Üçgen** sekmesi türü, kenar uzunluklarını ve hangi kenarın yarıçap olduğunu gösterir; **Kayıtlar** sekmesi bulunan türleri işaretler |
| c) Üçgenlerin özelliklerini varsayımları ile karşılaştırır | Her varsayım, kaydedilen üçgenlerle ve şu anki üçgenle karşılaştırılır; karşı örnek gösterilir |
| ç) Varsayımlarını doğrulanabilir önermeler şeklinde ifade eder | Varsayımlar “Eğer … ise …” önermesi biçiminde yazılır; durumu “Sınanmadı / Örneklerle doğrulandı / Yanlışlandı” olarak izlenir |
| d) Sunduğu önermelerin katkısını değerlendirir | Sınanan her önermenin altında “Bu önermenin katkısı ne?” seçenekleri ve “Örnek kur” düğmesi bulunur |

## Nereden açılır

- **Web:** `https://ekerem.github.io/cember-atolyesi/`
- **Android (APK):** `https://github.com/Ekerem/cember-atolyesi/releases/latest/download/cember-atolyesi.apk`

APK, internet varken web sürümünü açar; böylece web'e gelen her değişiklik uygulamaya da gelir. İnternet yoksa içine gömülü kopyayla çalışır.

## Yeni sürüm nasıl çıkarılır

1. `web/index.html` dosyasında değişikliği yap.
2. `web/index.html` içindeki `APP_VERSION` ile `web/version.json` içindeki `version` değerini aynı yeni sayıya yükselt (ör. `1.0.0` → `1.1.0`).
3. `main` dalına gönder. GitHub Actions web sayfasını yayınlar, APK'yı derler ve **Releases** bölümüne yükler.
4. Uygulamadaki **Güncellemeleri denetle** düğmesi yeni sürümü bulur.

APK'nın kendisinde (Android kodu) bir değişiklik olursa `version.json` içindeki `apkMin` değerini de yükselt; eski APK'lar "Yeni APK'yı indir" bağlantısını gösterir.

## Klasörler

| Klasör | İçerik |
|---|---|
| `web/` | Uygulamanın tamamı (tek HTML dosyası) ve `version.json` |
| `android/` | Web sayfasını gösteren küçük Android uygulaması |
| `.github/workflows/` | Otomatik yayın ve APK derleme |
| `config.json` | GitHub kullanıcı adı ve depo adı |

## İlk kurulumda bir kez

Deponun **Settings → Pages** sayfasında **Source** olarak **GitHub Actions** seç.

## Not

APK, depodaki `android/app/cember.keystore` anahtarıyla imzalanır; bu sayede yeni APK eskisinin üstüne kurulur. Okul içi dağıtım için yeterlidir; Play Store'a yüklemek için ayrı, gizli bir anahtar kullanılmalıdır.
