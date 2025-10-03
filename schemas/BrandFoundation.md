# BrandFoundation

## Properties
|Property | Expected Type | Description |
|--- |---|---|
| brandMission | Text | MIssion statement | 
| brandVision | Text | Vision Statement |
| brandCoreValues | Text | Core values | 
| brandStory | Text | Story | 
| brandPersonality |  Text | Personality | 
| primaryAudience | PeopleAudience | The different audiences |
| secondaryAudience | PeopleAudience | The different audiences |
| negativeAudience | PeopleAudience | Audiences to be forcibly excluded. |



## Example
```
 {
   "@type": "BrandFoundation",
   "brandMission": "xxx",
   "brandCoreValues": "xxx",
   "brandStory": "xxx",
   "brandPersonality": "xxx",
   "primaryAudience":  {
       "@type": "PeopleAudience",
       "name": "Bob the builder"
   },
   "secondaryAudience":  {
       "@type": "PeopleAudience",
       "name": "Bob the builder2"
   },
   "negativeAudience":  {
       "@type": "PeopleAudience",
       "name": "Bob the builder3"
   }
 }
```
