# BrandVoice


## Properties
|Property | Expected Type | Description |
|--- |---|---|
| primaryArchetype | BrandArchetypeType | xxx | 
| secondaryeArchetype | BrandArchetypeType | xxx | 
| toneHumor | QuantitativeValue | 1. Serious, 3. Neutral 5. Humoristic |
| toneEnthusiasm | QuantitativeValue |1. Matter-of-fact, 3.Neutral, 5. Enthusiastic  |
| toneFormality | QuantitativeValue | 1. Casual, 3.Neutral, 5. Formal |
| toneRespectfulness | QuantitativeValue | 1. Irreverent, 3. Neutral, 5. Respectful |
| brandVoiceCharacteristics | Text | xxx | 
| brandToneVariations | Text | Vision Statement |
| brandCoreValues | Text | Core values | 
| brandStory | Text | Story | 
| brandPersonality |  Text | Personality | 



## Example
```
 "toneHumor": {
        "@type": "Rating",
        "name": "tone dimension - humor",
        "description": "1=Very Serious, 3=Neutral/Witty, 5=Very Humorous",
        "ratingValue": 5,
        "bestRating": 5
      },
      "toneEnthusiasm": {
        "@type": "Rating",
        "name": "tone dimension - enthusiasm",
        "description": "1=Very Neutral/Objective, 3=Balanced/Calm, 5=Very Passionate/Excited",
        "ratingValue": 2,
        "bestRating": 5
      },
      "toneFormality": {
        "@type": "Rating",
        "name": "tone dimension - formality",
        "description": "1=Very Casual, 3=Neutral/Conversational, 5=Very Formal",
        "ratingValue": 4,
        "bestRating": 5
      },
      "toneRespectfulness": {
        "@type": "Rating",
        "name": "tone dimension - respsectfulness",
        "description": "1=Very Irreverent/Edgy, 3=Appropriately Direct, 5=Highly Respectful/Deferential",
        "ratingValue": 5,
        "bestRating": 5
      }


{
  "@type": "BrandVoice",
  "primaryArchetype": "CaregiverBrandArchetype",
  "secondaryeArchetype": "JesterBrandArchetype",
  "toneHumor": 4,
  "toneEnthusiasm": 3,
  "toneFormality": 2,
  "toneRespectfulness": 4,
  "xxx": "xxx",
  "xxx": "xxx",
  "xxx": "xxx",
  "xxx": "xxx",
  "xxx": "xxx",
  "xxx": "xxx",
  "xxx": "xxx",
  "xxx": "xxx",
  "xxx": "xxx",

}


```
output properties: 
- toneHumor: 1 to 5, 1. Serious, 3. Neutral 5. Humoristic
- toneEnthusiasm: 1 to 5, 1. Matter-of-fact, 3.Neutral, 5. Enthusiastic
- toneFormality: 1 to 5, 1. Casual, 3.Neutral, 5. Formal
- tonetechnical: 1 to 5, 1. easy to understand, 5. very technical
- toneAssertiveness: 1 to 5, 1. humble, 5. very assertive
