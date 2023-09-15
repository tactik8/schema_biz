# Mapping Salesforce

## Objects
|Salesforce object |Schema type |
|------------------|------------|
|Account |Organization |
|Order | Order | 
|Work order |Action |
|Service appointment |Action |


## Field Mapping

### SF to schema

#### Address
```json
  {
    "@context": "https://schema.org/",
    "@type": "schema:postalAddress",
    "@id": ???,
    "addressCountry": record.Address.Country,
    "addressLocality": record.Address.City,
    "addressRegion": record.Address.State,
    "postalCode": record.Address.PostalCode,
    "streetAddress": record.Address.Street
  }
  ```

#### Account
```json
  {
    "@context": "https://schema.org/",
    "@type": "schema:organization",
    "@id": record.id,
    "description": record.Description
    "name": record.name,
    "legalName": record.legalName,
    "parentOrganization": {
      "@type": "schema:organization",
      "sameAs": "https://www.salesforce.com/account/" + record.ParentId
      },
    "url": record.Website
  }
  ```

#### Contact

```json
  {
    "@context": "https://schema.org/",
    "@type": "schema:person",
    "@id": ???,
    "address": {
        "@context": "https://schema.org/",
        "@type": "schema:postalAddress",
        "@id": ???,
        "addressCountry": record.MailingAddress.Country,
        "addressLocality": record.MailingAddress.City,
        "addressRegion": record.MailingAddress.State,
        "postalCode": record.MailingAddress.PostalCode,
        "streetAddress": record.MailingAddress.Street
    },
    "birthDate": record.Birthdate,
    "description": record.Description,
    "email": record.Email,
    "familyName": record.legalName,
    "givenName": record.legalName,
    "jobTitle": record.Title,
    "telephone": record.Phone,
    "workLocation": {
        "@context": "https://schema.org/",
        "@type": "schema:postalAddress",
        "@id": ???,
        "addressCountry": record.MailingAddress.Country,
        "addressLocality": record.MailingAddress.City,
        "addressRegion": record.MailingAddress.State,
        "postalCode": record.MailingAddress.PostalCode,
        "streetAddress": record.MailingAddress.Street
    },
    "worksFor": {
      "@type": "schema:organization",
      "sameAs": "https://www.salesforce.com/account/" + record.AccountId
      },
    "url": record.Website
  }
  ```

  
  
