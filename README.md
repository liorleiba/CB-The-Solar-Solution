# CB-The-Solar-Solution
### **General description:**
A project analyzing the rapid growth, development, global spread and other ongoing activities of solar energy farms on recent decades around the globe. <br>
###### The project was done as a part of a Code-Bridge competition hosted by Yandex.Practicum. <br>
Feel free to check the project's landing page created by my partner: [Reference>>](https://qiuhanzhou.github.io/CODEBRIDGE/)

---

### Used Technology:
**Python Version:** 3.9.12 <br>
**Packages:** pandas, numpy, scipy, matplotlib, seaborn, plotly, missingno, geopy, itertools, translators, loguru, pathos, re, requests

---
### **Project's cause and purpose:**
When residential solar energy equipment was first made available to homeowners it was costly. The people who made the switch were usually those who wanted to make a conscious effort to reduce their carbon footprints. But they also had the means to invest in the equipment and services needed to make that switch. In the beginning, like many other new technologies, initial adopters often paid more until the technologies become more mainstream.

Yes, solar energy is increasingly becoming a viable fuel source for everyone. Today, switching to solar energy is far more affordable with the help of programs like the Investment Tax Credit (ITC). This incentive provides a tax credit of 26 percent of the cost to install solar power at your home. While this credit is in effect at 26% until the end of 2022, once it expires, solar energy will still remain a low-priced source of power as prices will most likely continue to drop. Meanwhile, oil, gas, and coal prices are likely to continue to increase, especially as sources are depleted and the costs to obtain these fuels grow.

I've explored the alternate solution to the energy problem, which is **the solar market**. I've researched it's growth and it's spread globally in the past years, to see how the world is running into the inevitable shifting to using solar energy as the planet's main resource.

---
## Geomapped missing locations

Created a selective reverse geomapping function which is able to reverse-mapped `lat-lon` formatted coordinates according to a given query parameter to find accurate addresses, with a punctuality that moves deeply from mapping the coordinnates continent, country and state, up to the suburb and street name. <br>
Values are available to be received both in the English language (The default), in the local language of a location, or at any other defined language available (internal). <br>

Used that function to fill 4 different location columns, all missing-values-inclusive, ranging from 7% up to 47% missing values of each column. 


## Explored global energy output

Visualized a heatmap showcasing the capacity of each declared solar plant on Earth using the coordinates of each solar project on the data. The plot can be used in order to identify countries and areas that invest deeper on solar energy than others. <br>
###### *For example, below you can see a zoomed screenshot of Asia's countries' solar energy output:*<br>

![A zoomed look of china](https://github.com/liorleiba/CB-The-Solar-Solution/blob/solar-patch-2/images/newplot%20(1).png)


## Data cleaning

Used some heavy tools like the `missingno` library to explore the missing-values columns' possible connections and handling options across the 15 out of the 27 columns of the data which contained missing values.

##### Some exploratory plotting methods with `missingno` used in the project:

###### ***A nullity bar chart that represent the amount of non-missing values on each column:*** 
![image](https://user-images.githubusercontent.com/117908614/201458019-b539f62e-f3d3-42b1-b8aa-990ea1448d26.png)
###### ***A nullity correlation dendrogram; the closer the connected columns' tail, the stronger the appearance correlation:***
![image](https://github.com/liorleiba/CB-The-Solar-Solution/blob/solar-patch-2/images/image.png)

---
## The Dataset

The analyzed "Global Solar Power Tracker" data contains 27 columns describing different aspects of solar energy projects that their rows are grouped by the hosting country of each (Alphabetically). <br>
Each of the rows represents a single solar project's (*at a certain developement status stage*) unique characteristics information, the main ones are:
* <b><i>Project name</i></b>.
* <b><i>Energy capacity</i></b> information.
* <b><i>Developement status stage</i></b>.
* The <b><i>start year</i></b> the dev. status stage began, and also <b><i>retired year</i></b>, if available.
* <b><i>Coordinates</i></b> (Latitude-Longitude) and <b><i>location columns</i></b> ranging from continental region to city of the solar project.
* <b><i>Ownership</i></b> / <b><i>Operator</i></b> names.

The dataset also contains local language names for non-English native countries for a few of the above aspects and others, as well as a Wikipedia page link for each project.

###### ***Disclaimer Note:*** *The analyzed dataset contains the initials '[GEM](https://globalenergymonitor.org/)', which stands for the "Global Energy Monitor", an organization that monitors the global energy markets status around the world. The dataset was taken straightly from the GEM data sources.*
