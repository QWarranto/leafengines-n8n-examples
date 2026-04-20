
## 🎯 QGIS Plugin Officially Approved!

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
**Founder Pricing:** First 100 customers get lifetime pricing lock
