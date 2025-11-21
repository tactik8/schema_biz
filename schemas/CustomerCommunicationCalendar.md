# CustomerCommunicationCalendar 
Schedule that organizes and plans all content a company will create and publish, including details like topics, authors, due dates, and publication dates. It's a strategic tool used to track a content pipeline, ensure a consistent publishing schedule, and coordinate team efforts for various content formats such as blog posts, social media updates, and newsletters. 

## Properties 

|Property | Expected Type | Description |
|--- |---|---|
| name | text | A short, clear, and catchy title for the core topic.	 | 
| pillarFamily | text | Why does this pillar exist? Education, Entertainment, Insprational, Promotional, Engagement, Timely |
| TargetAudience | PersonAudience | Which specific part of your audience persona is this pillar primarily aimed at?	 | 
| Stage of Buyer's Journey | text | Which stage of the journey does this content address? (e.g., Awareness, Consideration, Decision).	|



## Example

```
{
  "@context": "https://schema.org",
  "@type": "Event",
  "name": "Q4 Holiday Product Catalog Email Campaign",
  "startDate": "2025-12-05T10:00:00-05:00",
  "endDate": "2025-12-05T10:05:00-05:00",
  "eventStatus": "https://schema.org/EventScheduled",
  "description": "Launch of the main holiday catalog email, featuring curated gift bundles for high-value customers.",
  
  "organizer": {
    "@type": "Organization",
    "name": "Acme Retail Co.",
    "email": "marketing@acmeretail.com"
  },
  
  "workPerformed": {
    "@type": "CreativeWork",
    "name": "Holiday Catalog Email V3",
    "encodingFormat": "text/html",
    "isAccessibleForFree": "true",
    "text": "The final HTML content of the email, or a link to the creative asset.",
    "keywords": "holiday, catalog, email, Q4, retail",
    "mainEntityOfPage": "https://campaign-drafts.acmeretail.com/holiday-v3"
  },
  
  "audience": {
    "@type": "Audience",
    "name": "High-Value Repeat Purchasers (Segment ID: 4B)",
    "description": "Customers who have placed 3+ orders in the last 12 months with an AOV > $150.",
    "audienceType": "Customer Segment",
    "geographicArea": "USA & Canada"
  },
  
  "about": {
    "@type": "Action",
    "name": "Customer Retention",
    "result": {
      "@type": "QuantitativeValue",
      "name": "Target Open Rate",
      "value": "25%",
      "unitText": "Percent"
    }
  }
}


```


## JSON Schema

```

{
  "$schema": "http://json-schema.org/draft-07/schema#",
  "$id": "http://example.com/schemas/commCalendarEvent.json",
  "title": "CustomerCommunicationCalendar",
  "description": "Schema for storing customer communication calendar.",
  "type": "object",
  "properties": {
    "@context": {
      "type": "string",
      "description": "The JSON-LD context, typically set to https://schema.org."
    },
    "@type": {
      "type": "string",
      "description": "The primary Schema.org type, typically 'Event' for a scheduled item."
    },
    "name": {
      "type": "string",
      "description": "A concise, descriptive name for the communication campaign or event."
    },
    "events": {
      "type": "array",
      "items": {
        "$schema": "http://json-schema.org/draft-07/schema#",
        "title": "CustomerCommunicationCalendarEvent",
        "description": "Schema for validating a scheduled customer communication event (e.g., email, social post).",
        "type": "object",
        "properties": {
          "@context": {
            "type": "string",
            "description": "The JSON-LD context, typically set to https://schema.org."
          },
          "@type": {
            "type": "string",
            "description": "The primary Schema.org type, typically 'Event' for a scheduled item."
          },
          "name": {
            "type": "string",
            "description": "A concise, descriptive name for the communication campaign or event."
          },
          "startDate": {
            "type": "string",
            "format": "date-time",
            "description": "The precise date and time when the communication is scheduled to be launched (ISO 8601 format)."
          },
          "endDate": {
            "type": "string",
            "format": "date-time",
            "description": "The expected end date or time of the communication deployment window."
          },
          "eventStatus": {
            "type": "string",
            "description": "The status of the event (e.g., EventScheduled, EventPostponed)."
          },
          "description": {
            "type": "string",
            "description": "A detailed description of the communication's content and goal."
          },
          "workPerformed": {
            "type": "object",
            "description": "Details about the creative asset (the content) being communicated.",
            "properties": {
              "@type": {
                "type": "string",
                "description": "The type of creative work, e.g., 'CreativeWork', 'EmailMessage', or 'VideoObject'."
              },
              "name": {
                "type": "string",
                "description": "The internal name or version of the creative asset."
              },
              "encodingFormat": {
                "type": "string",
                "description": "The file format of the content (e.g., 'text/html', 'video/mp4')."
              },
              "contentUrl": {
                "type": "string",
                "format": "uri",
                "description": "A URI pointing to the final asset file or draft."
              }
            },
            "required": [
              "@type",
              "name"
            ]
          },
          "audience": {
            "type": "object",
            "description": "Details about the target customer segment or audience receiving the communication.",
            "properties": {
              "@type": {
                "type": "string",
                "description": "The Schema.org type, typically 'Audience'."
              },
              "name": {
                "type": "string",
                "description": "The human-readable name of the audience segment (e.g., 'High-Value Purchasers')."
              },
              "audienceType": {
                "type": "string",
                "description": "A classification of the audience (e.g., 'Customer Segment', 'Social Media Followers')."
              }
            },
            "required": [
              "@type",
              "name"
            ]
          },
          "about": {
            "type": "object",
            "description": "The strategic objective or goal this communication supports.",
            "properties": {
              "@type": {
                "type": "string",
                "description": "The Schema.org type, typically 'Action' or 'Goal'."
              },
              "name": {
                "type": "string",
                "description": "The name of the strategic action (e.g., 'Customer Retention', 'Lead Generation')."
              }
            },
            "required": [
              "@type",
              "name"
            ]
          }
        },
        "required": [
          "@context",
          "@type",
          "name",
          "startDate",
          "workPerformed",
          "audience"
        ]
      }
    },
    "required": [
      "@context",
      "@type",
      "name",
      "events"
    ]
  }
}

```
