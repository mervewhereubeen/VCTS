# VCTS — Risk Register (v0.1)

| ID  | Risk                          | Olasılık | Etki   | Mitigasyon                                      |
|-----|-------------------------------|----------|--------|------------------------------------------------|
| R1  | Düşük kaliteli görüntü (ışık, blur) | Orta     | Yüksek | WB/CLAHE, “yeniden çek” uyarısı               |
| R2  | ROI hatası (yüz/dudak tespiti)       | Orta     | Orta   | Alternatif yöntem, fallback                    |
| R3  | Aşırı uyum (overfitting)             | Orta     | Orta   | Data augmentation, erken durdurma, validasyon |
| R4  | Gizlilik / etik / onam sorunları     | Düşük    | Yüksek | Anonimleştirme, açık rıza, veri politikası     |
| R5  | Klinik doğrulama gecikmesi           | Orta     | Yüksek | Pilot çalışma planı, uzman görüşleri           |
| R6  | API güvenliği                        | Düşük    | Orta   | JWT, hız limiti, loglama                       |
