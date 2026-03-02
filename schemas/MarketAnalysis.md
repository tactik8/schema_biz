# MarketAnalysis

## Properties
### **Market Analysis Schema: Dot Notation Mapping**

| Property Path | Expected Type | Description |
| :--- | :--- | :--- |
| `analysis.industryVertical` | `String` | The specific sector (e.g., **Renewable Energy**). |
| `analysis.marketMaturity` | `Enum` | Lifecycle stage: `Emerging`, `HighGrowth`, `Mature`, `Declining`. |
| `analysis.geographicFocus` | `Enum` | Spatial boundary: `Global`, `Regional`, `Local`. |
| `analysis.pestle.political` | `String` | Impact of government policy, trade, and stability. |
| `analysis.pestle.economic` | `String` | Macro factors: inflation, interest rates, and GDP. |
| `analysis.pestle.sociological` | `String` | Cultural trends, demographics, and lifestyle shifts. |
| `analysis.pestle.technological` | `String` | R&D, automation, and tech-driven disruption. |
| `analysis.pestle.legal` | `String` | Regulatory environment and compliance requirements. |
| `analysis.pestle.environmental` | `String` | Ecological factors and sustainability mandates. |
| `analysis.marketSize.value` | `Number` | Numerical value of the total market (TAM). |
| `analysis.marketSize.currency` | `String` | ISO currency code (e.g., `USD`). |
| `analysis.compIntel.competitorCount` | `Integer` | Total number of active players in the segment. |
| `analysis.compIntel.concentrationRatio` | `String` | Market structure (e.g., `Monopoly`, `Fragmented`). |
| `analysis.compIntel.benchmarkCriteria[]` | `Array` | Factors used to compare players (e.g., `Pricing`). |
| `analysis.compIntel.topTier[].brand` | `String` | Legal or trade name of the competitor. |
| `analysis.compIntel.topTier[].marketShare` | `String` | Percentage of market controlled by the brand. |
| `analysis.compIntel.topTier[].differentiation`| `String` | **BAV:** The brand's unique perceived value. |
| `analysis.compIntel.topTier[].relevance` | `String` | **BAV:** Alignment with consumer needs. |
| `analysis.compIntel.topTier[].esteem` | `String` | **BAV:** Reputation and quality perception. |
| `analysis.compIntel.topTier[].knowledge` | `String` | **BAV:** Depth of consumer awareness. |
| `analysis.customers[].segmentName` | `String` | Name of target group (e.g., `Early Adopters`). |
| `analysis.customers[].acquisitionCost` | `Enum` | CAC Level: `Low`, `Medium`, `High`. |
| `analysis.customers[].lifetimeValue` | `Enum` | LTV Level: `Low`, `Medium`, `High`, `VeryHigh`. |
| `analysis.customers[].primaryMotivator` | `String` | The core "Why" behind the purchase. |
| `analysis.swot.strengths[]` | `Array` | Internal strategic advantages. |
| `analysis.swot.weaknesses[]` | `Array` | Internal operational vulnerabilities. |
| `analysis.swot.opportunities[]` | `Array` | External growth vectors. |
| `analysis.swot.threats[]` | `Array` | External risks and market pressures. |


## Example

  ```
  {
  "@context": {
    "biz": "https://schema.org/custom/business-intel#",
    "market": "https://schema.org/custom/market-dynamics#",
    "strategy": "https://schema.org/custom/competitive-strategy#",
    "brand": "https://schema.org/custom/brand-equity#"
  },
  "@type": "biz:MarketAnalysisReport",
  "industryVertical": "Renewable Energy",
  "marketMaturity": "HighGrowth",
  "geographicFocus": "Global",
  "environmentalAnalysis": {
    "@type": "strategy:PESTLEFramework",
    "political": "Subsidies and trade tariffs impacting cross-border solar trade.",
    "economic": "Rising interest rates affecting capital-intensive project financing.",
    "sociological": "Increased consumer demand for carbon-neutral household solutions.",
    "technological": "Breakthroughs in solid-state battery storage efficiency.",
    "legal": "New ESG reporting requirements and grid-access regulations.",
    "environmental": "Climate-driven shift in resource availability (wind/solar patterns)."
  },
  "marketSize": {
    "@type": "market:SizingData",
    "totalAddressableMarket": { "value": 850.5, "unit": "Billion", "currency": "USD" },
    "serviceableAddressableMarket": { "value": 120.0, "unit": "Billion", "currency": "USD" }
  },
  "competitiveIntelligence": {
    "@type": "strategy:MarketStructure",
    "competitorCount": 45,
    "concentrationRatio": "Fragmented",
    "benchmarkCriteria": ["Pricing", "Innovation", "MarketShare"],
    "topTierCompetitors": [
      {
        "@type": "brand:CompetitorProfile",
        "brand": "EcoVolt Dynamics",
        "marketShare": "8.5%",
        "brandEquityMetrics": {
          "differentiation": "Patented hyper-efficient PV coating.",
          "relevance": "High alignment with residential grid-tie needs.",
          "esteem": "Premium quality perception with 25-year warranty.",
          "knowledge": "Moderate; expanding into emerging markets."
        }
      }
    ]
  },
  "customerProfiles": [
    {
      "@type": "biz:TargetSegment",
      "segmentName": "Early Adopters",
      "acquisitionCost": "High",
      "lifetimeValue": "VeryHigh",
      "primaryMotivator": "Innovation"
    }
  ],
  "strategicMatrix": {
    "@type": "strategy:SWOTAnalysis",
    "strengths": ["Proprietary AI grid management", "Agile R&D team"],
    "weaknesses": ["Limited manufacturing scale", "High initial product cost"],
    "opportunities": ["Green hydrogen integration", "Public-private partnerships"],
    "threats": ["Supply chain volatility for rare earth metals", "Incumbent lobby groups"]
  }
}

```

## JSON Schema

```

{
  "$schema": "https://json-schema.org/draft/2020-12/schema",
  "title": "Market Analysis Report Schema",
  "description": "A structured schema for industry analysis, competitive intelligence, and brand equity.",
  "type": "object",
  "properties": {
    "industryVertical": { "type": "string" },
    "marketMaturity": { 
      "type": "string", 
      "enum": ["Emerging", "HighGrowth", "Mature", "Declining"] 
    },
    "geographicFocus": { 
      "type": "string", 
      "enum": ["Global", "Regional", "Local"] 
    },
    "pestle": {
      "type": "object",
      "properties": {
        "political": { "type": "string" },
        "economic": { "type": "string" },
        "sociological": { "type": "string" },
        "technological": { "type": "string" },
        "legal": { "type": "string" },
        "environmental": { "type": "string" }
      },
      "required": ["political", "economic", "sociological", "technological", "legal", "environmental"]
    },
    "marketSize": {
      "type": "object",
      "properties": {
        "value": { "type": "number" },
        "currency": { "type": "string", "default": "USD" },
        "unit": { "type": "string", "description": "e.g., Millions, Billions" }
      }
    },
    "competitiveIntelligence": {
      "type": "object",
      "properties": {
        "competitorCount": { "type": "integer" },
        "concentrationRatio": { "type": "string" },
        "benchmarkCriteria": {
          "type": "array",
          "items": { "type": "string" }
        },
        "topTierCompetitors": {
          "type": "array",
          "items": {
            "type": "object",
            "properties": {
              "brand": { "type": "string" },
              "marketShare": { "type": "string" },
              "differentiation": { "type": "string" },
              "relevance": { "type": "string" },
              "esteem": { "type": "string" },
              "knowledge": { "type": "string" }
            },
            "required": ["brand", "differentiation", "relevance", "esteem", "knowledge"]
          }
        }
      }
    },
    "customerProfiles": {
      "type": "array",
      "items": {
        "type": "object",
        "properties": {
          "segmentName": { "type": "string" },
          "acquisitionCost": { "type": "string", "enum": ["Low", "Medium", "High"] },
          "lifetimeValue": { "type": "string", "enum": ["Low", "Medium", "High", "VeryHigh"] },
          "primaryMotivator": { "type": "string" }
        }
      }
    },
    "swot": {
      "type": "object",
      "properties": {
        "strengths": { "type": "array", "items": { "type": "string" } },
        "weaknesses": { "type": "array", "items": { "type": "string" } },
        "opportunities": { "type": "array", "items": { "type": "string" } },
        "threats": { "type": "array", "items": { "type": "string" } }
      }
    }
  },
  "required": ["industryVertical", "marketMaturity", "geographicFocus", "pestle", "swot"]
}

```

