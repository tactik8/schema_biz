# BrandVisualIdentity

## Properties

|Property | Expected Type | Description |
|--- |--- |--- |
|logo | Logo | logo object |
|primaryColor | BrandColor | the color  |
|secondaryColor | BrandColor | the color  |
|accentColor | BrandColor | the color  |
|colorGuidelines | text | xxx|
|primaryTypeface | BrandTypeface | xxx |
|secondaryTypeface | BrandTypeface | xxx |
|typographyHierarchy | xxx | xxx |



## Example 

```
{
          "@type": "BrandVisualIdentity",
          "@id": "https://www.test.com#brandvisualidentity",
          "validFrom": "2022-01-01",
          "validThrough": "2028-01-01",          
          "primaryColor": {
                    "@type": "BrandColor",
                    "name": "Forest Green",
                    "description": "Our signature color representing growth and sustainability",
                    "hex": "#2D5016",
                    "RGB": "#2D5016",
                    "CMYK": "#2D5016",
                    "Pantone": "#2D5016"
          },
          "secondaryColor": {
                    "@type": "BrandColor",
                    "name": "Forest Green",
                    "description": "Our signature color representing growth and sustainability",
                    "hex": "#2D5016",
                    "RGB": "#2D5016",
                    "CMYK": "#2D5016",
                    "Pantone": "#2D5016"
          },
          "accentColor": {
                    "@type": "BrandColor",
                    "name": "Forest Green",
                    "description": "Our signature color representing growth and sustainability",
                    "hex": "#2D5016",
                    "RGB": "#2D5016",
                    "CMYK": "#2D5016",
                    "Pantone": "#2D5016"
          },
          "colorGuidelines": "Some guidelines.",
          "primaryTypeface": {
                      "@type": "DefinedTerm",
                      "name": "Montserrat",
                      "description": "Headers and display text",
                      "weights": "Bold (700), SemiBold (600), Medium (500),
                      "url": "https://fonts.google.com/specimen/Montserrat"
          },
          "secondaryTypeface": {
                      "@type": "DefinedTerm",
                      "name": "Montserrat",
                      "description": "Headers and display text",
                      "weights": "Bold (700), SemiBold (600), Medium (500),
                      "url": "https://fonts.google.com/specimen/Montserrat"
          },
          "typographyHierarchy": ""

}


```
