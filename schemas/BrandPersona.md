
# BrandPersona

## Properties
|Property | Expected Type | Description |
|--- |---|---|
| suggestedGender | Test | The typical gender for this audience. |
| suggestedMinAge | Number | The typical minimum age for this audience. |
| suggestedMaxAge | Number | The typical maximum age for this audience. |
| geographicArea | Test | The typical geographic area for this audience (city vs suburbs vs campaign) |
| psyQuote | Text | A quote the person could have said to represent themselves | 
| psyRepresentation | Text | A short image of the audience. ("David, a caring dog parent in his 30s-40s."). |
| psyPersonalityTraits | Text | ("Responsible, loving, proactive, attentive to their dog's needs.") | 
| psyValuesBeliefs | Text | The typical value sor beliefs of this audience. | 
| psyInterests |  Text | The typical interests or hobbies of this audience.  | 
| psyPreferredBrands | Text | Text |
| psyOnlineBehaviour  | Text | The online behaviour typical of this audience. |
| psyShoppingHabits  | Text | The shopping habits of this audience regarding this product or service. |
| psyProductNeeds  | Text | The typical needs for this audience from this type of product or service. |
| psyBrandEngagement  | Text | Text |
| psyKeyMessages | Text | The key messages likely to resonate with the audience. |
| psyMessagingTone  | Text | The tone to be used to communicate with the audience.  |
| psyCallToAction  | Text | The call to actions susceptible to resonate with the audience. |



## Example
```

```



```

{
  "$schema": "https://json-schema.org/draft/2020-12/schema",
  "title": "BrandPersona",
  "description": "A detailed representation of a target audience segment used for marketing and product alignment.",
  "type": "object",
  "required": [
    "name",
    "jobTitle",
    "quotation",
    "age"
  ],
  "properties": {
    "name": {
      "type": "string",
      "description": "A fictional but descriptive moniker that humanizes the persona (e.g., 'Eco-Conscious Ethan')."
    },
    "jobTitle": {
      "type": "string",
      "description": "The persona's professional title for B2B contexts or primary life role/stage for B2C contexts."
    },
    "quotation": {
      "type": "string",
      "description": "A first-person mantra or quote that encapsulates the persona's core motivation or pain point."
    },
    "age": {
      "oneOf": [
        {
          "type": "integer",
          "minimum": 0,
          "description": "The exact age of the persona."
        },
        {
          "type": "string",
          "description": "A descriptive age range (e.g., '25-34' or 'Mid-40s')."
        }
      ],
      "description": "The chronological age or life stage range of the target segment."
    },
    "gender": {
      "type": "string",
      "description": "The gender identity or demographic lean of the persona."
    },
    "location": {
      "type": "string",
      "description": "The geographic region, climate, or urbanization level (e.g., 'Metropolitan Europe' or 'Rural Midwest')."
    },
    "income_education": {
      "type": "string",
      "description": "A summary of the persona's socioeconomic status, including annual earnings and highest level of schooling."
    },
    "family_status": {
      "type": "string",
      "description": "Household composition, marital status, and presence of dependents."
    }
  }
}

```
