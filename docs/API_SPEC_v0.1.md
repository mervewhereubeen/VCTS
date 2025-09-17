 VCTS — API Specification (v0.1)

/health (GET)
- **Amaç**: Servisin ayakta olduğunu göstermek.
- **Response (200 OK)**:
  
```json

{ "status": "ok", "version": "0.1" }



/predict (POST, multipart/form-data)

Body: image (jpeg/png)

Response (örnek):
{
  "request_id": "12345",
  "preprocess": {"wb": true, "clahe": true},
  "metrics": {"paleness": 0.67},
  "dl": {"model": "mobilenet_v2", "prob_solgun": 0.72},
  "decision": {"risk": "orta", "score": 0.70}
}

/sessions?patient_id= (GET)

Amaç: Belirli bir hasta için geçmiş oturumları listelemek.

Response (örnek):
[
  {"id": 1, "date": "2025-09-17", "risk": "orta"},
  {"id": 2, "date": "2025-09-18", "risk": "yüksek"}
]


