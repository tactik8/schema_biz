# Prompt

## Properties

|Property | Expected Type | Description |
|--- |--- |--- |
|name | Text | The name of the prompt. |
|description | Text | The description of the prompt (what it does).   |
|businessProcess | Text | The business process supported by this prompt (if applicable).  |
|subjectMatter | Text | The subject matter represented by this prompt (project management, marketing, etc).  |
|deliverable | text | The deliverable produced by this prompt. |
|outputJsonSchema | text | The json schema required of the output |
|outputExample | Text | An exampl eof the output | 
|promptElement | PromptItem | A list of the prompt items part of this prompt. |

## Example 

```

{
  "@type": "Prompt",
  "@id": "prompt01",
  "name": "Base prompt",
  "description": "Bas eprompt to be used for any situations",
  "businessProcess": "businessProcess",
  "subjectMatter": "subjectMatter",
  "deliverable": "deliverable",
  "outputJsonSchema": "Bas eprompt to be used for any situations",
  "outputExample": "Bas eprompt to be used for any situations",
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

"type": 
"string"
},
"description": 
{
"type": 
"string"
},
"businessProcess": 
{
"type": 
"string"
},
"subjectMatter": 
{
"type": 
"string"
},
"deliverable": 
{
"type": 
"string"
},
"outputJsonSchema": 
{
"type": 
"string"
},
"outputExample": 
{
"type": 
"string"
},
"promptElement": 
{
"type": 
"array",
"items": 
{
"type": 
"object",
"properties": 
{
"@type": 
{
"type": 
"string"
},
"@id": 
{
"type": 
"string"
},
"promptID": 
{
"type": 
"string"
},
"promptCategory": 
{
"type": 
"string"
},
"position": 
{
"type": 
"integer"
},
"text": 
{
"type": 
"string"
}
}
}
}
}
}
}


```
