# Opportunity

## Properties 

| **Field Name** | **Schema.org Type / JSON Type** | **Description** | 
| :--- | :--- | :--- | 
| **@context** | URL | Defines the vocabulary used (Schema.org). | 
| **@type** | Text (Schema Type) | Opportunity. | 
| **name** | Text | The descriptive title of the opportunity. | 
| **description** | Text | A summary of the opportunity. | 
| **opportunityStatus** | Status | Status |
| **OpportunityType** | OpportunityType | The OpportunityType | 
| **expectedRevenue** | Number | The expected revenue | 
| **plannedCloseDate** | Date | The planned date of closing. | 
| **actualCloseDate** | Date | The planned date of closing. | 
| **opportunityStage** | OpportunityStage | Stage of the opportunity | 
| **opportunityStageHistory** | OpportunityStage | The different opportunityStages | 
| **opportunityMember** | OpportunityRole | The people working on the opportunity | 



### OpportunityStage
| **Field Name** | **Schema.org Type / JSON Type** | **Description** | 
| :--- | :--- | :--- | 
| **@context** | URL | Defines the vocabulary used (Schema.org). | 
| **@type** | Text (Schema Type) | Opportunity. | 
| **name** | Text | The name of the stage. | 
| **description** | Text | The desc of the stage. | 
| **probability** | Number | Probability associated with the stage | 
| **stageStartDate** | Date | The date the stage started | 
| **stageEndDate** | Date | The date the stage end | 


### OpportunityType
| **Field Name** | **Schema.org Type / JSON Type** | **Description** | 
| :--- | :--- | :--- | 
| **@context** | URL | Defines the vocabulary used (Schema.org). | 
| **@type** | Text (Schema Type) | OpportunityType. | 
| **name** | Text | The name of the OpportunityType. | 
| **OpportunityStages** | OpportunityStage | The stages associated with the type. | 

### OpportunityRole
| **Field Name** | **Schema.org Type / JSON Type** | **Description** | 
| :--- | :--- | :--- | 
| **@context** | URL | Defines the vocabulary used (Schema.org). | 
| **@type** | Text (Schema Type) | OpportunityType. | 
| **name** | Text | The role. | 
| **roleMember** | Person | Pesrsona assuming the role | 
| **role** | Text | The role (owner, contrinutor, etc). | 
| **contributionPercentage** | Number | The percentage contributed. | 

