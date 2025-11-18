# CampaignMembership

## Properties 

| **Field Name** | **Schema.org Type / JSON Type** | **Description** | 
| :--- | :--- | :--- | 
| **@context** | URL | Defines the vocabulary used (Schema.org). | 
| **@type** | Text (Schema Type) | Specifies the main entity type (`CommunicateAction` for a campaign). | 
| **member** | Text | A member of a ProgramMembership. Organizations can be members of CampaignMembership. | 
| **inclusionDate** | Date | The date the member was added to the Campaign |
| **exclusionDate** | Date | The date the member was excluded from the Campaign |
| **campaignMemberStatus** | CampaignMemberStatus | The status of the member (potantialCampaignMemberStatus, activeCampaignMemberStatus, convertedCampaignMemberStatus, failedCampaignMemberStatus, excludedCampaignMemberStatus) |
| **campaignInteraction** | CampaignInteraction | The interactions with the member for this campaign |


## Example 

```
{
  "@type": "",
  "@id": "Some id",
  "member": {
    "@type": "Person",
    "@id": "Some person"
  },
  "inclusionDate": "",
  "exclusionDate": "xxx",
  "campaignMemberStatus": "xxx",
  "campaignInteraction": [
    {
      "@type": "CommunicateAction"
      
    }
  ],
 }




```
