# AdGroup

## Properties
| Field Name | JSON Type | Description |
| :--- | :--- | :--- |
| **adGroupId** | string | The unique numerical identifier assigned to the Ad Group by Google Ads. |
| **campaignId** | string | The numerical identifier of the parent campaign to which this Ad Group belongs. |
| **adGroupName** | string | The descriptive name of the Ad Group. |
| **campaignStatus** | string (enum) | The operational status of the Ad Group (`ENABLED`, `PAUSED`, `REMOVED`). |
| **inLanguage** | string | The language of the ad group |
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
  "adGroupId": "205478119234",
  "campaignId": "199456700012",
  "adGroupName": "Performance Runners - Exact Match",
  "status": "ENABLED",
  "defaultBid": 1.25,
  "inLanguage": "fr",
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
      "type": "RSA",
      "finalUrl": "https://www.example.com/shoes/glidemax-5",
      "headlines": [
        {
          "text": "The GlideMax 5",
          "maxCharacters": 30,
          "pinPosition": 1
        },
        {
          "text": "Race Day Ready!",
          "maxCharacters": 30,
          "pinPosition": null
        },
        {
          "text": "Free Shipping Over $50",
          "maxCharacters": 30,
          "pinPosition": 3
        }
      ],
      "descriptions": [
        {
          "text": "Lightweight, Responsive Foam Technology for Peak Performance.",
          "maxCharacters": 90
        },
        {
          "text": "Shop our full collection of marathon and distance running shoes today.",
          "maxCharacters": 90
        }
      ]
    },
    {
      "adId": "310945780002",
      "type": "ETA",
      "finalUrl": "https://www.example.com/deals",
      "headlines": [
        {
          "text": "Daily Deals on Runners",
          "maxCharacters": 30,
          "pinPosition": null
        },
        {
          "text": "Free Returns on All Shoes",
          "maxCharacters": 30,
          "pinPosition": null
        }
      ],
      "descriptions": [
        {
          "text": "Find Your Perfect Fit. Limited time offers and promotions available now.",
          "maxCharacters": 90
        }
      ]
    }
  ]
}
```
