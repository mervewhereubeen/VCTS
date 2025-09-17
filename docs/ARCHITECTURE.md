# VCTS — Architecture (v0.1)

## High-level Akış

Patient (image upload)
│
▼
Preprocess (WB / CLAHE / Normalize / ROI)
│
├─ Classic metrics (ör: LAB tabanlı paleness, edge yoğunluğu)
└─ DL inference (Transfer Learning: ResNet/MobileNet; opsiyonel YOLO ile lokal ROI)
│
Decision Fusion (ağırlıklar + eşikler)
│
├─ FastAPI (REST) → SQL (sessions/results)
└─ UI (Hasta yükleme + Doktor paneli)


## Bileşenler
- **Preprocess**: Beyaz dengesi (WB), kontrast (CLAHE), normalizasyon, ROI çıkarımı.
- **ML**: Transfer learning (ResNet/MobileNet). Gerektiğinde **YOLO** ile lokal analiz.
- **Decision**: Klasik metrik + model çıktısını birleştirip risk etiketi üretme (Düşük/Orta/Yüksek).
- **API (FastAPI)**: `/health`, `/predict`, `/sessions` (v0.1 sözleşme; uygulama sonraki sprintte).
- **DB (SQL/SQLite)**: `patients`, `sessions`, `results` temel tabloları (şema taslağı v0.1).
- **UI**: 
  - Hasta: Görsel yükleme → anlık sonuç kartı.
  - Doktor: Liste/filtre → sonuç kartları + küçük önizleme.

## Veri Akışı (özet)
1. Hasta görseli yükler (web arayüzü veya API).
2. Görsel preprocess aşamasından geçer (WB/CLAHE/ROI).
3. Klasik metrikler ve DL modeli bağımsız skor üretir.
4. Decision Fusion ile tek risk skoru/etiket çıkar.
5. Sonuçlar API üzerinden DB’ye yazılır; UI’de gösterilir.

## Dağıtım (MVP)
- Tek servis (API+UI aynı repo). 
- Veritabanı: hızlı prototip için SQLite; ölçeklenmede Postgres.
- Docker opsiyonel (ileride).

## Notlar
- Bu belge **tasarım niyeti**ni anlatır; uygulama kodu bir sonraki sprintte geliştirilecektir.
