# Brand 

## Properties 

|Property | Expected Type | Description |
|--- |---|---|
| brandFoundation | BrandFoundation | brandFoundation | 
| brandVisualIdentity | BrandVisualIdentity | BrandVisualIdentity |
| brandVoice | BrandVoice | BrandVoice | 
| brandPhotographyGuidelines | BrandPhotographyGuidelines | BrandPhotographyGuidelines | 
| brandApplications |  BrandApplications | BrandApplications | 
| brandStandards | BrandStandards | BrandStandards |



## Example

```
{
  "@context": "https://schema.org",
  "@type": "Organization",
  "name": "GreenLeaf Coffee Co.",
  "legalName": "GreenLeaf Coffee Co.",
  "url": "https://www.greenleafcoffee.com",
  "logo": "https://www.greenleafcoffee.com/logo.png",
  "foundingDate": "2018",
  "founder": {
    "@type": "Person",
    "name": "Sarah Chen",
    "jobTitle": "Founder & CEO"
  },
  "slogan": "Grown with Purpose. Roasted with Care.",
  "description": "GreenLeaf Coffee Co. is a sustainable coffee roaster partnering directly with farming cooperatives to produce exceptional specialty-grade coffee. We're committed to regenerative agriculture, fair pricing, and complete transparency—from the farm to your cup.",
  
  "brand": {
    "@type": "Brand",
    "name": "GreenLeaf Coffee Co.",
    "slogan": "Grown with Purpose. Roasted with Care.",
    
    "brandFoundation": {

      

    },
    
    "visualIdentity": {
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
    },
    
    "brandVoice": {
      "@type": "DefinedTerm",
      "name": "Brand Voice and Messaging",
      
      "voiceCharacteristics": [
        "Warm, not corporate",
        "Knowledgeable, not preachy",
        "Optimistic, not naive",
        "Conversational, not casual"
      ],
      
      "toneVariations": {
        "socialMedia": "Most casual, emoji usage okay, enthusiastic",
        "website": "Professional but warm, informative",
        "customerService": "Empathetic, solution-focused, patient",
        "technical": "Detailed, informative, still accessible",
        "sustainabilityReports": "Transparent, data-driven, honest about challenges"
      },
      
      "messagingPillars": [
        {
          "@type": "DefinedTerm",
          "name": "Direct Trade Partnership",
          "description": "We know our farmers by name. We visit farms, build long-term relationships, and pay 30% above fair trade minimums. No middlemen, no exploitation, just honest partnerships."
        },
        {
          "@type": "DefinedTerm",
          "name": "Regenerative Practices",
          "description": "Coffee farming can heal the planet. We work with farmers implementing regenerative agriculture—building soil health, increasing biodiversity, and sequestering carbon. Every bag helps restore ecosystems."
        },
        {
          "@type": "DefinedTerm",
          "name": "Exceptional Quality",
          "description": "Sustainability means nothing without amazing taste. Our beans score 85+ on specialty coffee scales. We roast in small batches to highlight each origin's unique character. Ethical and delicious aren't mutually exclusive."
        },
        {
          "@type": "DefinedTerm",
          "name": "Complete Transparency",
          "description": "Every bag includes the farm name, farmer cooperative, altitude, processing method, and the price we paid. Scan the QR code to see farm photos and impact data. No secrets, no greenwashing."
        }
      ],
      
      "writingStyleGuidelines": {
        "grammar": {
          "oxfordComma": true,
          "numbersSpelledOut": "one through nine",
          "numbersNumeric": "10+",
          "percentSymbol": true,
          "spacesAfterPeriod": 1
        },
        
        "terminology": {
          "preferred": [
            "farming partners",
            "regenerative agriculture",
            "direct trade",
            "carbon sequestration",
            "specialty-grade"
          ],
          "avoid": [
            "suppliers",
            "green farming",
            "cheap",
            "perfect",
            "revolutionary"
          ]
        }
      }
    },
    
    "photographyGuidelines": {
      "@type": "DefinedTerm",
      "name": "Photography and Imagery",
      
      "visualStyle": {
        "aesthetic": "Natural, warm, authentic, unposed",
        "mood": "Optimistic, grounded, human-focused",
        "colorPalette": "Earth tones, deep greens, warm browns, natural light",
        "feel": "Documentary meets lifestyle—real moments, not overly styled"
      },
      
      "subjectMatter": {
        "doFeature": [
          "Farmers and farming communities (with consent)",
          "Coffee plants in natural environments",
          "Hands working with coffee",
          "Small moments of coffee ritual",
          "Natural landscapes and biodiversity",
          "People genuinely connecting over coffee",
          "Behind-the-scenes"
        ],
        "avoid": [
          "Stock photos that feel generic",
          "Overly stylized flat lays",
          "People staring at phones",
          "Sad, poverty-focused imagery",
          "Perfect, untouchable luxury shots"
        ]
      },
      
      "lightingAndColor": {
        "lighting": "Natural light, golden hour preferred, soft diffused light",
        "colorGrading": "Warm with slightly lifted shadows",
        "avoid": "Heavy vignettes, oversaturation, cool tones"
      }
    },
    
    "brandApplications": {
      "@type": "DefinedTerm",
      "name": "Brand Applications",
      
      "printCollateral": {
        "businessCard": {
          "@type": "Product",
          "name": "Business Card",
          "width": "3.5 inches",
          "height": "2 inches",
          "material": "Recycled uncoated cardstock, 16pt thickness"
        },
        
        "letterhead": {
          "@type": "Product",
          "name": "Letterhead",
          "width": "8.5 inches",
          "height": "11 inches",
          "material": "100% recycled, natural white"
        }
      },
      
      "digitalApplications": {
        "website": {
          "@type": "WebSite",
          "name": "Website Design",
          "additionalProperty": [
            {
              "@type": "PropertyValue",
              "name": "Base Typography Size",
              "value": "16px"
            },
            {
              "@type": "PropertyValue",
              "name": "Grid Columns",
              "value": "12"
            },
            {
              "@type": "PropertyValue",
              "name": "Max Width",
              "value": "1200px"
            },
            {
              "@type": "PropertyValue",
              "name": "Spacing Unit",
              "value": "8px"
            }
          ]
        },
        
        "socialMedia": {
          "profileImage": "Stacked logo version on Cream background (square format)",
          "contentTemplates": [
            {
              "@type": "ImageObject",
              "name": "Instagram Post",
              "width": "1080px",
              "height": "1080px"
            },
            {
              "@type": "ImageObject",
              "name": "Instagram Story",
              "width": "1080px",
              "height": "1920px"
            },
            {
              "@type": "ImageObject",
              "name": "Facebook Post",
              "width": "1200px",
              "height": "630px"
            }
          ]
        }
      },
      
      "packaging": {
        "@type": "Product",
        "name": "Coffee Bag",
        "material": "Kraft paper with compostable liner, matte finish",
        "size": ["12oz", "2lb"],
        "additionalProperty": [
          {
            "@type": "PropertyValue",
            "name": "Front Elements",
            "value": "Logo, roast level indicator, origin name, tasting notes"
          },
          {
            "@type": "PropertyValue",
            "name": "Back Elements",
            "value": "Farm information, QR code, brewing recommendations, roast date"
          }
        ]
      }
    },
    
    "brandStandards": {
      "@type": "DefinedTerm",
      "name": "Brand Standards and Guidelines",
      
      "trademark": {
        "@type": "DefinedTerm",
        "name": "Trademark Usage",
        "firstMention": "GreenLeaf Coffee Co.™",
        "subsequentMentions": "GreenLeaf or GreenLeaf Coffee",
        "contactEmail": "legal@greenleafcoffee.com"
      },
      
      "copyright": {
        "@type": "DefinedTerm",
        "name": "Copyright Information",
        "copyrightNotice": "© 2024 GreenLeaf Coffee Co. All rights reserved."
      },
      
      "brandGovernance": {
        "approvalProcess": "All brand materials must be approved by Marketing Director",
        "updateProcess": "Brand book reviewed and updated quarterly",
        "contactEmail": "brand@greenleafcoffee.com"
      }
    }
  },
  
  "contactPoint": {
    "@type": "ContactPoint",
    "telephone": "+1-555-COFFEE",
    "contactType": "Customer Service",
    "email": "hello@greenleafcoffee.com",
    "availableLanguage": "English"
  },
  
  "address": {
    "@type": "PostalAddress",
    "streetAddress": "123 Roastery Lane",
    "addressLocality": "Portland",
    "addressRegion": "OR",
    "postalCode": "97201",
    "addressCountry": "US"
  },
  
  "sameAs": [
    "https://www.instagram.com/greenleafcoffee",
    "https://www.facebook.com/greenleafcoffee",
    "https://twitter.com/greenleafcoffee",
    "https://www.linkedin.com/company/greenleafcoffee"
  ]
}



```
