# PromptItem
An item that is part of the prompt. Items are text content that are associated with a role. 
## Properties

|Property | Expected Type | Description |
|--- |--- |--- |
|promptID| Text |  The id of the prompt |
|promptCategory | Text | The category of the prompt (role, task, context, output format, constraints)  |
|position | Number | The position of the prompt line with respect to the other prompt lines. |
|text | Text | The actual text of the prompt ("You are a helpful agent") |

## Example

```

{
  "@type": "PromptItem",
  "@id": "abc23",
  "promptID": "prompt1",
  "promptCategory": "role",
  "position": 2,
  "text": "You are a helpful agent"
}


```


## JSON Schema

```
{
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
            "description": "The category of the prompt (role, task, context, output format, constraints)  "
        },
        "position": {
            "type": "integer",
            "description": "The position of the prompt line with respect to the other prompt lines."
        },
        "text": {
            "type": "string",
            "description": "The actual text of the prompt ("You are a helpful agent")"
        }
    }
}


```
