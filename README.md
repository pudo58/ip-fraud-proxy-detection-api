# IP Fraud & Proxy Detection API

🔐 **Real-time IP intelligence API** for detecting **proxy, VPN, hosting, and high-risk IP addresses**.  
Built to help developers **prevent fraud, bots, fake signups, and abuse** by analyzing IP reputation, ASN, and network signals.

👉 **Live on RapidAPI:**  
https://rapidapi.com/tholv-tholv-default/api/ip-fraud-proxy-detection-api

🌐 **Official website:**  
https://ipdeepcheck.com

---

## 🚀 Features

- ✅ Proxy & VPN detection  
- ✅ Hosting / cloud IP identification  
- ✅ Fraud risk score (0–100)  
- ✅ ASN & ISP information  
- ✅ Reverse DNS analysis  
- ✅ Fast & lightweight JSON responses  
- ✅ Free tier & Pro tier available  

---

## 🧠 How It Works

This API combines multiple **network intelligence signals**:

- ASN ownership & ISP data
- Hosting / cloud provider fingerprints
- Reverse DNS pattern analysis
- Heuristic risk scoring
- Offline-first classification with cache optimization

⚡ Designed for **low latency**, **high throughput**, and **minimal external dependency**.

---

## 📦 API Endpoint

### Detect IP Reputation

## GET /api/v1/ip/check


### Query Parameters

| Name | Type | Required | Description |
|----|----|----|----|
| `ip` | string | ✅ | IPv4 or IPv6 address to analyze |

---

### Example Request

```bash
curl -X GET \
  "https://ipdeepcheck.com/api/v1/ip/check?ip=8.8.8.8" \
  -H "X-API-Key: YOUR_API_KEY"
```
## 📄 Example Response (Pro Plan)
```json
{
  "ip": "8.8.8.8",
  "type": "PUBLIC",
  "is_proxy": false,
  "is_vpn": false,
  "is_hosting": true,
  "risk_score": 12,
  "asn": "15169",
  "organization": "Google LLC",
  "country": "US",
  "confidence": 0.98,
  "method": "ASN + DNS + Heuristic"
}
```
