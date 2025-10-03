# VisualIdentity

## Properties

|Property | Expected Type | Description |
|--- |--- |--- |
|logo | Logo | logo object |
|colorPalette | ColorPalette | the color palette |
|typography | Typography | the typo | 
|graphicElements | ge | ge |


## Example 

```

 {
      "@type": "DefinedTerm",
      "name": "Visual Identity",
      
      "logo": {
        "@type": "ImageObject",
        "name": "Logo System",
        "description": "Full color horizontal lockup with leaf icon and wordmark",
        
        "variations": [
          {
            "@type": "ImageObject",
            "name": "Horizontal Logo",
            "description": "Standard for most applications"
          },
          {
            "@type": "ImageObject",
            "name": "Stacked Logo",
            "description": "For square formats (social media profile images)"
          },
          {
            "@type": "ImageObject",
            "name": "Icon Only",
            "description": "Minimum 24px, for app icons or small spaces"
          },
          {
            "@type": "ImageObject",
            "name": "Monochrome White",
            "description": "On dark backgrounds or photos"
          },
          {
            "@type": "ImageObject",
            "name": "Monochrome Black",
            "description": "On light backgrounds when color isn't available"
          }
        ],
        
        "minimumSize": {
          "print": "0.75 inches wide (horizontal), 0.5 inches (icon only)",
          "digital": "120px wide (horizontal), 32px (icon only)"
        }
      },
      
      "colorPalette": {
        "@type": "DefinedTerm",
        "name": "Color Palette",
        
        "primaryColors": [
          {
            "@type": "DefinedTerm",
            "name": "Forest Green",
            "description": "Our signature color representing growth and sustainability",
            "color": "#2D5016",
            "additionalProperty": [
              {
                "@type": "PropertyValue",
                "name": "HEX",
                "value": "#2D5016"
              },
              {
                "@type": "PropertyValue",
                "name": "RGB",
                "value": "45, 80, 22"
              },
              {
                "@type": "PropertyValue",
                "name": "CMYK",
                "value": "44, 0, 73, 69"
              },
              {
                "@type": "PropertyValue",
                "name": "Pantone",
                "value": "574 C"
              }
            ]
          },
          {
            "@type": "DefinedTerm",
            "name": "Cream",
            "description": "Warmth and approachability",
            "color": "#F5F1E8",
            "additionalProperty": [
              {
                "@type": "PropertyValue",
                "name": "HEX",
                "value": "#F5F1E8"
              },
              {
                "@type": "PropertyValue",
                "name": "RGB",
                "value": "245, 241, 232"
              },
              {
                "@type": "PropertyValue",
                "name": "CMYK",
                "value": "0, 2, 5, 4"
              },
              {
                "@type": "PropertyValue",
                "name": "Pantone",
                "value": "7527 C"
              }
            ]
          },
          {
            "@type": "DefinedTerm",
            "name": "Earth Brown",
            "description": "Coffee, richness, organic materials",
            "color": "#6B4423",
            "additionalProperty": [
              {
                "@type": "PropertyValue",
                "name": "HEX",
                "value": "#6B4423"
              },
              {
                "@type": "PropertyValue",
                "name": "RGB",
                "value": "107, 68, 35"
              },
              {
                "@type": "PropertyValue",
                "name": "CMYK",
                "value": "0, 36, 67, 58"
              },
              {
                "@type": "PropertyValue",
                "name": "Pantone",
                "value": "4695 C"
              }
            ]
          }
        ],
        
        "secondaryColors": [
          {
            "@type": "DefinedTerm",
            "name": "Sage Green",
            "description": "Supporting natural palette",
            "color": "#9CAF88",
            "additionalProperty": [
              {
                "@type": "PropertyValue",
                "name": "HEX",
                "value": "#9CAF88"
              },
              {
                "@type": "PropertyValue",
                "name": "RGB",
                "value": "156, 175, 136"
              },
              {
                "@type": "PropertyValue",
                "name": "CMYK",
                "value": "11, 0, 22, 31"
              }
            ]
          },
          {
            "@type": "DefinedTerm",
            "name": "Terracotta",
            "description": "Accent for calls-to-action",
            "color": "#C84B31",
            "additionalProperty": [
              {
                "@type": "PropertyValue",
                "name": "HEX",
                "value": "#C84B31"
              },
              {
                "@type": "PropertyValue",
                "name": "RGB",
                "value": "200, 75, 49"
              },
              {
                "@type": "PropertyValue",
                "name": "CMYK",
                "value": "0, 63, 76, 22"
              }
            ]
          },
          {
            "@type": "DefinedTerm",
            "name": "Warm Gray",
            "description": "Typography and subtle elements",
            "color": "#5C5552",
            "additionalProperty": [
              {
                "@type": "PropertyValue",
                "name": "HEX",
                "value": "#5C5552"
              },
              {
                "@type": "PropertyValue",
                "name": "RGB",
                "value": "92, 85, 82"
              },
              {
                "@type": "PropertyValue",
                "name": "CMYK",
                "value": "0, 8, 11, 64"
              }
            ]
          }
        ],
        
        "colorUsageGuidelines": "Use 70% primary colors, 20% secondary colors, 10% accent colors"
      },
      
      "typography": {
        "@type": "DefinedTerm",
        "name": "Typography",
        
        "primaryTypeface": {
          "@type": "DefinedTerm",
          "name": "Montserrat",
          "description": "Headers and display text",
          "additionalProperty": {
            "@type": "PropertyValue",
            "name": "Weights",
            "value": "Bold (700), SemiBold (600), Medium (500)"
          },
          "url": "https://fonts.google.com/specimen/Montserrat"
        },
        
        "secondaryTypeface": {
          "@type": "DefinedTerm",
          "name": "Merriweather",
          "description": "Body copy and long-form text",
          "additionalProperty": {
            "@type": "PropertyValue",
            "name": "Weights",
            "value": "Regular (400), Bold (700)"
          },
          "url": "https://fonts.google.com/specimen/Merriweather"
        },
        
        "typographyHierarchy": [
          {
            "@type": "DefinedTerm",
            "name": "H1",
            "description": "Montserrat Bold, 48pt / 3rem"
          },
          {
            "@type": "DefinedTerm",
            "name": "H2",
            "description": "Montserrat SemiBold, 36pt / 2.25rem"
          },
          {
            "@type": "DefinedTerm",
            "name": "H3",
            "description": "Montserrat SemiBold, 28pt / 1.75rem"
          },
          {
            "@type": "DefinedTerm",
            "name": "H4",
            "description": "Montserrat Medium, 22pt / 1.375rem"
          },
          {
            "@type": "DefinedTerm",
            "name": "Body",
            "description": "Merriweather Regular, 16pt / 1rem, line-height 1.6"
          },
          {
            "@type": "DefinedTerm",
            "name": "Small",
            "description": "Merriweather Regular, 14pt / 0.875rem"
          },
          {
            "@type": "DefinedTerm",
            "name": "Button",
            "description": "Montserrat SemiBold, 16pt / 1rem, uppercase, letter-spacing: 0.05em"
          }
        ]
      },
      
      "graphicElements": {
        "@type": "DefinedTerm",
        "name": "Graphic Elements",
        
        "patterns": [
          {
            "@type": "DefinedTerm",
            "name": "Leaf Pattern",
            "description": "Subtle repeating leaf motif for backgrounds"
          },
          {
            "@type": "DefinedTerm",
            "name": "Coffee Bean Scatter",
            "description": "Organic, hand-drawn coffee bean illustrations"
          }
        ],
        
        "iconStyle": {
          "@type": "DefinedTerm",
          "name": "Icon Style",
          "description": "Line icons, 2px stroke weight, rounded caps, 24x24px base grid"
        }
      }
    }


```
