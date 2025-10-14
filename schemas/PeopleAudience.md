# PeopleAudience

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

  {
    "@type": "PeopleAudience",
    "name": "Bob the builder",
    "description": "",
    "requiredGender": "male",
    "requiredMinAge": 30,
    "requiredMaxAge": 40,
    "suggestedGender": "male",
    "suggestedAge": 40,
    "suggestedMinAge": 40,
    "suggestedMaxAge": 40,
    "geographicArea": {},
    "psyQuote": "",
    "psyRepresentation": "",
    "psyPersonalityTraits": "",
    "psyValuesBeliefs": "",
    "psyInterests": "",
    "psyPreferredBrands": "",
    "psyOnlineBehaviour": "",
    "psyShoppingHabits": "",
    "psyProductNeeds": "",
    "psyBrandEngagement": "",
    "psyKeyMessages": "",
    "psyMessagingTone": "",
    "psyCallToAction": ""

}
```

```
{
  "title": "BrandAudiencePersona",
  "type": "object",
  "properties": {
    "identification": {
      "type": "object",
      "description": "I. Overview & Identification",
      "properties": {
        "persona_name": {
          "type": "string",
          "description": "Fictional but descriptive name (e.g., 'Tech-Savvy Tina')."
        },
        "photo_url": {
          "type": "string",
          "format": "uri",
          "description": "URL to a visual representation of the persona."
        },
        "job_title_role": {
          "type": "string",
          "description": "Professional position (B2B) or key life role (B2C)."
        },
        "summary_quote": {
          "type": "string",
          "description": "A short sentence or quote capturing their core attitude."
        }
      },
      "required": ["persona_name", "job_title_role"]
    },
    "demographics": {
      "type": "object",
      "description": "II. Demographics",
      "properties": {
        "age": {
          "type": ["string", "integer"],
          "description": "Specific age or age range."
        },
        "gender": {
          "type": "string",
          "description": "Gender identity."
        },
        "location": {
          "type": "string",
          "description": "Geographic location or type (e.g., 'Urban West Coast')."
        },
        "income_education": {
          "type": "string",
          "description": "Relevant financial status and educational background."
        },
        "family_status": {
          "type": "string",
          "description": "Marital status, number of children, etc."
        }
      }
    },
    "psychographics_lifestyle": {
      "type": "object",
      "description": "III. Psychographics & Lifestyle",
      "properties": {
        "personality_traits": {
          "type": "array",
          "items": {
            "type": "string"
          },
          "description": "Key adjectives describing their general disposition (e.g., 'Ambitious', 'Cautious')."
        },
        "values_beliefs": {
          "type": "array",
          "items": {
            "type": "string"
          },
          "description": "What matters most to them (e.g., 'Sustainability', 'Innovation')."
        },
        "interests_hobbies": {
          "type": "array",
          "items": {
            "type": "string"
          },
          "description": "How they spend their free time."
        },
        "motivations": {
          "type": "string",
          "description": "What drives their decisions related to your industry."
        }
      }
    },
    "goals_pain_points": {
      "type": "object",
      "description": "IV. Goals & Pain Points",
      "properties": {
        "primary_goal": {
          "type": "string",
          "description": "The main objective they are trying to achieve."
        },
        "primary_pain_point": {
          "type": "string",
          "description": "The biggest problem or frustration your brand can solve."
        },
        "objections_to_purchase": {
          "type": "array",
          "items": {
            "type": "string"
          },
          "description": "Common hesitations or barriers to buying your product/service."
        }
      },
      "required": ["primary_goal", "primary_pain_point"]
    },
    "brand_interaction_behavior": {
      "type": "object",
      "description": "V. Brand Interaction & Behavior",
      "properties": {
        "tech_proficiency": {
          "type": "string",
          "enum": ["High", "Medium", "Low"],
          "description": "Their comfort level and expertise with technology."
        },
        "information_sources": {
          "type": "array",
          "items": {
            "type": "string"
          },
          "description": "Where they go for advice and research (e.g., 'Industry Leaders', 'Reddit')."
        },
        "preferred_channels": {
          "type": "array",
          "items": {
            "type": "string"
          },
          "description": "Best platforms for your brand to reach them (e.g., 'Email', 'LinkedIn')."
        },
        "relationship_expectation": {
          "type": "string",
          "description": "What kind of connection they want with your brand (e.g., 'Expert', 'Transactional')."
        }
      }
    },
    "messaging_strategy": {
      "type": "object",
      "description": "VI. Messaging Strategy",
      "properties": {
        "keywords_language": {
          "type": "array",
          "items": {
            "type": "string"
          },
          "description": "Specific words they use to describe their needs."
        },
        "brand_voice_adaptation": {
          "type": "string",
          "description": "How your voice should be toned for this persona (e.g., 'more empathetic', 'highly technical')."
        },
        "core_message_value_prop": {
          "type": "string",
          "description": "The one sentence that will resonate most with them."
        },
        "cta_focus": {
          "type": "string",
          "description": "What action is most appealing (e.g., 'Request a Demo', 'Read the Case Study')."
        }
      }
    }
  },
  "required": [
    "identification",
    "demographics",
    "psychographics_lifestyle",
    "goals_pain_points",
    "brand_interaction_behavior",
    "messaging_strategy"
  ]
}

```
