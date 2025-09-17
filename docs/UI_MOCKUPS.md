# VCTS — UI Mockups (v0.1)

Bu belge, **Hasta Yükleme** ve **Doktor Paneli** ekranlarının düşük sadakat (low-fi) taslağını **düz metin** ile tarif eder. Amaç: “ne üretilecek” sorusuna net ve sade cevap vermek.

---

## 1) Hasta — Görsel Yükleme & Sonuç Kartı

**Ekran yapısı**
- Üst başlık: “VCTS — Virtual Chemotherapy Tracking System”
- Birincil buton: **Yeni Görsel Yükle (jpg/png)**
- Önizleme alanı: seçilen görselin küçük önizlemesi
- Birincil buton: **İşle** (yükleme/işleme başlatır)
- Sonuç kartı:
  - **Risk:** YÜKSEK / ORTA / DÜŞÜK
  - **Skor:** ör. 0.70
  - **Açıklama:** ör. “Aydınlatma düşükse yeniden çekiniz.”
  - **Zaman damgası**

**Durumlar**
- Boş: görsel seçilmedi
- Yükleniyor: işlem sırasında loader/spinner
- Başarılı: risk etiketi + skor + kısa öneri
- Hata: “Yüz tespit edilemedi / ışık yetersiz” → “Çekim Rehberi”ne yönlendirme

**Çekim Rehberi (kısa)**
- Doğal ışık, nötr arka plan, kamera sabit
- Yüz tam karşıdan; ağız/dudak için yakın plan

---

## 2) Doktor — Panel & Listeleme

**Sayfa bölümleri**
- Sol panel (filtreler):
  - Arama kutusu
  - Tarih aralığı seçimi
  - Risk filtresi (Düşük/Orta/Yüksek)
  - Hasta listesi (ID + uyarı sayısı)
- Üst uyarılar (yüksek riskli son kayıtlar)
- Sağ panel (seçili hasta):
  - Son 10 sonuç (tarih | risk)
  - Kayıt detayı: küçük görsel önizleme, risk/skor, kısa not

**Eylemler**
- Listeden hasta seç → sağ panel güncellenir
- Filtrelere göre liste ve sonuçlar yenilenir
- Kayıt detayında küçük önizleme görüntülenir

---

## 3) Kullanıcı Akışları (özet)

**Hasta akışı**
1. Görsel yükle
2. İşle → Sonuç kartını gör
3. Gerekirse “Çekim Rehberi”
4. Yeni görsel yükle

**Doktor akışı**
1. Paneli aç → Üst uyarılara bak (YÜKSEK risk)
2. Hasta seç → Son 10 kaydı gör
3. Kayıt detayını aç → önizleme + not

---

## 4) Durum/Boş Hali Mesajları
- Boş liste: “Bu aralıkta kayıt yok.”
- Ağ hatası: “Sunucuya ulaşılamıyor. Lütfen tekrar deneyin.”
- Geçersiz format: “Sadece .jpg/.png kabul ediliyor.”

## 5) Erişilebilirlik (A11y) Notları
- Tüm butonlar klavye ile erişilebilir olmalı
- Risk etiketi sadece renkle değil **ikon + metin** ile de belirtilmeli (ör. “YÜKSEK ⚠”)
- Görsel `alt` metni: “Yüz önizleme — tarih/saat”

## 6) Tema (MVP)
- Basit, yüksek kontrastlı, kart tabanlı düzen
- Başlıklar H2/H3; içerik listeler ve net etiketler
- Primary butonlar: “İşle” (hasta), “Filtrele” (doktor)
