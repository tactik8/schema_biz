# ProjectActivity

## Properties 

| **Field Name** | **Schema.org Type / JSON Type** | **Description** | 
| :--- | :--- | :--- | 
| **@context** | URL | Defines the vocabulary used (Schema.org). | 
| **@type** | Text (Schema Type) | ProjectActivity | 
| **name** | Text | The descriptive title of the activity. | 
| **description** | Text | A summary of the activity. |
| **objectives** | Objective | The objectives of the activity |
| **activityStatus** | ActivityStatus | The status of the activity (potential, active, completed, canceled) | 
| **plannedStartDate** | Date | The date planned to begin activity | 
| **plannedEndDate** | Date | The date planned to end activity | 
| **plannedDuration** | Duration | The planned duration of the activity | 
| **plannedCost** | Number | Planned cost | 
| **actualStartDate** | Date | The date actual to begin activity | 
| **actualEndDate** | Date | The date actual to end activity | 
| **actualdDuration** | Duration | The planned duration of the activity | 
| **actualCost** | Number | Actual cost |
| **scheduleVariance** | Number | Variance |
| **schedulePerformanceIndex** | Number | SPI |
| **costVariance** | Number | Variance cost |
| **costPerformanceIndex** | Number | CPI |
| **activityOwner** | person, organization | The owner of the activity | 
| **activityContributors** | person, organization | The contributors of the activity | 
| **activityDeliverable** | Thing | The deliverables from the activity | 
| **hasPart** | Activity | Sub activities part of this activity | 
| **constraints** | ActivityConstraint | Constraints around start or finish of activity | 



### Objectives
| **@type** | Text | Objective | 
| **@id** | Text | The id | 
| **name** | Text | The name of the objective | 
| **description** | Activity | The description of the objective. | 
| **objectiveStatus** | Status | The status of the objective. | 
| **hasPart** | Objectives | Sub objectives | 
| **isPartOf** | Objectives | Objectives that this one is a part of | 


### ActivityDeliverable
| **@type** | Text | ActivityDeliverable | 
| **@id** | Text | The id | 
| **name** | Text | The name of the deliverable | 
| **description** | Activity | The activity that must start for this one to start | 
| **deliverableStatus** | Status | The status of the deliverable. | 
| **review** | Review | Reviews of the deliverable. |


### Constraints
| **@type** | Text | ActivityConstraint | 
| **@id** | Text | The id | 
| **finishToStart** | Activity | The activity that must finish for this one to start | 
| **startToStart** | Activity | The activity that must start for this one to start | 
| **finishToFinish** | Activity | The activity that must finish before fisnishing this one. | 
| **startNoEarlierThan** | Date | Constraints around start or finish of activity | 
| **startNoLaterThan** | Date | Constraints around start or finish of activity | 
| **finishtNoEarlierThan** | Date | Constraints around start or finish of activity | 
| **finishNoLaterThan** | Date | Constraints around start or finish of activity | 

