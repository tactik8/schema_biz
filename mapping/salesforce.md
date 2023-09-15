# Mapping Salesforce

## Objects
|Salesforce object |Schema type |
|------------------|------------|
|Account |Organization |
|Order | Order | 
|Work order |Action |
|Service appointment |Action |


## Field Mapping

### Organization
#### SF to schema
```jsonc {
  "@context": "https://schema.org/",
  "@id": record.id,
  "name": record.name,
  "legalName": record.legalName,
  "url": record.website
  }
  ```

  
  
