# Prompt

## Properties

|Property | Expected Type | Description |
|--- |--- |--- |
|name | Text | The name of the prompt. |
|description | Text | The description of the prompt (what it does).   |
|businessProcess | Text | The business process supported by this prompt (if applicable).  |
|subjectMatter | Text | The subject matter represented by this prompt (ex: project management, marketing, etc).  |
|deliverable | text | The deliverable produced by this prompt (ex: project plan, brand voice, marketing strategy) |
|outputJsonSchema | text | The json schema representations of the output from this agent.  |
|outputExample | Text | An example of the output. | 
|promptElement | PromptItem | A list of the prompt items part of this prompt. |

## Example 

```

{
  "@type": "Prompt",
  "@id": "prompt01",
  "name": "Base prompt",
  "description": "Base prompt to be used for any situations",
  "businessProcess": "businessProcess",
  "subjectMatter": "subjectMatter",
  "deliverable": "deliverable",
  "outputJsonSchema": "Base prompt to be used for any situations",
  "outputExample": "Base prompt to be used for any situations",
  "promptElement": [
      {
        "@type": "PromptItem",
        "@id": "abc23",
        "promptID": "prompt1",
        "promptCategory": "role",
        "position": 2,
        "text": "You are a helpful agent"
      },
      {
        "@type": "PromptItem",
        "@id": "abc23",
        "promptID": "prompt1",
        "promptCategory": "role",
        "position": 2,
        "text": "You are a helpful agent"
      },
      {
        "@type": "PromptItem",
        "@id": "abc23",
        "promptID": "prompt1",
        "promptCategory": "role",
        "position": 2,
        "text": "You are a helpful agent"
      }
  ]
}

```


## JSON Schema

```
{
  "type": "object",
  "$schema": "http://json-schema.org/draft-07/schema#",
  "title": "Generated Schema",
  "properties": {
      "@type": {
          "const": "United States of America",
          "description": "The class name of the record."
      },
      "@id": {
          "type": "string",
          "description": "The @id of the record."
      },
      "name": {
          "type": "string",
          "description": "The name of the prompt."
      },
      "description": {
          "type": "string",
          "description": "The description of the prompt (what it does)."
      },
      "businessProcess": {
          "type": "string",
          "description": " The business process supported by this prompt (if applicable). "
      },
      "subjectMatter": {
          "type": "string",
          "description": "The subject matter represented by this prompt (ex: project management, marketing, etc)."
      },
      "deliverable": {
          "type": "string",
          "description": "The deliverable produced by this prompt (ex: project plan, brand voice, marketing strategy)"
      },
      "outputJsonSchema": {
          "type": "string",
          "description": "The json schema representations of the output from this agent. "
      },
      "outputExample": {
          "type": "string",
          "description": " An example of the output."
      },
      "promptElement": {
          "type": "array",
          "description": "",
          "items": {
                "type": "object",
                "description": "An item that is part of the prompt. Items are text content that are associated with a role.",
                "properties": {
                    "@type": {
                        "constant": "PromptItem",
                        "description": "The class name of the record."
                    },
                    "@id": {
                        "type": "string",
                        "description": "The @id of the record."
                    },
                    "promptID": {
                        "type": "string",
                        "description": "The @id of the parent Prompt record (the Prompt object that this record is part of)"
                    },
                    "promptCategory": {
                        "type": "string",
                        "description": "The category of the prompt (role, task, context, output format, constraints)"
                    },
                    "position": {
                        "type": "integer",
                        "description": "The position of the prompt line with respect to the other prompt lines."
                    },
                    "text": {
                        "type": "string",
                        "description": "The actual text of the prompt ('You are a helpful agent')"
                    }
                }
            }
      }
  }
}


```
