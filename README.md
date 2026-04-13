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
3. Enter your API key (request from [SoilSidekick Pro](https://app.soilsidekickpro.com))

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