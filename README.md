# VCTS
VCTS – Virtual Chemotherapy Tracking System

Kısa Özet

Kemoterapi sürecindeki hastalarda görülen görsel semptomları (ör. cilt solgunluğu, dudak çatlağı, ağız içi lezyonlar) görüntü işleme + derin öğrenme ile önceden belirlenmiş protokole göre analiz edip erken uyarı üretmeyi amaçlayan hibrit bir sistem.

Neden?

Evde/uzaktan takiple erken farkındalık

Klinik iş yükünü azaltma, kişiselleştirilmiş takip

Hasta ve hekim arasında otomatik veri akışı

Temel Bileşenler

Ön-işleme: Gürültü azaltma, histogram eşitleme, renk düzeltme, ROI çıkarımı

ML: Transfer learning (ResNet/MobileNet), gerektiğinde YOLO ile lokal analiz

Backend: FastAPI (REST), DB: SQL tabanlı kayıt

Arayüz: Hasta yükleme ekranı + Doktor paneli (öneri ve geçmiş)
