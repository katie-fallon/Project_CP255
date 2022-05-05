# Predicting Heat: 
## Modeling the Urban Heat Island Effect in Seattle


### RESEARCH QUESTION
What areas of Seattle are more likely to experience hotter temperatures due to the Urban Heat Island Effect? 

Urban Heat Islands (UHI), which cause higher temperatures in urban areas, are the result of a high concentration of impervious surfaces that absorb heat, density of buildings coupled with a lack of vegetation, and pollutants trapped in the atmosphere from industry and vehicle emissions. UHIs not only lead to warmer temperatures in cities but increase energy emissions and can lead to heat-related injuries and even death. While UHIs are not solely caused by Climate Change they are exasperated by an increased frequency of extreme heat events. This project attempts to model areas of the City that will be more vulnerable to higher temperatures by measuring risk factors.

### MOTIVATION
Seattle has a historically temperate climate, but in recent years, due to anthropogenic climate change, the prevelence of extreme weather events has increased. Seattle experienced its hottest day in recorded history on June 28th, 2021 when temperatures peaked at 108°. Before 2021, Seattle had only experienced 4 days over 100° ever. There were 3 days where temperatures reached over 100° in 2021. Extreme Heat, exasurbated by Urban Heat Islands, have negative health a disproportionate affect the cities most vulnerable populations. The effects of Urban Heat Islands can increase air temperature in an city by between 2 and 8°C (Mohajerani et. al, 2017).

### METHODOLOGY
According to a body of scientific research (include sources), the largest contributors to the Urban Heat Island effect are prevelance of dark surfaces, building density, lack of vegitation or tree canopy, and increased air pollution. This report attempts to measure, normalize, and weight the prevelance of these factors to model areas of the city that will experience hotter temperatures and be more vulnerable to extreme heat events. Data is aggregated at the Census Tract level. 

### Urban Canopy: 
To measure urban canopy, I gathered 2015 Street Tree data from the City of Seattle Data portal. It is important to note that trees on park land are not included in the Trees data set (fig. 1).

**Figure 1.** <img width="338" alt="Screen Shot 2022-05-05 at 11 04 23 AM" src="https://user-images.githubusercontent.com/98435077/166985457-063d387a-27e4-4ef4-8c01-0c31975c9506.png">

In order to measure the density of the urban canopy, I calculated the number of trees per census tract and normalized it by the area of each census tract minus the area of park land in each tract. By subtracting park land, which is mostly heavily forested, by the census tract area we can get a better understanding of the true distribution of urban canopy in each census tract.

### Air Pollution:
**_Vehicle Traffic_**

**Figure 2.** <img width="400" alt="Screen Shot 2022-05-05 at 3 22 44 PM" src="https://user-images.githubusercontent.com/98435077/167034975-1b87f0d8-562f-4e39-ae71-b792dd4fd9a2.png">

<img width="287" alt="Screen Shot 2022-05-05 at 4 25 16 PM" src="https://user-images.githubusercontent.com/98435077/167044695-6c7754cb-af52-4fd0-ad57-3ee10f40b161.png">

<img width="299" alt="Screen Shot 2022-05-05 at 4 44 52 PM" src="https://user-images.githubusercontent.com/98435077/167044703-c556a285-dfa0-4a52-99ee-34f12d0fb4b5.png">

**_Industrial Areas_**

**Figure 3.** <img width="273" alt="Screen Shot 2022-05-05 at 3 31 58 PM" src="https://user-images.githubusercontent.com/98435077/167038304-5ee4ed64-f1d1-4953-b6d4-462a0d3b2aa8.png">




### Dark Surfaces:
**Figure 4.**
<img width="277" alt="Screen Shot 2022-05-05 at 3 43 37 PM" src="https://user-images.githubusercontent.com/98435077/167038243-ef64971f-5e02-44bd-be95-2bb279021acf.png">

<img width="287" alt="Screen Shot 2022-05-05 at 4 16 53 PM" src="https://user-images.githubusercontent.com/98435077/167044724-84e690d6-47df-4dc8-9c64-6776025f3c1a.png">

### Building Density/ Thermal Mass
Nearly half of all developable land in Seattle is zoned for single family housing (Adlin, 2021). While upzoning or building denser is typically heralded as a solution to urban sprawl and a way to reduce green house gas emissions, denser, larger buildings also absorb more heat. As a proxy to understand the effects of dense urban development on UHI, I analyzed the cities zoning code, combined areas of the city that are zoned as Commercial, Downtown, Mixed Use, Multi-Family Housing, and Major Institutions into a dense urban development category. While zoning is not a perfect proxy for thermal mass, it gives us a strong indication of where denser urban development exists in the city.

**Figure 5.** <img width="350" alt="Screen Shot 2022-05-05 at 11 57 56 AM" src="https://user-images.githubusercontent.com/98435077/167005201-89782b50-f629-48c0-97b8-b89242a65b1b.png">

### Weighting and Combining Data

### KEY FINDINGS

### LIMITATIONS AND NEXT STEPS

### REFERENCES
You can use the [editor on GitHub](https://github.com/katie-fallon/Project_CP255/edit/main/README.md) to maintain and preview the content for your website in Markdown files.

Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.

### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [Basic writing and formatting syntax](https://docs.github.com/en/github/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/katie-fallon/Project_CP255/settings/pages). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://support.github.com/contact) and we’ll help you sort it out.
