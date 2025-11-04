# Campaign

## Properties 

| **Field Name** | **Schema.org Type / JSON Type** | **Description** | 
| :--- | :--- | :--- | 
| **@context** | URL | Defines the vocabulary used (Schema.org). | 
| **@type** | Text (Schema Type) | Specifies the main entity type (`CommunicateAction` for a campaign). | 
| **name** | Text | The descriptive title of the marketing campaign. | 
| **description** | Text | A summary of the campaign's goals, channels, and duration. | 
| **identifier** | Text | A unique internal tracking code for the campaign. | 
| **actionStatus** | URL (Status Type) | The execution status of the action (e.g., `ActiveActionStatus`). | 
| **startDate** | Date | The official start date of the campaign. | 
| **endDate** | Date | The official end date of the campaign. | 
| **agent** | Organization | The entity responsible for conducting the campaign. | 
| *agent.name* | Text | Name of the organization. | 
| *agent.url* | URL | Website of the organization. | 
| **instrument** | DigitalDocument/WebPage (Array) | The specific assets and materials used to carry out the campaign (e.g., landing pages, creative briefs). | 
| *instrument\[\].name* | Text | Name of the specific instrument (e.g., "Campaign Landing Page"). | 
| *instrument\[\].url* | URL | URL of the instrument (if applicable). | 
| **about** | Product | The main product or service being promoted by the campaign. | 
| *about.name* | Text | Name of the product being promoted. | 
| *about.brand* | Brand | The brand identity of the product. | 
| **recipient** | Audience | The specific group of people the campaign is trying to reach. | 
| *recipient.name* | Text | A descriptive label for the target audience segment. | 
| *recipient.geographicArea* | Text | The primary location/region the campaign is running in. | 
| *recipient.audienceType* | Text | Detailed demographic or psychographic breakdown of the audience. |

## Example

```
{
    "@context": "https://schema.org",
    "@type": "CommunicateAction",
    "name": "Spring 2026 'Renew & Refresh' Digital Campaign",
    "description": "A focused, multi-channel campaign (social, search, email) running for 8 weeks to promote the new line of eco-friendly home appliances and drive first-time buyer conversions.",
    "identifier": "SR2026-001",
    "actionStatus": "https://schema.org/ActiveActionStatus",
    "startDate": "2026-03-01",
    "endDate": "2026-04-30",
    "agent": {
        "@type": "Organization",
        "name": "GreenLife Appliances Inc.",
        "url": "https://www.greenlife.com",
        "logo": "https://www.google.com/search?q=https://www.greenlife.com/logo.svg"
    },
    "instrument": [
        {
            "@type": "DigitalDocument",
            "name": "Campaign Creative Brief",
            "encodingFormat": "application/pdf"
        },
        {
            "@type": "WebPage",
            "name": "Campaign Landing Page",
            "url": "https://www.google.com/search?q=https://www.greenlife.com/refresh-2026"
        }
    ],
    "about": {
        "@type": "Product",
        "name": "GreenLife Eco-Washer Model 5000",
        "brand": {
            "@type": "Brand",
            "name": "GreenLife Eco"
        },
        "category": "Home Appliances"
    },
    "recipient": {
        "@type": "Audience",
        "name": "Environmentally Conscious Homeowners",
        "geographicArea": "North America",
        "audienceType": "Adults (30-55) with household income > $75k",
        "knowsLanguage": "en"
    }
}


```

## JSON Schema

```
{
  "$schema": "http://json-schema.org/draft-07/schema#",
  "title": "Marketing Campaign Schema (Schema.org CommunicateAction Model)",
  "type": "object",
  "description": "A JSON Schema definition for a marketing campaign, modeled after the Schema.org CommunicateAction type.",
  
  "properties": {
    "@context": {
      "type": "string",
      "description": "Defines the vocabulary used (must be 'https://schema.org')."
    },
    "@type": {
      "type": "string",
      "description": "Specifies the main entity type (must be 'CommunicateAction').",
      "enum": ["CommunicateAction"]
    },
    "name": {
      "type": "string",
      "description": "The descriptive title of the marketing campaign."
    },
    "description": {
      "type": "string",
      "description": "A summary of the campaign's goals, channels, and duration."
    },
    "identifier": {
      "type": "string",
      "description": "A unique internal tracking code for the campaign (e.g., 'SR2026-001')."
    },
    "actionStatus": {
      "type": "string",
      "description": "The execution status of the action (e.g., 'https://schema.org/ActiveActionStatus')."
    },
    "startDate": {
      "type": "string",
      "format": "date",
      "description": "The official start date of the campaign (YYYY-MM-DD)."
    },
    "endDate": {
      "type": "string",
      "format": "date",
      "description": "The official end date of the campaign (YYYY-MM-DD)."
    },
    
    "agent": {
      "$ref": "#/definitions/Organization",
      "description": "The organization responsible for running the campaign."
    },
    
    "about": {
      "$ref": "#/definitions/Product",
      "description": "The main product or service being promoted."
    },
    
    "recipient": {
      "$ref": "#/definitions/Audience",
      "description": "The specific group targeted by the campaign."
    },
    
    "instrument": {
      "type": "array",
      "description": "An array of specific assets and materials used to carry out the campaign (e.g., landing pages, creative briefs).",
      "items": { "$ref": "#/definitions/DigitalDocumentOrWebPage" }
    }
  },
  
  "required": ["@context", "@type", "name", "startDate", "endDate", "agent", "about", "recipient"],
  
  "definitions": {
    "Organization": {
      "type": "object",
      "description": "Schema for the Organization running the campaign.",
      "properties": {
        "@type": { "type": "string", "enum": ["Organization"] },
        "name": { "type": "string", "description": "Name of the organization." },
        "url": { "type": "string", "format": "url", "description": "Website of the organization." },
        "logo": { "type": "string", "format": "url", "description": "URL to the organization's logo." }
      },
      "required": ["@type", "name"]
    },
    "Product": {
      "type": "object",
      "description": "Schema for the Product being promoted.",
      "properties": {
        "@type": { "type": "string", "enum": ["Product"] },
        "name": { "type": "string", "description": "Name of the product." },
        "category": { "type": "string", "description": "The product's general category (e.g., 'Home Appliances')." },
        "brand": {
          "type": "object",
          "properties": {
            "@type": { "type": "string", "enum": ["Brand"] },
            "name": { "type": "string", "description": "The brand name." }
          },
          "required": ["@type", "name"]
        }
      },
      "required": ["@type", "name"]
    },
    "Audience": {
      "type": "object",
      "description": "Schema for the target Audience.",
      "properties": {
        "@type": { "type": "string", "enum": ["Audience"] },
        "name": { "type": "string", "description": "A descriptive label for the target audience segment." },
        "geographicArea": { "type": "string", "description": "The primary location/region the campaign is running in." },
        "audienceType": { "type": "string", "description": "Detailed demographic or psychographic breakdown." },
        "knowsLanguage": { "type": "string", "description": "The language the audience knows (ISO 639-1 code, e.g., 'en')." }
      },
      "required": ["@type", "name"]
    },
    "DigitalDocumentOrWebPage": {
      "type": "object",
      "description": "A campaign asset (e.g., brief, landing page).",
      "properties": {
        "@type": { "type": "string", "description": "Must be 'DigitalDocument' or 'WebPage'." },
        "name": { "type": "string", "description": "Name of the asset." },
        "url": { "type": "string", "format": "url", "description": "URL of the asset (required for WebPage)." },
        "encodingFormat": { "type": "string", "description": "File format (e.g., 'application/pdf' for DigitalDocument)." }
      },
      "required": ["@type", "name"]
    }
  }
}


```
