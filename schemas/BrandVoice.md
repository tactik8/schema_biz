# BrandVoice


## Properties
|Property | Expected Type | Description |
|--- |---|---|
| brandVision | Text | Story | 
| brandMission |  Text | Personality | 
| brandCoreValues | Text | Core values | 
| brandStory | Text | Story | 
| brandPersonality |  Text | Personality | 
| primaryArchetype | BrandArchetypeType | xxx | 
| secondaryeArchetype | BrandArchetypeType | xxx | 
| toneHumor | QuantitativeValue | 1. Serious, 3. Neutral 5. Humoristic |
| toneEnthusiasm | QuantitativeValue |1. Matter-of-fact, 3.Neutral, 5. Enthusiastic  |
| toneFormality | QuantitativeValue | 1. Casual, 3.Neutral, 5. Formal |
| toneRespectfulness | QuantitativeValue | 1. Irreverent, 3. Neutral, 5. Respectful |
| brandVoiceCharacteristics | Text | xxx | 
| brandToneVariations | Text | Vision Statement |



## Example
```
  {
   "@type": "BrandVoice",
   "brandVision":"xx",
   "brandMission": "xxx",
   "brandCoreValues": "xxx",
   "brandStory": "xxx",
   "brandPersonality": "xxx",
   "primaryArchetype": "CaregiverBrandArchetype",
   "secondaryeArchetype": "JesterBrandArchetype",
   "toneHumor": 4,
   "toneEnthusiasm": 3,
   "toneFormality": 2,
   "toneRespectfulness": 4
  }




```


## JSON Schema

```
{
  "$schema": "http://json-schema.org/draft-04/schema#",
  "type": "object",
  "properties": {
    "@type": {
      "type": "string"
    },
    "brandVision": {
      "type": "string",
       "title": "xxx",
      "description": "ccc",
    },
    "brandMission": {
      "type": "string",
      "title": "xxx",
      "description": "ccc",
    },
    "brandCoreValues": {
      "type": "string",
       "title": "xxx",
      "description": "ccc",
    },
    "brandStory": {
      "type": "string",
       "title": "xxx",
      "description": "ccc",
    },
    "brandPersonality": {
      "type": "string",
       "title": "xxx",
      "description": "ccc",
    },
    "primaryArchetype": {
      "type": "string"
    },
    "secondaryeArchetype": {
      "type": "string",
 "title": "xxx",
      "description": "ccc",
    },
    "toneHumor": {
      "type": "integer",
      "title": "xxx",
      "description": "ccc",
      "minimum": "1",
      "maximum": 5
    },
    "toneEnthusiasm": {
     "type": "integer",
 "title": "xxx",
      "description": "ccc",
      "minimum": "1",
      "maximum": 5
    },
    "toneFormality": {
     "type": "integer",
 "title": "xxx",
      "description": "ccc",
      "minimum": "1",
      "maximum": 5
    },
    "toneRespectfulness": {
      "type": "integer",
 "title": "xxx",
      "description": "ccc",
      "minimum": "1",
      "maximum": 5
    }
  },
  "required": [
    "@type",
    "brandVision",
    "brandMission",
    "brandCoreValues",
    "brandStory",
    "brandPersonality",
    "primaryArchetype",
    "secondaryeArchetype",
    "toneHumor",
    "toneEnthusiasm",
    "toneFormality",
    "toneRespectfulness"
  ]
}


```



output properties: 
- toneHumor: 1 to 5, 1. Serious, 3. Neutral 5. Humoristic
- toneEnthusiasm: 1 to 5, 1. Matter-of-fact, 3.Neutral, 5. Enthusiastic
- toneFormality: 1 to 5, 1. Casual, 3.Neutral, 5. Formal
- tonetechnical: 1 to 5, 1. easy to understand, 5. very technical
- toneAssertiveness: 1 to 5, 1. humble, 5. very assertive
