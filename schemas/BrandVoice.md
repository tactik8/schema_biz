# BrandVoice


## Properties
|Property | Expected Type | Description |
|--- |---|---|
| brandVision | Text | The Aspiration. A clear, inspiring statement describing the future you are working to create; it defines the long-term impact and ultimate success of the brand. (e.g., "A world where every person has access to clean energy.") |
| brandMission |  Text | The Business. A concise statement explaining what the brand does, who it does it for, and why it does it. It is an action-oriented explanation of the current business goals. | 
| brandCoreValues | Text | The Principles. The fundamental beliefs and guiding principles that dictate the brand's behavior, decision-making, and culture. They are non-negotiable standards. (e.g., Integrity, Innovation, Customer Focus). | 
| brandStory | Text | The Narrative. The overarching, compelling narrative that connects the brand's history, purpose, values, and vision into a cohesive, emotional journey for the audience. | 
| brandPersonality |  Text | The Character. A set of human characteristics and traits that the brand consistently expresses through its voice and visual identity. It dictates how the brand speaks and acts. (e.g., trustworthy, witty, rebellious, sincere). | 
| primaryArchetype | BrandArchetypeType | The Main Identity. The dominant, universally recognizable symbolic pattern (e.g., The Hero, The Creator, The Innocent) that shapes the brand's deepest meaning and serves as the core of its personality. | 
| secondaryeArchetype | BrandArchetypeType | The Supporting Role. A second, less dominant archetype that adds complexity and nuance to the brand's personality, helping it to be more distinctive and avoid being a cliché.  | 
| toneHumor | QuantitativeValue | The use of lightheartedness, jokes, or playfulness (humorous) versus a direct, earnest, or sober manner (serious). 1. Serious, 3. Neutral 5. Humoristic |
| toneEnthusiasm | QuantitativeValue |The level of emotion or excitement conveyed. Does the brand use exclamation points and hype (enthusiastic), or does it stick to plain, objective statements (matter-of-fact)? 1. Matter-of-fact, 3.Neutral, 5. Enthusiastic  |
| toneFormality | QuantitativeValue | The level of professionalism in language. Does the brand use contractions, slang, and an approachable style (casual), or proper grammar and a more distant approach (formal)? 1. Casual, 3.Neutral, 5. Formal  |
| toneRespectfulness | QuantitativeValue | The deference shown to conventions, authority, or subjects. Is the brand polite and mindful of tradition (respectful), or does it challenge norms and use bold, unexpected language (irreverent)? 1. Irreverent, 3. Neutral, 5. Respectful |
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
       "title": "The Aspiration",
      "description": "A clear, inspiring statement describing the future you are working to create; it defines the long-term impact and ultimate success of the brand. (e.g., \"A world where every person has access to clean energy.\")"
    },
    "brandMission": {
      "type": "string",
      "title": "The Business",
      "description": "A concise statement explaining what the brand does, who it does it for, and why it does it. It is an action-oriented explanation of the current business goals."
    },
    "brandCoreValues": {
      "type": "string",
       "title": "The Principles",
      "description": "The fundamental beliefs and guiding principles that dictate the brand's behavior, decision-making, and culture. They are non-negotiable standards. (e.g., Integrity, Innovation, Customer Focus)."
    },
    "brandStory": {
      "type": "string",
       "title": "The Narrative",
      "description": "The overarching, compelling narrative that connects the brand's history, purpose, values, and vision into a cohesive, emotional journey for the audience."
    },
    "brandPersonality": {
      "type": "string",
       "title": "The Character",
      "description": "A set of human characteristics and traits that the brand consistently expresses through its voice and visual identity. It dictates how the brand speaks and acts. (e.g., trustworthy, witty, rebellious, sincere)."
    },
    "primaryArchetype": {
      "type": "string",
"title": "The Main Identity",
 "description": "The dominant, universally recognizable symbolic pattern (e.g., The Hero, The Creator, The Innocent) that shapes the brand's deepest meaning and serves as the core of its personality.Archetypes: Innocent, Orphan/Regular Guy/Gal, Hero, Caregiver, Explorer, Rebel/Outlaw, Lover, Creator, Jester, Sage, Magician, Ruler."
    },
    "secondaryeArchetype": {
      "type": "string",
"title": "The Supporting Role",
 "description": "A second, less dominant archetype that adds complexity and nuance to the brand's personality, helping it to be more distinctive and avoid being a cliché. Archetypes: Innocent, Orphan/Regular Guy/Gal, Hero, Caregiver, Explorer, Rebel/Outlaw, Lover, Creator, Jester, Sage, Magician, Ruler."
    },
    "toneHumor": {
      "type": "integer",
      "title": "Humorous vs. Serious",
      "description": "The use of lightheartedness, jokes, or playfulness (humorous) versus a direct, earnest, or sober manner (serious). 1. Serious, 3. Neutral 5. Humoristic",
      "minimum": "1",
      "maximum": 5
    },
    "toneEnthusiasm": {
     "type": "integer",
     "title": "Enthusiastic vs. Matter-of-fact",
      "description": "The level of emotion or excitement conveyed. Does the brand use exclamation points and hype (enthusiastic), or does it stick to plain, objective statements (matter-of-fact)? 1. Matter-of-fact, 3.Neutral, 5. Enthusiastic",
      "minimum": "1",
      "maximum": 5
    },
    "toneFormality": {
     "type": "integer",
     "title": "Formal vs. Casual",
      "description": "The level of professionalism in language. Does the brand use contractions, slang, and an approachable style (casual), or proper grammar and a more distant approach (formal)? 1. Casual, 3.Neutral, 5. Formal ",
      "minimum": "1",
      "maximum": 5
    },
    "toneRespectfulness": {
      "type": "integer",
       "title": "Respectful vs. Irreverent",
      "description": "The deference shown to conventions, authority, or subjects. Is the brand polite and mindful of tradition (respectful), or does it challenge norms and use bold, unexpected language (irreverent)? 1. Irreverent, 3. Neutral, 5. Respectful",
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
