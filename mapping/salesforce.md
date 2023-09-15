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

#### Metadata
```json
  {
    "@metadata": {
      "source": {
          "@type": "schema:dataFeedItem",
          "sameAs": "https://www.salesforce.com/" + <object> + "/" + record.Id,
      },
      "observationDate": record.LastModifiedDate,
      "observationCredibility": ???,
      "agent": {
          "@type": "schema:person",
          "sameAs": "https://www.salesforce.com/user" + record.LastModifiedById
    }
  }
}
```
        


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
    "streetAddress": record.Address.Street,
    "sameAs": "https://www.salesforce.com/address/" + record.id
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
    "url": record.Website,
    "sameAs": "https://www.salesforce.com/account/" + record.Id
  }
  ```

#### Asset
```json
  {
    "@context": "https://schema.org/",
    "@type": "schema:person",
    "@id": ???,
    "serialNumber": record.SerialNumber,
    "category":
    "color":
    "depth":
    "gtin": 
    "height":
    "itemCondition":
    "manufacturer":
    "material":
    "model":
    "mpn":
    "productID",
    "productionDate": record.ManufactureDate, 
    "purchaseDate": record.PurchaseDate,
    "releaseDate":
    "sku": record.StockKeepingUnit,
    "weight":
    "width":
    "description":
    "name": record.Name,
    "image":
    "url":
    "sameAs": "https://www.salesforce.com/asset/" + record.Id, 
  }
```

#### Contact

```json
  {
    "@context": "https://schema.org/",
    "@type": "schema:person",
    "@id": ???,
    "additionalName": record.Name.MiddleName,
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
    "familyName": record.Name.FirstName,
    "givenName": record.Name.LastName,
    "honorificPrefix": record.Name.Salutation,
    "honorificSuffix": record.Name.Suffix,
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
    "url": record.Website,
    "sameAs": "https://www.salesforce.com/contact/" + record.Id
  }
  ```





#### Order
```json
  {
    "@context": "https://schema.org/",
    "@type": "schema:order",
    "@id": "",
    "billingAddress": Address(record.BillingAddress),
    "confirmationNumber":
    "customer": {
      "@type": "schema:organization":
      "sameAs": "https://www.salesforce.com/account/" + record.AccountId
    },
    "discount":
    "discountCode":
    "discountCurrency":
    "orderDate":
    "orderDelivery": {
      "@type": "schema:parcelDelivery", 
      "deliveryAddress": Address(record.ShippingAddress),
      "sameAs":  "https://www.salesforce.com/order/" + record.Id,
    },
    "orderNnumber":
    "orderStatus": record.status,
    "orderedItem": "",
    "partOfInvoive":
    "paymentDueDate":
    "paymentMethod":
    "paymentMethodId":
    "seller":
    "description": record.Description,
    "sameAs": "https://www.salesforce.com/order/" + record.Id

}

```


#### OrderProduct
```json

  {
    "@context": "https://schema.org/",
    "@type": "schema:order",
    "sameAs": "https://www.salesforce.com/order/" + record.OrderId,
    {
      "@context": "https://schema.org/",
      "@type": "schema:orderItem",
      "@id": "",
      "orderDelivery": {
        "@type": "schema:parcelDelivery", 
        "deliveryAddress": Address(record.ShippingAddress),
        "sameAs":  "https://www.salesforce.com/order/" + record.Id,
      },
      "orderItemNumber": record.OrderItemNumber,
      "orderItemstatus": "",
      "orderQuantity": Quantity,
      "orderedItem": {
        "@type": "schem:product",
        "sameAs": "https://www.salesforce.com/order/" + record.Product2Id,
      },
      "price": record.unitPrice,
      "priceCurrency": 
      "description": record.Description,
      "sameAs": "https://www.salesforce.com/order/" + record.Id
  
  }
}

```





#### Product2
```json
  {
    "@context": "https://schema.org/",
    "@type": "schema:person",
    "@id": "",
    "category":  "",
    "color": "",
    "depth": "",
    "gtin":  "",
    "height": "",
    "itemCondition": "",
    "manufacturer": "",
    "material": "",
    "model": "",
    "mpn": "",
    "productID", "https://www.salesforce.com/asset/" + record.ProductCode,
    "productionDate": record.ManufactureDate, 
    "purchaseDate": record.PurchaseDate,
    "releaseDate": "",
    "sku": record.StockKeepingUnit,
    "weight": "",
    "width": "",
    "description": record.Description,
    "name": record.Name,
    "image": "",
    "url": record.DisplayUrl,
    "sameAs": "https://www.salesforce.com/product2/" + record.Id
  }
```


  
  
