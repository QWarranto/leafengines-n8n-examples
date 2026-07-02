
## 🎯 QGIS Plugin Officially Approved!

## ⚡ Get Started Now

**Free tier — no signup, no credit card:**
- **Test key:** `leaf-test-370df0a2e62e` (works immediately)
- **Free header:** `x-free-tier: true` (no key needed)

**Ready for production?**
- [Starter — $149/mo →](https://buy.stripe.com/5kQ6oHcB88bR93s8MSaMU04)
- [Pro — $499/mo →](https://buy.stripe.com/14A6oH7gO3VBcfE1kqaMU05)

**Partner Program:** Stop building for free. Use our API to sell $100–200 soil reports to local farmers, drone pilots, and GIS communities. You buy each report for $25. [Join our Partner Program →](https://soilcertify.com)

**Preliminary Site Scan - SoilCertify**
Quick geotechnical overview with essential soil data and basic risk indicators.
https://buy.stripe.com/fZu00j44C0Jp4Nc3syaMU0f
---

**Plugin ID:** 4987 (LeafEngines Agricultural Intelligence)  
**Version:** 1.0.2 Experimental  
**Status:** ✅ **PUBLICLY AVAILABLE**  
**Download:** https://plugins.qgis.org/plugins/qgis_leafengines/version/1.0.2/download/

### Key Features:
- **USDA soil data** - Soil composition, pH, N/P/K recommendations
- **EPA water quality** - Water quality metrics and analysis
- **Satellite vegetation indices** - NDVI, water-stress overlays from NASA MODIS
- **AI-powered crop recommendations** - Tailored to exact field polygons
- **Carbon credit calculations** - Environmental impact scoring
- **Offline-first architecture** - Works in remote/"deep canopy" areas

### Strategic Advantages for Partners:
1. **Pre-vetted, low-risk integration** - Officially approved by QGIS after rigorous review
2. **Seamless future-proofing** - Aligns with QGIS release cycles (QGIS 4.0.0+ ready)
3. **Instant credibility** - Discoverable by 500,000+ QGIS users in agriculture sector
4. **Regulatory advantage** - Preferred for government/EPA/USDA-related procurements
5. **Ecosystem power** - Integrates with thousands of complementary QGIS plugins

### For OEM Partners:
Embed LeafEngines agricultural intelligence directly into your hardware or software platforms with confidence. The official QGIS approval eliminates weeks of custom validation, security audits, and compatibility testing.

*Approved: April 14, 2026*


# LeafEngines n8n Examples

> 🏆 **Global Startup Awards 2026 — North America Regional Nominee**

Example workflows and documentation for the LeafEngines Agricultural Intelligence n8n node.

## 📦 Installation
```bash
npm install n8n-nodes-leafengines
```

## 📖 Documentation

### Available Nodes
- **LeafEngines Soil** - USDA soil composition analysis
- **LeafEngines Environmental Intelligence** - Multi-source environmental scoring

### Credential Setup
1. Go to **Credentials** → **Add Credential** in n8n
2. Search for "LeafEngines"
3. Enter API key: **`leaf-test-370df0a2e62e`** (test key - works immediately)

**Free Tier Option:** Leave API key empty and use header `x-free-tier: true`

**Production API Key:** Request from [SoilSidekick Pro](https://soilsidekickpro.com/api-docs)

## 🚀 Example Workflows

### 1. Basic Soil Analysis
```json
{
  "nodes": [
    {
      "name": "Schedule Trigger",
      "type": "n8n-nodes-base.scheduleTrigger",
      "parameters": {"rule": {"interval": "weekly"}}
    },
    {
      "name": "LeafEngines Soil",
      "type": "n8n-nodes-leafengines.leafenginesSoil",
      "parameters": {"county": "Fulton", "state": "GA"}
    },
    {
      "name": "Google Sheets",
      "type": "n8n-nodes-base.googleSheets",
      "parameters": {"operation": "append"}
    }
  ]
}
```

### 2. Environmental Impact Assessment
```json
{
  "nodes": [
    {
      "name": "Webhook Trigger",
      "type": "n8n-nodes-base.webhook"
    },
    {
      "name": "LeafEngines Environmental",
      "type": "n8n-nodes-leafengines.environmentalIntelligence",
      "parameters": {"location": "{{ $json.location }}"}
    },
    {
      "name": "If Logic",
      "type": "n8n-nodes-base.if",
      "parameters": {"conditions": [{"leftValue": "{{ $json.riskScore }}", "rightValue": "70", "operation": "gt"}]}
    },
    {
      "name": "Slack Send",
      "type": "n8n-nodes-base.slack",
      "parameters": {"channel": "#alerts", "text": "High environmental risk detected"}
    }
  ]
}
```

## 📊 Use Cases

### Agricultural Management
- Soil health monitoring
- Irrigation scheduling
- Crop rotation planning

### Environmental Compliance
- Sustainability reporting
- Carbon credit calculation
- Regulatory compliance checks

### Land Evaluation
- Property due diligence
- Development suitability assessment
- Risk analysis

## 🔧 Contribution

This repository contains example workflows and documentation. The n8n node package is distributed via npm.

For issues, feature requests, or contributions to the node implementation, please use the appropriate channels.

## 📄 License

Examples and documentation are provided under MIT License.

## 📞 Support

- **Documentation:** [LeafEngines n8n Integration Guide](https://docs.leafengines.com/n8n)
- **Community:** [n8n Community Forum](https://community.n8n.io)
- **Issues:** Please report issues through proper support channels

## 🆓 Free Tier - Test Immediately

**Zero friction to try:** No email, no credit card, no commitment.

### **Two Ways to Test Free:**
1. **Test Key:** `leaf-test-370df0a2e62e` (works immediately)
2. **Free Tier Header:** `x-free-tier: true` (no API key needed)

### **What You Get:**
- Basic soil analysis with county FIPS codes
- USDA soil data access
- Limited requests for evaluation
- Perfect for prototyping and testing

**No risk, no commitment.** Test before buying.

## 💰 Pricing for n8n Automation Examples

These examples work with LeafEngines' agricultural intelligence API:

**Monthly Subscription Plans:**

| Region | Starter | Pro | Local Payment Methods |
|--------|---------|-----|----------------------|
| **United States** | $49 | $149 | Card, Apple Pay, Google Pay, Affirm |
| **European Union** | €45 (VAT incl.) | €135 (VAT incl.) | Klarna (DE), iDEAL (NL), EPS (AT), Apple/Google Pay |
| **United Kingdom** | £38 (VAT incl.) | £115 (VAT incl.) | Afterpay/Clearpay, Apple/Google Pay |
| **Australia** | AU$75 (GST incl.) | AU$225 (GST incl.) | Afterpay, Apple/Google Pay |

**Free Testing:** Use `leaf-test-370df0a2e62e` test key or `x-free-tier: true` header

**Test key gives you:**
- Full soil analysis capabilities
- Crop recommendations
- All free tier features

**Metered Pricing:** Pay-as-you-go credit packs + monthly subscriptions

Want higher limits or commercial use? Get instant API keys via Stripe checkout.
- [Starter – $149/mo →](https://buy.stripe.com/5kQ6oHcB88bR93s8MSaMU04)
- [Pro – $499/mo →](https://buy.stripe.com/14A6oH7gO3VBcfE1kqaMU05)
