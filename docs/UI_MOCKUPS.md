VCTS — UI Mockups (v0.1)

Bu doküman; Hasta Yükleme ve Doktor Paneli ekranlarının düşük sadakat (low-fi) taslaklarını, akışını ve durumlarını tarif eder.

1) Hasta — Görsel Yükleme & Sonuç Kartı
+---------------------------------------------------------------+
|  VCTS — Virtual Chemotherapy Tracking System                  |
+---------------------------------------------------------------+
|  [ Yeni Görsel Yükle ]  (jpg/png)                             |
|                                                               |
|  Önizleme Alanı:                                              |
|  +---------------------------------------------------------+  |
|  |  (Seçilen görsel küçük önizleme)                       |  |
|  +---------------------------------------------------------+  |
|                                                               |
|  [ İşle ]  ->  (loader/spinner)                               |
|                                                               |
|  Sonuç Kartı (işlem sonrası):                                 |
|  +---------------------------------------------------------+  |
|  |  Risk: YÜKSEK / ORTA / DÜŞÜK                            |  |
|  |  Skor: 0.70                                             |  |
|  |  Not: Aydınlatma düşükse yeniden çekiniz.               |  |
|  |  Zaman: 2025-09-17 21:10                                |  |
|  +---------------------------------------------------------+  |
|                                                               |
|  [ Yeni Görsel ]     [ Yardım / Çekim Rehberi ]               |
+---------------------------------------------------------------+


Durumlar

Boş → görsel seçilmemiş

Yükleniyor → spinner

Başarılı → risk etiketi + skor + kısa öneri

Hata → “Yüz tespit edilemedi / ışık yetersiz” uyarısı

Çekim Rehberi (kısa)

Doğal ışık, nötr arka plan, kamera sabit

Yüz tam karşıdan; ağız/dudak için yakın plan

2) Doktor — Panel & Listeleme
+---------------------------------------------------------------+
|  VCTS — Doctor Dashboard                                      |
+---------------------------------------------------------------+
|  Sol Panel (Filtreler)              |  Sağ Panel (Seçili Hasta)|
|  ---------------------------------  |  ------------------------|
|  [Arama] [Tarih] [Risk]             |  Hasta: #PT-001          |
|  Hasta Listesi:                     |  Sonuçlar (son 10):      |
|   • #PT-001  (2 uyarı)              |   2025-09-17 | ORTA      |
|   • #PT-002                         |   2025-09-15 | DÜŞÜK     |
|   • #PT-003                         |   2025-09-12 | YÜKSEK    |
|                                     |  Kayıt Detayı:           |
|  Üst Uyarılar:                      |  +---------------------+  |
|   ! #PT-012 — YÜKSEK (24s)          |  | Önizleme (küçük)   |  |
|   ! #PT-034 — YÜKSEK (48s)          |  | Risk: ORTA | 0.70  |  |
|                                     |  | Not: Işık düşük…   |  |
|                                     |  +---------------------+  |
+---------------------------------------------------------------+


Eylemler

Sol listeden hasta seç → sağ panel güncellenir

Filtreler: tarih aralığı, risk düzeyi

Detayda küçük görsel önizleme

3) Kullanıcı Akışları (özet)

Hasta: Görsel yükle → İşle → Sonuç kartını gör → Gerekirse rehber → Yeni görsel
Doktor: Üst uyarılara bak → Hasta seç → Son 10 kayıt → Detay incele

4) Durum/Boş Hali Mesajları

Boş Liste: “Bu aralıkta kayıt yok.”

Ağ Hatası: “Sunucuya ulaşılamıyor. Lütfen tekrar deneyin.”

Geçersiz Format: “Sadece .jpg/.png kabul ediliyor.”

5) Erişilebilirlik (A11y) Notları

Butonlar klavye ile erişilebilir olmalı

Risk etiketi yalnız renk değil ikon + metin ile de ifade edilmeli (örn. YÜKSEK !)

Görsel alt metni: “Yüz önizleme — tarih/saat”

6) Tema (MVP)

Basit, kontrastı yüksek, kart tabanlı

Başlıklar H2/H3; içerikte düzenli listeler

Primary buton: “İşle” / “Filtrele”
