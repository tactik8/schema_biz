# ContentPillar 

## Properties 

|Property | Expected Type | Description |
|--- |---|---|
| name | text | A short, clear, and catchy title for the core topic.	 | 
| pillarFamily | text | Why does this pillar exist? Education, Entertainment, Insprational, Promotional, Engagement, Timely |
| TargetAudience | PersonAudience | Which specific part of your audience persona is this pillar primarily aimed at?	 | 
| Stage of Buyer's Journey | text | Which stage of the journey does this content address? (e.g., Awareness, Consideration, Decision).	|
| Keyword | text | The primary, high-level keyword or topic you want to rank for (for SEO-focused pillars).	 | 
| Definition | text | A 1-2 sentence description of what this pillar covers and, just as importantly, what it does not cover.	 | 
| subPillars | ContentPillar | Sub topics |
| Primary Format | text | The best content type for this pillar/sub-pillar.	 |
| Distribution Channel(s)	 | text | Where will this content primarily be shared?	.	 |
| Repurposing Opportunities	 | text | How can the primary content be broken down and reused?	 |
| Call-to-Action (CTA)		 | text | The desired action after consuming the content	 |

  
  
  ## Example


## JSON Schema

```
{
  "$schema": "http://json-schema.org/draft-07/schema#",
  "$id": "http://example.com/contentPillarSchema.json",
  "title": "Content Pillar Documentation Format",
  "description": "A systematic format for documenting all aspects of content pillars and their associated content clusters.",
  "type": "object",
  "properties": {
    "pillars": {
      "type": "array",
      "description": "The main array containing all defined content pillars.",
      "items": {
        "type": "object",
        "properties": {
          "pillar_name": {
            "type": "string",
            "description": "A short, clear title for the core topic."
          },
          "pillar_goal": {
            "type": "string",
            "description": "The brand or business objective this pillar serves (e.g., Education, Promotion, Trust)."
          },
          "target_audience_segment": {
            "type": "string",
            "description": "The specific audience persona this pillar is aimed at."
          },
          "key_head_term": {
            "type": "string",
            "description": "The primary, high-level keyword or topic for SEO."
          },
          "pillar_definition": {
            "type": "string",
            "description": "A 1-2 sentence description of what the pillar covers."
          },
          "sub_pillars": {
            "type": "array",
            "description": "Array of specific, in-depth sub-topics or topic clusters.",
            "items": {
              "type": "object",
              "properties": {
                "sub_pillar_name": {
                  "type": "string",
                  "description": "The name of the mid-level theme or topic cluster."
                },
                "buyer_journey_stage": {
                  "type": "string",
                  "description": "Which stage of the customer journey this content addresses (e.g., Awareness, Consideration, Decision)."
                },
                "content_ideas": {
                  "type": "array",
                  "description": "Specific titles or concepts for individual content pieces.",
                  "items": {
                    "type": "object",
                    "properties": {
                      "idea_title": {
                        "type": "string"
                      },
                      "target_keywords": {
                        "type": "array",
                        "items": {
                          "type": "string"
                        },
                        "description": "Specific, long-tail keywords for the content idea."
                      },
                      "content_mapping": {
                        "type": "array",
                        "description": "Mapping to format and channels.",
                        "items": {
                          "type": "object",
                          "properties": {
                            "primary_format": {
                              "type": "string",
                              "description": "e.g., Long-form blog, Video tutorial, Infographic."
                            },
                            "distribution_channel": {
                              "type": "string",
                              "description": "e.g., Website Blog, YouTube, Instagram Reels."
                            },
                            "repurposing_opportunities": {
                              "type": "string",
                              "description": "How the content can be reused (e.g., Pulling tips for social carousel)."
                            },
                            "call_to_action": {
                              "type": "string",
                              "description": "The desired audience action."
                            }
                          },
                          "required": ["primary_format", "distribution_channel"]
                        }
                      }
                    },
                    "required": ["idea_title"]
                  }
                }
              },
              "required": ["sub_pillar_name"]
            }
          },
          "performance_review": {
            "type": "object",
            "description": "Optional section for tracking and review.",
            "properties": {
              "start_date": {
                "type": "string",
                "format": "date",
                "description": "When the pillar was officially launched."
              },
              "performance_metrics": {
                "type": "array",
                "items": {
                  "type": "string"
                },
                "description": "The specific KPIs to measure success (e.g., Time on Page, Traffic Share)."
              },
              "review_date": {
                "type": "string",
                "format": "date",
                "description": "When the pillar's performance will be audited."
              },
              "status_notes": {
                "type": "string",
                "description": "Current status and key takeaways."
              }
            }
          }
        },
        "required": ["pillar_name", "pillar_goal", "pillar_definition"]
      }
    }
  },
  "required": ["pillars"]
}


```
