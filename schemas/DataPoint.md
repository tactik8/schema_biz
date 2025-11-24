# DataPoint
One of many datapoint making up the value. Since values can comes from different sources. 


|Property |Expected Type |Description |
|---------|--------------|------------|
|object |Thing |The ref of the thing having the property |
|propertyID | string |The name of the property |
|value | Any |The actual value |
|dataFeed | DataFeed | The datafeed that proivded the value. |
|dataFeedItem | DataFeedItem | The dataFeedItem that provided the value. |
|agent | Person | The person that provided the value. |
|credibility | number | The credibility of this data point ( 0 to 1) |
|observationDate | Date | The date the data point has been observed. | 
