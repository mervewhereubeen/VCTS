# VCTS — Research Notes (v0.1)

## Problem Tanımı
Kemoterapi hastalarında gelişen yan etkiler çoğu zaman geç fark ediliyor. Bu proje, görsel veriler üzerinden **erken uyarı** sağlayarak komplikasyonları azaltmayı hedefliyor.

## Hedef Kullanıcı
- Onkologlar ve ilgili alanda görev yapan sağlık görevlileri
- Kemoterapi sürecindeki hastalar
- Evde bakım hizmetleri ve sağlık kuruluşları (ileride)

## Mevcut Yaklaşımlar
- Günümüzde sistemler genellikle laboratuvar testleri veya hasta beyanına dayanıyor.
- Görsel tabanlı otomatik analiz yapan sistem sayısı çok az.

## Özgün Katkı
- Hibrit yapı: klasik görüntü işleme + derin öğrenme (transfer learning / YOLO).
- Görsellerden doğrudan semptom tespiti.
- Doktor ve hasta paneline otomatik veri akışı ile gerçek zamanlı izlenim ve takip.

## Açık Sorular
- Düşük kaliteli görüntüler (ışık, açı, bulanıklık) nasıl yönetilecek?
- Farklı cilt tonları için model nasıl genelleştirilecek?
- Etik/onam süreçleri nasıl belgelenecek?
- Semptopmların öncelik sırası ne olmalı ve neden? / Hangi semptomlar öncelikli ele alınmalı (cilt solgunluğu, dudak çatlağı, mukozit)?
