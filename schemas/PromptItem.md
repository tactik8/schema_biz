# PromptItem

## Properties

|Property | Expected Type | Description |
|--- |--- |--- |
|promptID| Text |  The id of the prompt |
|promptCategory | Text | The category of the prompt (role, task, context, output format, constraints)  |
|position | Nnumber | The position of the prompt line with respect to the other prompt lines. |
|text | Text | the actual text of the prompt ("You are a helpful agent") |

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
