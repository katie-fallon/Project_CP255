# Predicting Heat: 
## Modeling the Urban Heat Island Effect in Seattle
<img width="938" alt="Screen Shot 2022-05-05 at 5 31 50 PM" src="https://user-images.githubusercontent.com/98435077/167048212-b24f039c-a111-4453-838c-3ecd62a5404c.png">

### RESEARCH QUESTION
What areas of Seattle are more likely to experience hotter temperatures due to the Urban Heat Island Effect? Do Urban Heat Islands disproportionately impact already disadvantaged communities?

Urban Heat Islands (UHI), which cause higher temperatures in urban areas when compared to rural or suburban areas, are the result of a high concentration of impervious surfaces that absorb heat, density of buildings coupled with a lack of vegetation, and pollutants trapped in the atmosphere from industry and vehicle emissions. UHIs not only lead to warmer temperatures in cities but increase energy emissions and can lead to heat-related injuries and even death. While Urban Heat Islands are not solely created or caused by Climate Change, UHIs are exasperated by an increased frequency of extreme heat events. This project attempts to model areas of the city that will be more vulnerable to higher temperatures by measuring, weighting, and aggregating UHI risk factors. These results are then compared to the Office of Planning and Community Development’s (OPCD) Racial and Social Equity Index to analyze if disadvantaged communities are more likely to experience higher temperatures.

### MOTIVATION
Seattle has a historically temperate climate, but in recent years, due to anthropogenic climate change, the number of extreme heat events has increased. Seattle experienced its hottest day in recorded history on June 28th, 2021, when temperatures peaked at 108°. Before 2021, Seattle had only recorded four days where temperatures peaked over 100°. There were three such days in 2021. The effects of Urban Heat Islands can increase the air temperature in a city by between 2 and 8°C (Mohajerani et al., 2017) and exacerbate heat-related health risks for vulnerable populations. As a famously rainy city, Seattle is entirely unprepared to handle and respond to extreme heat. By identifying areas that are more vulnerable to increased temperatures due to the Urban Heat Island Effect, this project seeks to expose spatial inequities and encourage government intervention to reduce the severity of UHIs.


### METHODOLOGY & ANALYSIS
According to a body of scientific research, the most significant contributors to the Urban Heat Island effect are the prevalence of dark impermeable surfaces, thermal mass from buildings, lack of vegetation or tree canopy, and increased air pollution from heavy industry and vehicle emissions (Penny, 2019). This report attempts to measure, normalize, and weigh the prevalence of these factors to model areas of the city that will experience hotter temperatures and be more vulnerable to extreme heat events. 

The data used is aggregated at the Census Tract level. While this is helpful in understanding general UHI risk throughout the city, it does not allow us to see more nuanced differences within census tracts. Future studies could benefit from using a smaller unit of aggregation in their analysis.

### Urban Canopy: 
A robust urban canopy has been shown to lower urban temperatures, reduce air pollution, and preserve biodiversity (United Nations, 2018). When areas lack tree coverage, they are more likely to experience warmer temperatures. To compare urban canopies throughout the city, I gathered 2015 street tree data from an inventory created by the City of Seattle that cataloged every street tree's location, condition, and ownership. While this data set is several years old, it is the most recent and comprehensive available data set on street trees in the city.

<img width="371" alt="Screen Shot 2022-05-08 at 3 02 24 PM" src="https://user-images.githubusercontent.com/98435077/167323027-44fe57f2-3611-4fee-af90-7cd37db4213e.png">

To measure the density of the urban canopy, I calculated the number of trees per census tract and normalized it by the area of each census tract minus the area of parkland in each tract. It is important to note that trees on parkland are not included in the trees data set, which could skew the data and give the impression that census tracts with large parks have a less dense canopy. By subtracting the area that is parkland, which for the most part is heavily forested, we can get a better understanding of the actual density of urban canopy in each census tract.

<img width="373" alt="Screen Shot 2022-05-07 at 2 55 23 PM" src="https://user-images.githubusercontent.com/98435077/167273106-adc34715-5a9a-4bfc-b1a0-39ba217505c8.png">

It is clear from fig 2. That North Seattle (north of 85th Street) and the Duwamish River Valley have a sparser urban canopy than wealthier, more central areas of the city like Capitol Hill and Freemont.

### Air Pollution:
Air pollution is a significant contributor to increased temperatures in cities. The release of greenhouse gases through air pollutants is not only a significant cause of climate change, but it also has acute warming effects on the areas surrounding the pollution source. This project focuses on vehicle emissions pollution and industrial pollution as together they are responsible for over half of air pollution in cities (EPA).

**_Vehicle Traffic_**

Vehicle emissions from trucks and passenger vehicles account for 82% of U.S. transportation sector greenhouse gas emissions (EPA). By combining 2018 Seattle streets traffic data with 2018 state highway data, I was able to map the relative vehicle traffic on Seattle Streets.

<img width="369" alt="Screen Shot 2022-05-08 at 3 02 46 PM" src="https://user-images.githubusercontent.com/98435077/167317708-edb5591a-2c7e-43c3-8908-fcfaedf15bbc.png">

According to a recent study, the negative impacts of air pollution from vehicle emissions are most acute within 1,000ft of congested roadways (Barboza, 2017). To visualize the areas most impacted by air pollution from increased traffic, I created a 1,000ft buffer of streets where the Average Annual Daily Traffic (AADT) exceeded 50,000 vehicles. An AADT of 50,000 or higher is generally accepted as the threshold for high-volume routes by the U.S. Department of Transportation. 

<img width="373" alt="Screen Shot 2022-05-07 at 2 57 00 PM" src="https://user-images.githubusercontent.com/98435077/167273124-fd66665d-28cc-4b76-b7ea-38baec9a2ba5.png">

The map above shows the percentage of each census tract within 1,000ft of a high-volume roadway. Highway 99, I-5, I-90, 520, and the West Seattle Bridge, as well as a few other smaller road segments, make up a majority of the roads that average more than 50,000 trips a day. Therefore, the communities surrounding these roads are shouldering a disproportionate percentage of vehicle emission pollution in the city.

<img width="373" alt="Screen Shot 2022-05-07 at 2 57 40 PM" src="https://user-images.githubusercontent.com/98435077/167273134-cf0e320b-fd66-43b8-9a37-2f5c1729c132.png">

Finally, I aggregated the percentage of each census tract within 1,000ft feet of a high-volume route. Since most of these high-volume roadways run north-south through the city's center, census tracts that border the Puget Sound (west) or Lake Washington (east) are less likely to experience air pollution from vehicle emissions.

**_Industrial Areas_**

One of the other largest emitters of air pollution is industrial facilities. Since a point data set listing all industrial emitters was not available, my next best option was to use Seattle City Zoning Maps to isolate industrial zoned land and use it as a proxy for industry location. While this is likely overinclusive in its scope and fails to reveal potential differences between industrial zoned land, it gives us a good picture of where industrial uses occur in the city and, therefore, where air pollution is likely to be higher.

<img width="371" alt="Screen Shot 2022-05-07 at 2 58 13 PM" src="https://user-images.githubusercontent.com/98435077/167273143-8d62fe60-78f7-4741-81e3-d2ced97959d9.png">

A majority of Seattle’s Industrial zoned land surrounds the Duwamish River, an EPA superfund site that has suffered from over a century of industrial pollution. The remainder of Seattle’s Industrial zoned land is along the Lake Washington ship canal, the north shore of Elliott Bay, and sections of Lake Union. The map below shows the percentage of each census tract zoned as industrial.

<img width="373" alt="Screen Shot 2022-05-07 at 2 58 29 PM" src="https://user-images.githubusercontent.com/98435077/167273147-29e71c13-f65c-419a-98ce-32226392a9d2.png">

### Dark Surfaces:
Asphalt Concrete (AC) plays a significant role in higher urban temperatures. Asphalt has a lower albedo than other types of pavements. It is less reflective and absorbs more heat leading to increased street temperatures (Mohajerani et al., 2017). ![image](https://user-images.githubusercontent.com/98435077/167346294-e634d910-e86f-4fc3-82fb-7da791be9e3b.png)

<img width="369" alt="Screen Shot 2022-05-08 at 3 03 12 PM" src="https://user-images.githubusercontent.com/98435077/167317686-7aac3ee1-42e8-4674-8e52-446aa03e9e0f.png">

For this analysis, two of the five pavement types used on Seattle streets were categorized as asphalt (asphalt and composite pavement), while the other three were excluded. Composite pavement is concrete, brick, or another type of rigid pavement that has been topped with a layer of asphalt (SDOT). Because Asphalt makes up the top layer of pavement, composite pavement maintains the heat absorption nature of asphalt.

<img width="369" alt="Screen Shot 2022-05-08 at 3 03 40 PM" src="https://user-images.githubusercontent.com/98435077/167317666-85d9332b-ae88-4667-afce-b090b13244e0.png">

The percentage of streets paved with asphalt in each census tract was calculated by dividing the asphalt and composite road segment lengths by the total length of roads in each census tract. Approximately 35% of the streets in Seattle are either paved with asphalt or composite materials (SDOT). However, asphalt streets are not distributed evenly throughout the city. Central Seattle is much more likely to have asphalt streets when compared to North and South Seattle. 

### Building Density/ Thermal Mass
Nearly half of all developable land in Seattle is zoned for single-family housing (Adlin, 2021). While upzoning and urban infill is typically heralded as a solution to urban sprawl and a way to reduce greenhouse gas emissions, denser, larger buildings have a higher thermal mass, absorbing more heat and increasing urban temperatures (Ng et al., 2011).

<img width="373" alt="Screen Shot 2022-05-07 at 2 59 59 PM" src="https://user-images.githubusercontent.com/98435077/167273188-75631301-63c8-43d1-97d3-39756a2a4052.png">

As a proxy to understand the effects of dense urban development on UHI, I returned to the city's zoning code and combined areas that are zoned as Commercial, Downtown, Mixed Use, Multi-Family Housing, and Major Institutions into one denser urban development category. While zoning is not a perfect proxy to calculate the thermal mass of buildings and does not allow us to see variation within these areas, it gives us a strong indication of where denser urban development exists in the city.

<img width="373" alt="Screen Shot 2022-05-07 at 3 00 30 PM" src="https://user-images.githubusercontent.com/98435077/167273192-02838d3b-c7a6-4901-8656-3bdb678e6f91.png">

Like the Industrial zoning map, the map above shows the percentage of each census tract zoned for higher density development. Seattle’s “Urban Villages” Policy, which was initially adopted in the 1990s, diversified the location of higher density development in the city, so it was not solely concentrated in the city’s core (Beekman, 2021). While 81% of Seattle's residential zoning is still single-family, urban villages and neighborhood upzoning have created pockets of higher-density zoning throughout the city (Badger and Bui, 2019).

### Weighting & Combining Data to Predict Heat Vulnerability
To compare the data, I first needed to normalize each data set so they were all on the same scale. For each data set, I used the following formula:

  _X normalized = (x – x minimum) / range of X_

This made the range of all values across all the data sets fall between 0 and 1, so they are easily comparable and can be combined.

Next, I weighted each data set by how big of a role it plays in the severity of the Urban Heat Island effect. I determined weights based on my research of how much each factor influences UHI and how accurately I think the data reflects the true metric I am trying to measure. For example, the Industrial and Higher Density Development maps were given lower weights because they provide rougher pictures of the true nature of air pollution and urban density, respectively. The weights are as follows:

- Urban Canopy: **.30**
- Air Pollution from Vehicle Traffic: **.25**
- Air Pollution from Industry: **.10**
- Surface Type (Asphalt): **.20**
- Building Density: **.15**
  
Once the weights were applied, I combined the five values to create an Urban Heat Island risk score for each census tract. All normalized and weighted vehicle traffic, industry, surface type, and building density data were added together to increase risk scores, the urban canopy data set was subtracted to reduce overall risk scores. This is also why census tracts can have net negative risk scores.

### KEY FINDINGS

<img width="368" alt="Screen Shot 2022-05-08 at 3 04 17 PM" src="https://user-images.githubusercontent.com/98435077/167317649-de12d4d5-1632-4f2c-9bbf-c7318dbbfd49.png">

### Already Disadvantaged Census Tracts are more likely to experience Higher Temperatures

### CONCLUSION

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
