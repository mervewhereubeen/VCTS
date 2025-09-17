# VCTS — Roadmap (v0.1)

## Kısa Vade (0–2 Hafta)
- Dokümantasyon ve mimari taslakların tamamlanması.
- Basit ön-işleme denemeleri (ör: histogram eşitleme, beyaz dengesi).
- FastAPI iskeleti (sadece `/health` endpoint).
- Küçük örnek veri seti hazırlığı (placeholder).

## Orta Vade (1.5–2.5 Ay)
- Transfer learning (ResNet / MobileNet) ile ilk prototip model.
- Doktor panelinde geçmiş sonuçların listelenmesi ve grafik gösterimi.
- Eşik / karar birleştirme kalibrasyonu (paleness skoru + model çıktısı).
- Basit güvenlik: JWT tabanlı oturum açma.

## Uzun Vade (4–6 Ay)
- YOLO tabanlı lokal tespit (ör: dudak çatlağı, mukozit alanları).
- Zaman serisi modelleme (LSTM) ile semptom ilerleyiş tahmini.
- Klinik pilot testler ve kullanıcı geri bildirimine göre iterasyon.
- Postgres veritabanına geçiş + Docker ile dağıtım.
- Mobil uygulama entegrasyonu (ileri faz).
