
# BrandPersona

## Properties
| Property | Expected Type | Description |
| :--- | :--- | :--- |
| **name** | `string` | A fictional but descriptive moniker that humanizes the persona (e.g., 'Eco-Conscious Ethan'). |
| **jobTitle** | `string` | The persona's professional title for B2B contexts or primary life role/stage for B2C contexts. |
| **quotation** | `string` | A first-person mantra or quote that encapsulates the persona's core motivation or pain point. |
| **age** | `integer` OR `string` | The chronological age or a descriptive life stage range (e.g., '25-34' or 'Mid-40s'). |
| **gender** | `string` | The gender identity or demographic lean of the persona. |
| **location** | `string` | The geographic region, climate, or urbanization level (e.g., 'Metropolitan Europe' or 'Rural Midwest'). |
| **income_education** | `string` | A summary of the persona's socioeconomic status, including annual earnings and highest level of schooling. |
| **family_status** | `string` | Household composition, marital status, and presence of dependents. |


## Example
```
{
  "name": "Modern Minimalist Maya",
  "jobTitle": "Senior UX Designer & Freelance Consultant",
  "quotation": "I value experiences over ownership; if a product doesn't simplify my life, it's just clutter.",
  "age": "28-35",
  "gender": "Female / Non-binary leaning",
  "location": "Urban Pacific Northwest (Seattle/Portland/Vancouver)",
  "income_education": "$95k+ annual income; Bachelor of Fine Arts in Digital Media.",
  "family_status": "Single; living with a partner in a rented high-rise apartment; no children; pet owner (Greyhound)."
}
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
