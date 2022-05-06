# Predicting Heat: 
## Modeling the Urban Heat Island Effect in Seattle
<img width="938" alt="Screen Shot 2022-05-05 at 5 31 50 PM" src="https://user-images.githubusercontent.com/98435077/167048212-b24f039c-a111-4453-838c-3ecd62a5404c.png">

### RESEARCH QUESTION
What areas of Seattle are more likely to experience hotter temperatures due to the Urban Heat Island Effect? 

Urban Heat Islands (UHI), which cause higher temperatures in urban areas when compared to rural or suburban areas, are the result of a high concentration of impervious surfaces that absorb heat, density of buildings coupled with a lack of vegetation, and pollutants trapped in the atmosphere from industry and vehicle emissions. UHIs not only lead to warmer temperatures in cities but increase energy emissions and can lead to heat-related injuries and even death. While UHIs are not solely caused by Climate Change, they are exasperated by an increased frequency of extreme heat events. This project attempts to model areas of the city that will be more vulnerable to higher temperatures by measuring risk factors.

### MOTIVATION
Seattle has a historically temperate climate, but in recent years, due to anthropogenic climate change, the number of extreme heat events has increased. Seattle experienced its hottest day in recorded history on June 28th, 2021, when temperatures peaked at 108°. Before 2021, Seattle had only recorded four days where temperatures peaked over 100°; there were three such days in 2021. The effects of Urban Heat Islands can increase the air temperature in a city by between 2 and 8°C (Mohajerani et al., 2017) and exacerbate heat-related health risks for vulnerable populations. As a famously rainy city, Seattle is entirely unprepared to handle and respond to extreme heat. By identifying areas that are more vulnerable to the Urban Heat Island Effect, this project seeks to expose spatial inequities and encourage government intervention to reduce the severity of UHI.

### METHODOLOGY
According to a body of scientific research (include sources), the most significant contributors to the Urban Heat Island effect are the prevalence of dark impermeable surfaces, thermal mass from buildings, lack of vegetation or tree canopy, and increased air pollution from heavy industry and vehicle emissions. This report attempts to measure, normalize, and weigh the prevalence of these factors to model areas of the city that will experience hotter temperatures and be more vulnerable to extreme heat events. Data is aggregated at the Census Tract level.

### Urban Canopy: 
A robust urban canopy has been shown to lower urban temperatures, reduce air pollution, and preserve biodiversity (United Nations, 2018). When areas lack tree coverage, they are more likely to experience warmer temperatures. To compare urban canopies throughout the city, I gathered 2015 street tree data from an inventory created by the City of Seattle that cataloged the location, condition, and ownership of every street tree in the city. While this data set is several years old, it is the most recent and comprehensive available data set on street trees in the city. 

<img width="375" align="center" alt="Screen Shot 2022-05-05 at 11 04 23 AM" src="https://user-images.githubusercontent.com/98435077/166985457-063d387a-27e4-4ef4-8c01-0c31975c9506.png">

To measure the density of the urban canopy, I calculated the number of trees per census tract and normalized it by the area of each census tract minus the area of parkland in each tract. It is important to note that trees on parkland are not included in the trees data set, which could skew the data and give the impression that census tracts with large parks have a less dense canopy. By subtracting the area that is parkland, which for the most part is heavily forested, we can get a better understanding of the actual density of urban canopy in each census tract.

<img width="375" align="center" alt="Screen Shot 2022-05-05 at 11 04 57 PM" src="https://user-images.githubusercontent.com/98435077/167076092-bfd1f652-24c0-4bc9-ad5c-7b2fd27fafc0.png">

It is clear from fig 2. That North Seattle (north of 85th Street) and the Duwamish River Valley have a sparser urban canopy than wealthier, more central areas of the city like Capitol Hill and Freemont. 

### Air Pollution:
Air pollution is a major contributor to increased temperatures in cities. The release of greenhouse gases through air pollutants is not only a significant cause of climate change, but it also has acute warming effects on the areas surrounding the pollution source. This project focuses on vehicle emissions pollution and industrial pollution as together they are responsible for over half of air pollution in cities (EPA).

**_Vehicle Traffic_**

Vehicle emissions from trucks and passenger vehicles account for 82% of U.S. transportation sector greenhouse gas emissions (EPA). By combining 2018 Seattle streets traffic data with 2018 State highway data, I was able to map the relative vehicle traffic on Seattle Streets.

<img width="400" align="center" alt="Screen Shot 2022-05-05 at 3 22 44 PM" src="https://user-images.githubusercontent.com/98435077/167034975-1b87f0d8-562f-4e39-ae71-b792dd4fd9a2.png">

According to a recent study, the negative impacts of air pollution from vehicle emissions are most acute within 1,000ft of congested roadways (Barboza, 2017). To visualize the areas most impacted by air pollution from increased traffic, I created a 1,000ft buffer of streets where the Average Annual Daily Traffic (AADT) exceeded 50,000 vehicles. An AADT of 50,000 or higher is generally accepted as the threshold for high-volume routes by the U.S. Department of Transportation.

<img width="375" align="center" alt="Screen Shot 2022-05-05 at 4 25 16 PM" src="https://user-images.githubusercontent.com/98435077/167044695-6c7754cb-af52-4fd0-ad57-3ee10f40b161.png">

The map above shows the percentage of each census tract within 1,000ft of a high-volume roadway. Highway 99, I-5, I-90, 520, and the West Seattle Bridge, as well as a few other smaller road segments, make up the roads with the highest number of daily trips. Therefore, the communities surrounding these roads are shouldering a disproportionate percentage of vehicle emission pollution in the city.

<img width="375" align="center" alt="Screen Shot 2022-05-05 at 4 50 57 PM" src="https://user-images.githubusercontent.com/98435077/167045549-f0081083-e9a3-4628-9907-168f9d32ca9b.png">

Finally, I aggregated the percentage of each census tract within 1,000ft feet of a high-volume route. Since most of these high-volume roadways run north-south through the center of the city, census tracts that border the Puget Sound (west) or Lake Washington (east) are less likely to experience air pollution from vehicle emissions.

**_Industrial Areas_**

One of the other largest emitters of air pollution are industrial facilities. Since I couldn’t find a point data set listing all of the industrial emitters, my next best option was to use Seattle City Zoning Maps to isolate industrial zoned land and use it as a proxy for industry location. While this is likely overinclusive in its scope and fails to reveal potential differences between industrial zoned land, it gives us a good picture of where industrial uses take place in the city and, therefore, where air pollution is likely to be higher.

<img width="375" align="center" alt="Screen Shot 2022-05-05 at 3 31 58 PM" src="https://user-images.githubusercontent.com/98435077/167038304-5ee4ed64-f1d1-4953-b6d4-462a0d3b2aa8.png">

Like the Road Buffer, the map below shows the percentage of each census tract zoned as industrial. 

<img width="375" align="center" alt="Screen Shot 2022-05-05 at 5 59 31 PM" src="https://user-images.githubusercontent.com/98435077/167050018-9ef15dab-0834-4f61-b375-86979e0f05b2.png">

### Dark Surfaces:
**Figure 4.**
<img width="375" align="center" alt="Screen Shot 2022-05-05 at 3 43 37 PM" src="https://user-images.githubusercontent.com/98435077/167038243-ef64971f-5e02-44bd-be95-2bb279021acf.png">

<img width="360" align="center" alt="Screen Shot 2022-05-05 at 4 16 53 PM" src="https://user-images.githubusercontent.com/98435077/167044724-84e690d6-47df-4dc8-9c64-6776025f3c1a.png">

### Building Density/ Thermal Mass
Nearly half of all developable land in Seattle is zoned for single family housing (Adlin, 2021). While upzoning or building denser is typically heralded as a solution to urban sprawl and a way to reduce green house gas emissions, denser, larger buildings also absorb more heat. As a proxy to understand the effects of dense urban development on UHI, I analyzed the cities zoning code, combined areas of the city that are zoned as Commercial, Downtown, Mixed Use, Multi-Family Housing, and Major Institutions into a dense urban development category. While zoning is not a perfect proxy for thermal mass, it gives us a strong indication of where denser urban development exists in the city.

**Figure 5.** <img width="350" align="center" alt="Screen Shot 2022-05-05 at 11 57 56 AM" src="https://user-images.githubusercontent.com/98435077/167005201-89782b50-f629-48c0-97b8-b89242a65b1b.png">

**Figure 6.** <img width="375" align="center" alt="Screen Shot 2022-05-05 at 5 25 28 PM" src="https://user-images.githubusercontent.com/98435077/167048127-1835258e-df68-440e-a57a-bd0ff099fb0b.png">

### Weighting and Combining Data

### KEY FINDINGS
<img width="375" align="center" alt="Screen Shot 2022-05-05 at 11 13 39 PM" src="https://user-images.githubusercontent.com/98435077/167077112-b76e7f79-6c47-44a7-99ba-a02514a45efb.png">


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
