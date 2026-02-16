# BrandVisualIdentity

## Properties

|Property | Expected Type | Description |
|--- |--- |--- |
|logo | Logo | logo object |
|validFrom| Date | Start date |
|validThrough| Date | End date |
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
           "backgroundColor": {
                    "@type": "BrandColor",
                    "name": "White",
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
## JSON Schema

```
{
  "$schema": "https://json-schema.org/draft/2020-12/schema",
  "$id": "https://example.com/BrandVisualIdentitySchema.json",
  "title": "BrandVisualIdentity",
  "description": "Schema for describing the visual identity and guidelines of a brand.",
  "type": "object",
  "properties": {
    "@type": {
      "type": "string",
      "const": "BrandVisualIdentity",
      "description": "The type of object, which is 'BrandVisualIdentity'."
    },
    "@id": {
      "type": "string",
      "format": "uri",
      "description": "A unique identifier or URL for this brand visual identity record."
    },
    "validFrom": {
      "type": "string",
      "format": "date",
      "description": "The date from which this visual identity is valid (e.g., 'YYYY-MM-DD')."
    },
    "validThrough": {
      "type": "string",
      "format": "date",
      "description": "The date until which this visual identity is valid (e.g., 'YYYY-MM-DD')."
    },
    "primaryColor": {
      "description": "The primary color of the brand's palette.",
      "$ref": "#/$defs/BrandColor"
    },
    "secondaryColor": {
      "description": "The secondary color of the brand's palette.",
      "$ref": "#/$defs/BrandColor"
    },
    "accentColor": {
      "description": "The accent color used for highlights and calls-to-action.",
      "$ref": "#/$defs/BrandColor"
    },
    "backgroundColor": {
      "description": "The color used for backgrounds.",
      "$ref": "#/$defs/BrandColor"
    },
    "colorGuidelines": {
      "type": "string",
      "description": "Textual guidelines on how the brand colors should be used."
    },
    "primaryTypeface": {
      "description": "The primary typeface (font) used for headings and display text.",
      "$ref": "#/$defs/BrandTypeface"
    },
    "secondaryTypeface": {
      "description": "The secondary typeface (font) used for body text and supplementary content.",
      "$ref": "#/$defs/BrandTypeface"
    },
    "typographyHierarchy": {
      "type": "string",
      "description": "Textual guidelines or a description of the font size and usage hierarchy (e.g., H1, H2, body)."
    }
  },
  "required": [
    "@type",
    "@id"
  ],
  "$defs": {
    "BrandColor": {
      "type": "object",
      "description": "Defines a specific brand color with its name and color codes.",
      "properties": {
        "@type": {
          "type": "string",
          "const": "BrandColor"
        },
        "name": {
          "type": "string",
          "description": "The common name of the color (e.g., 'Forest Green')."
        },
        "description": {
          "type": "string",
          "description": "A brief description of what the color represents or its purpose."
        },
        "hex": {
          "type": "string",
          "description": "The hexadecimal color code including the hash.",
          "pattern": "^#([A-Fa-f0-9]{6}|[A-Fa-f0-9]{3})$"
        },
        "RGB": {
          "type": "string",
          "description": "The RGB color code in 'rgb(r,g,b)' format.",
          "pattern": "^rgb\\(\\s*(?:(?:\\d{1,3})\\s*,\\s*){2}(?:\\d{1,3})\\s*\\)$"
        },
        "CMYK": {
          "type": "string",
          "description": "The CMYK color code for print (e.g., 'c,m,y,k')."
        },
        "Pantone": {
          "type": "string",
          "description": "The Pantone Matching System (PMS) color code."
        }
      },
      "required": [
        "@type",
        "name"
      ]
    },
    "BrandTypeface": {
      "type": "object",
      "description": "Defines a specific typeface used in the brand identity.",
      "properties": {
        "@type": {
          "type": "string",
          "const": "BrandTypeface"
        },
        "name": {
          "type": "string",
          "description": "The name of the typeface (e.g., 'Montserrat')."
        },
        "description": {
          "type": "string",
          "description": "A description of the typeface's purpose."
        },
        "weights": {
          "type": "array",
          "description": "A list of available numeric font weights.",
          "items": {
            "type": "integer",
            "minimum": 100,
            "maximum": 900
          },
          "examples": [400, 700]
        },
        "url": {
          "type": "string",
          "format": "uri",
          "description": "A URL where the typeface can be found (e.g., Google Fonts)."
        }
      },
      "required": [
        "@type",
        "name"
      ]
    }
  }
}

```

