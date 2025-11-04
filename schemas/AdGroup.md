# AdGroup

## Properties
| Field Name | JSON Type | Description |
| :--- | :--- | :--- |
| **adGroupId** | string | The unique numerical identifier assigned to the Ad Group by Google Ads. |
| **campaignId** | string | The numerical identifier of the parent campaign to which this Ad Group belongs. |
| **adGroupName** | string | The descriptive name of the Ad Group. |
| **status** | string (enum) | The operational status of the Ad Group (`ENABLED`, `PAUSED`, `REMOVED`). |
| **defaultBid** | number | The default Cost-Per-Click (CPC) bid set for this Ad Group, represented as a monetary value. |
| **keywords** | array (of Keyword) | A list of search terms and their match types targeted by this Ad Group. |
| *keywords\[\].text* | string | The keyword text itself (e.g., 'buy running shoes'). |
| *keywords\[\].matchType* | string (enum) | The keyword match type (`EXACT`, `PHRASE`, `BROAD`). |
| *keywords\[\].id* | string | The unique ID for the keyword asset. |
| **ads** | array (of AdCreative) | A list of all ad creatives contained within this Ad Group. |
| *ads\[\].adId* | string | The unique ID for the ad creative. |
| *ads\[\].adTitle* | string | The main headline for the ad. |
| *ads\[\].descriptionLine1* | string | The first line of the ad description. |
| *ads\[\].finalUrl* | string (url) | The landing page URL. |
| *ads\[\].type* | string (enum) | The type of ad creative (`RSA`, `ETA`, `DSA`, `CallAd`). |



## Example

```
{
  "adGroupId": "205478119234",
  "campaignId": "199456700012",
  "adGroupName": "Performance Runners - Exact Match",
  "status": "ENABLED",
  "defaultBid": 1.25,
  "keywords": [
    {
      "text": "[men's marathon shoe]",
      "matchType": "EXACT",
      "id": "5001"
    },
    {
      "text": "\"buy performance runners\"",
      "matchType": "PHRASE",
      "id": "5002"
    },
    {
      "text": "best race day shoes",
      "matchType": "BROAD",
      "id": "5003"
    }
  ],
  "ads": [
    {
      "adId": "310945780001",
      "adTitle": "The GlideMax 5 | Race Day Ready!",
      "descriptionLine1": "Lightweight, Responsive Foam. Free Shipping Over $50.",
      "finalUrl": "https://www.example.com/shoes/glidemax-5",
      "type": "RSA"
    },
    {
      "adId": "310945780002",
      "adTitle": "Free Returns on All Running Shoes",
      "descriptionLine1": "Find Your Perfect Fit. Shop Today's Deals.",
      "finalUrl": "https://www.example.com/deals",
      "type": "ETA"
    }
  ]
}

```

## JSON Schema
```
{
  "$schema": "http://json-schema.org/draft-07/schema#",
  "title": "Google Ads Ad Group Schema",
  "type": "object",
  "description": "A JSON Schema definition for a single Google Ads Ad Group, including its association with a Campaign, keywords, and creative assets.",

  "properties": {
    "adGroupId": {
      "type": "string",
      "description": "The unique numerical identifier assigned to the Ad Group by Google Ads."
    },
    "campaignId": {
      "type": "string",
      "description": "The numerical identifier of the parent campaign to which this Ad Group belongs."
    },
    "adGroupName": {
      "type": "string",
      "description": "The descriptive name of the Ad Group."
    },
    "status": {
      "type": "string",
      "description": "The operational status of the Ad Group.",
      "enum": ["ENABLED", "PAUSED", "REMOVED"]
    },
    "defaultBid": {
      "type": "number",
      "description": "The default Cost-Per-Click (CPC) bid set for this Ad Group, represented as a monetary value."
    },
    "keywords": {
      "type": "array",
      "description": "A list of search terms and their match types targeted by this Ad Group.",
      "items": { "$ref": "#/definitions/Keyword" }
    },
    "ads": {
      "type": "array",
      "description": "A list of all ad creatives (e.g., Expanded Text Ads, Responsive Search Ads) contained within this Ad Group.",
      "items": { "$ref": "#/definitions/AdCreative" }
    }
  },

  "required": ["adGroupId", "campaignId", "adGroupName", "status", "keywords", "ads"],

  "definitions": {
    "Keyword": {
      "type": "object",
      "description": "Schema for a targeted Keyword.",
      "properties": {
        "text": { "type": "string", "description": "The keyword text itself (e.g., 'buy running shoes')." },
        "matchType": {
          "type": "string",
          "description": "The keyword match type (e.g., 'EXACT', 'PHRASE', 'BROAD').",
          "enum": ["EXACT", "PHRASE", "BROAD"]
        },
        "id": { "type": "string", "description": "The unique ID for the keyword asset." }
      },
      "required": ["text", "matchType"]
    },
    "AdCreative": {
      "type": "object",
      "description": "Schema for a single Ad Creative asset (e.g., an RSA).",
      "properties": {
        "adId": { "type": "string", "description": "The unique ID for the ad creative." },
        "adTitle": { "type": "string", "description": "The main headline for the ad." },
        "descriptionLine1": { "type": "string", "description": "The first line of the ad description." },
        "finalUrl": { "type": "string", "format": "url", "description": "The landing page URL." },
        "type": {
          "type": "string",
          "description": "The type of ad creative (e.g., 'RSA', 'ETA', 'DSA').",
          "enum": ["RSA", "ETA", "DSA", "CallAd"]
        }
      },
      "required": ["adId", "adTitle", "descriptionLine1", "finalUrl"]
    }
  }
}
```
```
