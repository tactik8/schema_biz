# ContentPillar 
Content pillars are the core themes or topics that guide a brand's content strategy, ensuring it remains focused, consistent, and relevant to its audience. They are specific categories that all content falls into, such as sustainable fashion guides or exercise tips, and help streamline content creation by making it easier to generate new ideas and align with business goals. 

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

  ## Consolidated Content Pillar Schema Documentation

| Object | Field Name (from JSON) | Data Type | Description |
| :--- | :--- | :--- | :--- |
| **Pillar** | **pillar\_name** | `string` | A short, clear title for the core topic. |
| **Pillar** | **pillar\_goal** | `string` | The brand or business objective this pillar serves (e.g., Education, Promotion, Trust). |
| **Pillar** | **target\_audience\_segment** | `string` | The specific audience persona this pillar is aimed at. |
| **Pillar** | **key\_head\_term** | `string` | The primary, high-level keyword or topic for SEO. |
| **Pillar** | **pillar\_definition** | `string` | A 1-2 sentence description of what the pillar covers. |
| **Pillar** | **sub\_pillars** | `array of objects` | Array of specific, in-depth sub-topics or topic clusters. |
| **Pillar** | **performance\_review** | `object` | Tracking and review metadata for the pillar. |
| **Sub-Pillar** | **sub\_pillar\_name** | `string` | The name of the mid-level theme or topic cluster. |
| **Sub-Pillar** | **buyer\_journey\_stage** | `string` | Which stage of the customer journey this content addresses (e.g., Awareness, Consideration, Decision). |
| **Sub-Pillar** | **content\_ideas** | `array of objects` | Specific titles or concepts for individual content pieces. |
| **Content Idea** | **idea\_title** | `string` | The working title for the content piece. |
| **Content Idea** | **target\_keywords** | `array of strings` | Specific, long-tail keywords for the content idea. |
| **Content Idea** | **content\_mapping** | `array of objects` | Mapping to content formats and distribution channels. |
| **Content Mapping**| **primary\_format** | `string` | The best content type for this piece (e.g., Blog Post, Video Tutorial). |
| **Content Mapping**| **distribution\_channel** | `string` | Where the content will primarily be shared (e.g., Website Blog, YouTube). |
| **Content Mapping**| **repurposing\_opportunities** | `string` | How the content can be reused (e.g., Pulling tips for social carousel). |
| **Content Mapping**| **call\_to\_action** | `string` | The desired audience action after consuming the content. |
| **Performance** | **start\_date** | `string` (date) | When the pillar was officially launched. |
| **Performance** | **performance\_metrics** | `array of strings` | The specific KPIs used to measure success (e.g., Time on Page, Traffic Share). |
| **Performance** | **review\_date** | `string` (date) | When the pillar's performance will be formally audited. |
| **Performance** | **status\_notes** | `string` | Current status and key takeaways. |
  
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

## Prompt example

```
{"@type":"Prompt","@id":"prompt-marketing-strategy-generator-v1","name":"Marketing Strategy Generator","description":"This prompt is designed to guide an AI agent in generating a comprehensive marketing strategy. It covers target audience analysis, key messaging, channel selection, budget allocation, and high-level timeline based on user-provided product/service details and marketing objectives.","requirements":"The user should provide details about their product or service, target demographic, specific marketing goals, and any budget constraints. The agent will then synthesize this information into a structured marketing plan.","businessProcess":"Marketing and Brand Management","subjectMatter":"Marketing Strategy, Digital Marketing, Brand Positioning, Market Research","deliverable":"A structured marketing strategy document in JSON format, ready for review and implementation.","outputJsonSchema":"{\"type\":\"object\",\"properties\":{\"strategyName\":{\"type\":\"string\",\"description\":\"The overall name or title for the marketing strategy.\"},\"productService\":{\"type\":\"string\",\"description\":\"A description of the product or service for which the strategy is being developed.\"},\"targetAudience\":{\"type\":\"string\",\"description\":\"A detailed profile of the primary target audience, including demographics, psychographics, and behaviors.\"},\"marketingGoals\":{\"type\":\"array\",\"items\":{\"type\":\"string\"},\"description\":\"Specific, measurable, achievable, relevant, and time-bound (SMART) marketing objectives.\"},\"keyMessages\":{\"type\":\"array\",\"items\":{\"type\":\"string\"},\"description\":\"The core messages and value propositions to be communicated to the target audience.\"},\"marketingChannels\":{\"type\":\"array\",\"items\":{\"type\":\"string\"},\"description\":\"A list of recommended marketing channels (e.g., social media, email, SEO, PR, content marketing) and why they are suitable.\"},\"budgetAllocation\":{\"type\":\"object\",\"properties\":{\"totalBudget\":{\"type\":\"number\",\"description\":\"The estimated total budget for the marketing strategy.\"},\"channelBreakdown\":{\"type\":\"object\",\"additionalProperties\":{\"type\":\"number\"},\"description\":\"Percentage or monetary breakdown of the budget across different marketing channels.\"}},\"description\":\"Proposed budget allocation across various marketing activities and channels.\"},\"timeline\":{\"type\":\"string\",\"description\":\"A high-level timeline or key phases for the strategy's implementation (e.g., 'Q3 2024 - Q1 2025').\"}},\"required\":[\"strategyName\",\"productService\",\"targetAudience\",\"marketingGoals\",\"keyMessages\",\"marketingChannels\"]}","outputExample":"{\"strategyName\":\"Launch Strategy for 'EcoBloom' Sustainable Skincare Line\",\"productService\":\"A new line of organic, cruelty-free, and ethically sourced skincare products focused on sustainability.\",\"targetAudience\":\"Environmentally-conscious women aged 25-45, urban dwellers, interested in natural beauty and ethical consumption. Values transparency and product efficacy.\",\"marketingGoals\":[\"Achieve 15% brand awareness in target demographic within 6 months\",\"Generate 5,000 online leads per month through digital channels\",\"Secure 10 partnerships with eco-friendly influencers/bloggers in Q1\",\"Attain 2% market share in the sustainable beauty segment within 1 year\"],\"keyMessages\":[\"Nourish your skin, nurture the planet: EcoBloom, where beauty meets sustainability.\",\"Pure ingredients, powerful results: experience nature's best for your skin.\",\"Ethical beauty for a conscious generation: feel good, look good.\"],\"marketingChannels\":[\"Instagram & TikTok Influencer Marketing (micro and nano-influencers)\",\"SEO-optimized blog content focusing on sustainable beauty tips and ingredient transparency\",\"Targeted Facebook and Instagram Ads with strong visual storytelling\",\"Email Marketing for nurturing leads and customer loyalty\",\"Partnerships with eco-conscious lifestyle blogs and online communities\"],\"budgetAllocation\":{\"totalBudget\":75000,\"channelBreakdown\":{\"influencers\":0.35,\"seo_content\":0.2,\"social_ads\":0.25,\"email_marketing\":0.1,\"partnerships\":0.1}},\"timeline\":\"Initial launch phase: Q4 2024 (Brand awareness & initial sales); Growth phase: Q1-Q2 2025 (Market penetration & loyalty building)\"}","promptElement":[{"@type":"PromptItem","@id":"prompt-item-role-v1","promptID":"prompt-marketing-strategy-generator-v1","promptCategory":"role","position":1,"text":"You are a highly experienced and creative marketing strategist with expertise in various industries, including digital, traditional, and brand marketing. You have a deep understanding of consumer behavior, market trends, and effective campaign development that drives measurable results."},{"@type":"PromptItem","@id":"prompt-item-task-v1","promptID":"prompt-marketing-strategy-generator-v1","promptCategory":"task","position":2,"text":"Your task is to generate a comprehensive and actionable marketing strategy. This strategy should clearly define the target audience, articulate compelling key messages, recommend suitable marketing channels, propose a budget allocation, and outline a high-level implementation timeline. Ensure the strategy is innovative, data-driven, and tailored to the specific product/service and marketing goals provided."},{"@type":"PromptItem","@id":"prompt-item-context-v1","promptID":"prompt-marketing-strategy-generator-v1","promptCategory":"context","position":3,"text":"The user will provide you with the following essential information: 1. A detailed description of the product or service. 2. Specific marketing goals (e.g., brand awareness, lead generation, sales increase). 3. Characteristics of the desired target audience. 4. Any relevant budget considerations or constraints. You must integrate these details thoroughly into your strategy."},{"@type":"PromptItem","@id":"prompt-item-output-format-v1","promptID":"prompt-marketing-strategy-generator-v1","promptCategory":"output format","position":4,"text":"Deliver the complete marketing strategy as a JSON object, strictly adhering to the provided JSON schema. Ensure all required fields within the schema are populated with relevant and well-structured content. Do not include any introductory or concluding remarks outside the JSON structure."},{"@type":"PromptItem","@id":"prompt-item-constraints-v1","promptID":"prompt-marketing-strategy-generator-v1","promptCategory":"constraints","position":5,"text":"The strategy must be realistic, actionable, and suitable for a typical 6-12 month implementation period. Avoid generic or overly theoretical advice; focus on practical steps. If specific details (e.g., exact budget) are not provided by the user, make reasonable, informed assumptions based on typical industry standards for similar products/services. Do not ask clarifying questions; generate the best possible strategy based on the available information and your expertise."}]}

```
